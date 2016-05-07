<a name="0.3.0"></a>
# [0.3.0](https://github.com/mattlewis92/angular2-bootstrap-confirm/compare/0.2.0...v0.3.0) (2016-05-07)


### Features

* **position:** rename PositionService to Position ([5c05e4e](https://github.com/mattlewis92/angular2-bootstrap-confirm/commit/5c05e4e)), closes [#11](https://github.com/mattlewis92/angular2-bootstrap-confirm/issues/11)


### BREAKING CHANGES

* position: PositionService has now been renamed to Position. Use it like so:
```
import {Position} from 'angular2-bootstrap-confirm';
import {PositionService} from 'ng2-bootstrap/components/position';
provide(Position, {useClass: PositionService})
```



<a name="0.2.0"></a>
# [0.2.0](https://github.com/mattlewis92/angular2-bootstrap-confirm/compare/v0.1.0...v0.2.0) (2016-05-07)


### Features

* **angular2:** upgrade to angular2 RC1 ([d4d3c6b](https://github.com/mattlewis92/angular2-bootstrap-confirm/commit/d4d3c6b))
* **buttons:** allow hiding of the confirm / cancel buttons ([540b965](https://github.com/mattlewis92/angular2-bootstrap-confirm/commit/540b965)), closes [#10](https://github.com/mattlewis92/angular2-bootstrap-confirm/issues/10)
* **position:** provide a bundled copy of the position service so ng2-bootstrap isn't required as a peer dependency ([37b295f](https://github.com/mattlewis92/angular2-bootstrap-confirm/commit/37b295f))
* allow usage without a module bundler by providing a standalone position bundle ([9ebae67](https://github.com/mattlewis92/angular2-bootstrap-confirm/commit/9ebae67)), closes [#8](https://github.com/mattlewis92/angular2-bootstrap-confirm/issues/8)
* add bootstrap v4 classes ([3f4959f2](https://github.com/mattlewis92/angular2-bootstrap-confirm/commit/3f4959f2))

### BREAKING CHANGES

* position: you now need to provide the position service for the directive to use like so:
```
import {provide} from '@angular/core';
import {bootstrap} from '@angular/platform-browser-dynamic';
import {Confirm, ConfirmOptions, PositionService} from 'angular2-bootstrap-confirm';
import {PositionService as Ng2PositionService} from 'ng2-bootstrap/components/position';
// Or if you don't want to depend on the ng2-bootstrap module, use the bundled position service:
// import {PositionService as Ng2PositionService} from 'angular2-bootstrap-confirm/position/position';
bootstrap(MyApp, [
   provide(PositionService, {useClass: Ng2PositionService})
]);
```
* angular2: a peer dependency of angular2 RC1 is now required



# 0.1.0
_Initial release_