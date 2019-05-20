# BRAKEMAN REPORT

| Application path                              | Rails version | Brakeman version | Started at                | Duration         |
|-----------------------------------------------|---------------|------------------|---------------------------|------------------|
| /Users/garykrause/repos/operationcode_backend | 5.0.7         | 4.5.1            | 2019-05-19 20:42:15 -0400 | 0.400835 seconds |

| Checks performed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BasicAuth, BasicAuthTimingAttack, ContentTag, CreateWith, CrossSiteScripting, DefaultRoutes, Deserialize, DetailedExceptions, DigestDoS, DynamicFinders, EscapeFunction, Evaluation, Execute, FileAccess, FileDisclosure, FilterSkipping, ForgerySetting, HeaderDoS, I18nXSS, JRubyXML, JSONEncoding, JSONParsing, LinkTo, LinkToHref, MailTo, MassAssignment, MimeTypeDoS, ModelAttrAccessible, ModelAttributes, ModelSerialize, NestedAttributes, NestedAttributesBypass, NumberToCurrency, PermitAttributes, QuoteTableName, Redirect, RegexDoS, Render, RenderDoS, RenderInline, ResponseSplitting, RouteDoS, SQL, SQLCVEs, SSLVerify, SafeBufferManipulation, SanitizeMethods, SelectTag, SelectVulnerability, Send, SendFile, SessionManipulation, SessionSettings, SimpleFormat, SingleQuotes, SkipBeforeFilter, SprocketsPathTraversal, StripTags, SymbolDoSCVE, TranslateBug, UnsafeReflection, ValidationRegex, WithoutProtection, XMLDoS, YAMLParsing |

### SUMMARY

| Scanned/Reported  | Total |
|-------------------|-------|
| Controllers       | 29    |
| Models            | 18    |
| Templates         | 16    |
| Errors            | 0     |
| Security Warnings | 2 (0) |

| Warning Type               | Total |
|----------------------------|-------|
| Cross-Site Request Forgery | 1     |
| Mass Assignment            | 1     |

### SECURITY WARNINGS

| Confidence | Class                          | Method             | Warning Type                                                                       | Message                                                                                                                                     |
|------------|--------------------------------|--------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
|            | Api::V1::TeamMembersController | team_member_params | [Mass Assignment](https://brakemanscanner.org/docs/warning_types/mass_assignment/) | Potentially dangerous key allowed for mass assignment near line 39: `params.permit(:name, :role, :group, :description, :image_src, :email)` |

### Controller Warnings:

| Confidence | Controller            | Warning Type                                                                                             | Message                                                                                                                         |
|------------|-----------------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
|            | ApplicationController | [Cross-Site Request Forgery](https://brakemanscanner.org/docs/warning_types/cross-site_request_forgery/) | `protect_from_forgery` should be configured with `with: :exception` near line 4: `protect_from_forgery(:with => :null_session)` |

