Rails 7 サンプル minitest
=========================

[![Build status][shield-build]](#)
[![MIT licensed][shield-license]](#)
[![Rails][shield-rails]][rails]

Rails minitest のサンプル

## Table of Contents

* [Technologies](#technologies)
* [Demo](#demo)
* [How to make](#how-to-make)
* [Usage](#usage)
* [References](#references)
* [License](#license)

## Technologies

* [Rails][rails] 7.0.3.1
* [PostgreSQL][postgresql]

## Demo

* https://sample-rails7-minitest.fkoba.com

## How to make

### Rails アプリケーション作成

```sh
$ git clone git@github.com:kyuuki/sample-rails7-base.git sample-rails7-minitest
$ cd sample-rails7-minitest
```

### GitHub

- GitHub に sample-rails7-minitest という名前でリポジトリ追加


```sh
$ git remote set-url origin git@github.com:kyuuki/sample-rails7-minitest.git
$ git push
```

### factory_bot 導入

1. gem 追加 [(commit)](https://github.com/kyuuki/sample-rails7-minitest/commit/1e0a4c6c62a7b92565379857dba3bdd88f4035b8#diff-d09ea66f8227784ff4393d88a19836f321c915ae10031d16c93d67e6283ab55f)  
   $ bundle install
2. test/fixtures ディレクトリ削除
3. test/test_helper.rb から fixtures :all 削除 [(commit)](https://github.com/kyuuki/sample-rails7-minitest/commit/1e0a4c6c62a7b92565379857dba3bdd88f4035b8#diff-ba37813ca277c227a74a372479b7b05b7f3ff085d890ab708f80d62573efdb7a)


### システムテスト追加

1. test/application_system_test_case.rb を編集
2. $ rails g system_test static_page
3. テストコード追加
4. テスト実行  
   $ rails test:system

## Usage

```sh
$ git clone git@github.com:kyuuki/sample-rails7-minitest.git
$ cd sample-rails7-minitest
$ bundle install
$ rails db:create
$ rails s -b 0.0.0.0
```
<!-- $ rails db:migrate (今回は不要) -->

## References

* [factory_bot (英)](https://github.com/thoughtbot/factory_bot)
* [Rails テスティングガイド (日)](https://railsguides.jp/testing.html)

## License

This is licensed under the [MIT](https://choosealicense.com/licenses/mit/) license.  
Copyright &copy; 2022 [Fuji Programming Laboratory](https://fuji-labo.com/)



[rails]: https://rubyonrails.org/
[postgresql]: https://www.postgresql.org/

[shield-build]: https://img.shields.io/badge/build-passing-brightgreen.svg
[shield-license]: https://img.shields.io/badge/license-MIT-blue.svg
[shield-rails]: https://img.shields.io/badge/-Rails-CC0000.svg?logo=ruby-on-rails&style=flat
