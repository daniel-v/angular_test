# Changelog

## 1.0.0-alpha+4

- Update `pubspec.yaml` so it properly lists AngularDart `3.0.0-alpha`

## 1.0.0-alpha+3

- Fix the executable so `pub run angular_test` can be used

## 1.0.0-alpha+2

- Add built-in support for `package:pageloader`:

```dart
final fixture = await new NgTestBed<TestComponent>().create();
final pageObject = await fixture.getPageObject/*<ClickCounterPO>*/(
  ClickCounterPO,
);
expect(await pageObject.button.visibleText, 'Click count: 0');
await pageObject.button.click();
expect(await pageObject.button.visibleText, 'Click count: 1');
```

- Fix a serious generic type error when `NgTestBed` is forked

- Fix a generic type error
- Added `compatibility.dart`, a temporary API to some users migrate

Changes to `compatibility.dart` might not be considered in future semver
updates, and it **highly suggested** you don't use these APIs for any new code.

## 1.0.0-alpha+1

- Change `NgTextFixture.update` to have a single optional parameter

## 1.0.0-alpha

- Initial commit with compatibility for AngularDart `2.2.0`
