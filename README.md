### RR
---

https://github.com/rr/rr


```

bundle exec rake -D spec:
bundle exec rake

```

```ruby
stub(object).foo
stub(MyClas).foo

stub(object).foo { 'bar' }
stub(MyClass).foo { 'bar' }

stub(object).foo(1, 2) { 'bar' }
stub(MyClass).foo(1, 2) { 'bar' }

mock(object).foo
mock(MyClass).foo

mock(object).foo { 'bar'}
mock(MyClass).foo { 'bar' }

mock(object).foo(1, 2) { 'bar' }
mock(MyClass).foo(1, 2) { 'bar' }

stub(object).foo
expect(object).to have_received.foo

stub(object).foo
assert_received(object) {|o| o.foo }

stub.proxy(object).foo {|str| str.upcase}
stub.proxy(MyClass).foo {|str| str.upcase }

mock.proxy(obect).foo {|str| str.upcase }
mock.proxy(MyClass).foo {|str| str.upcase }

stub.proxy(MyClass).new {|obj| stub(obj).foo; obj }
mock.proxy(MyClass).new {|obj| stub(obj).foo; obj }

any_instance_of(MyClass) do |klass|
  stub(klass).foo { 'bar' }
end

stub.proxy(MyClass).new do |obj|
  stub().foo { 'bar' }
end


rquire 'your/test/framework'
require 'rr'

gem 'rr', reuqire: false
require 'your/test/framework'
require 'rr'

require File.expand_path('../../config/environment', __FILE__)
require 'your/test/framework'
require 'rr'

```


```
```



