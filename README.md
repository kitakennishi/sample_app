 * Ruby 2.1.0 
 * Rails 4.1.0
 * Node.js

Rails チュートリアル-3章 から


#### メモ1
******

RSpec
```ruby
require 'spec_helper'

describe User do

  before { @user = User.new(name: "Example User", email: "user@example.com") }

  subject { @user }

  it { should respond_to(:name) }
  it { should respond_to(:email) }
end
```

これをexpectを使用すると
まずsubjectがいらなくなる

```ruby
require 'spec_helper'

describe User do

  before { @user = User.new(name: "Example User", email: "user@example.com") }

  it { expect(@user).to respond_to(:name) }
  it { expect(@user).to respond_to(:email) }
end
```

#### メモ2
******

行末削除
```
$ find **/*.rb | xargs perl -p -i -e 's/\s+$/\n/'
```

