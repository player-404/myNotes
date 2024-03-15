### - Schema 是什么？
Schema 是mongoose的模式，它定义了字段的数据结构与数据类型

### - 使用 Schema
#### 1.定义 Schema
使用 new 创建 schema 实例
```javascript
const blogSchema = new Schema({
  title: String, // String is shorthand for {type: String}
  author: String,
  body: String,
  comments: [{ body: String, date: Date }],
  date: { type: Date, default: Date.now },
  hidden: Boolean,
  meta: {
    votes: Number,
    favs: Number
  }
});
```
#### 2.使用 Schema
将 Schema 串入 model 使用 Schema
```javascript
const Blog = mongoose.model('Blog', blogSchema);
```

### - 为文档（documents）实例添加方法
```ad-tip
Model(模型的实例是文档)
```
在 Schema 的 methods 属性对象中添加方法,该方法会添加到文档实例上

```javascript
animalSchema.methods.findSimilarTypes = function(cb) {
  return mongoose.model('Animal').find({ type: this.type }, cb);
};
const Animal = mongoose.model('Animal', animalSchema);
const dog = new Animal({ type: 'dog' });

dog.findSimilarTypes((err, dogs) => {
  console.log(dogs); // woof
});
```


