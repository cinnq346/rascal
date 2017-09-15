# Change Log

## [2.0.0]
### Fixed
- Connection pool was leaking connections following a connection error. With a pool size of 1, this locked up all publishers
- Listening to close and error events caused multiple channels to be created which appears to result in an unknown delivery tag error. See https://github.com/squaremo/amqp.node/issues/271
- Incorrect documenation said to listen for invalid_content, but in reality the event was invalid_message. Now emitting invalid_message only if invalid_content is not handled.
- Fixed examples

## [1.4.1]
### Fixed
- confirmPoolSize option as per https://github.com/guidesmiths/rascal/pull/19

## [1.4.0]
### Added
- Listing to connection close events as per #18
- Fixed bug with configuration which caused vhost config errors to be masked

## [1.3.1]
### Added
- Channel pooling (makes publishing much faster)

### Updated
- Dependencies

## [1.2.1]
### Updated
- Used wrong argument in callback

## [1.2.0]
### Added
- Workaround for https://github.com/guidesmiths/rascal/issues/17

## [1.1.0]
### Added
- This changelog
- License
- Badges
- Upgrading dependencies

The format is based on [Keep a Changelog](http://keepachangelog.com/)