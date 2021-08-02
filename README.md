# TYPO3 CMS distribution for testing my extensions

This is a TYPO3 distribution which I use to manually test my extensions:

- [crowdfunding](https://github.com/oliverklee/ext-crowdfunding)
  (once it supports TYPO3 9LTS)
- [csv_to_openimmo](https://github.com/oliverklee/ext-csv_to_openimmo)
  (once it supports TYPO3 9LTS)
- [feuserextrafields](https://github.com/oliverklee/ext-feuserextrafields)
  (once I have rewritten it)
- [oelib](https://github.com/oliverklee/ext-oelib)
- [onetimeaccount](https://github.com/oliverklee/ext-onetimeaccount)
- [realty](https://github.com/oliverklee/ext-realty)
  (once it supports TYPO3 9LTS)
- [seminars](https://github.com/oliverklee/ext-seminars)
- [tea](https://github.com/TYPO3-Documentation/tea)
- [site package](https://github.com/oliverklee/typo3-devsite)

## Usage

This distribution uses [ddev](https://github.com/drud/ddev).

### Initializing the project

```bash
ddev start
ddev install-typo3
```

## Database dump and import

There are two commands available for dumping the database and for importing the
dump to and from the file `dump.sql`:

```bash
ddev db-dump
ddev db-import
```

The dump includes (and hence overwrite on import) FE users and FE user groups,
but not BE users or BE user groups. (So it is safe to add BE users and then
run the import.)

## Relevant URLs and launch options

- Backend:
  - https://typo3-testing-distribution.ddev.site:8081/typo3/
  - `ddev launch /typo3`
- Frontend (DE):
  - https://typo3-testing.ddev.site:8081/
  - `ddev launch`
- Frontend (EN): https://typo3-testing-en.ddev.site:8081/
- MailHog:
  - https://typo3-testing.ddev.site:8026/
  - `ddev launch -m`

## Credentials

Backend admin: `admin` / `password`
Install tool password: `password`

Frontend users:
- `attendee` / `attendee`
- `editor` / `editor`
- `manager` / `manager`
