使用 XmlSerializer() 进行序列化xml时，要用

```csharp
XmlSerializer xmlSer = XmlSerializer.FromTypes(new[] { typeof(T) })[0];
```

替代

```csharp
XmlSerializer xmlSer = new XmlSerializer(typeof(T));
```