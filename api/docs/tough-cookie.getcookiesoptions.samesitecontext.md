<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [tough-cookie](./tough-cookie.md) &gt; [GetCookiesOptions](./tough-cookie.getcookiesoptions.md) &gt; [sameSiteContext](./tough-cookie.getcookiesoptions.samesitecontext.md)

## GetCookiesOptions.sameSiteContext property

Set this to 'none', 'lax', or 'strict' to enforce SameSite cookies upon retrieval.

- `'strict'` - If the request is on the same "site for cookies" (see the RFC draft for more information), pass this option to add a layer of defense against CSRF.

- `'lax'` - If the request is from another site, but is directly because of navigation by the user, such as, `<link type=prefetch>` or `<a href="...">`<!-- -->, then use `lax`<!-- -->.

- `'none'` - This indicates a cross-origin request.

- `undefined` - SameSite is not be enforced! This can be a valid use-case for when CSRF isn't in the threat model of the system being built.

Defaults to `undefined` if not provided.

**Signature:**

```typescript
sameSiteContext?: 'none' | 'lax' | 'strict' | undefined;
```

## Remarks

- It is highly recommended that you read [RFC6265bis - Section 8.8](https://tools.ietf.org/html/draft-ietf-httpbis-rfc6265bis-02##section-8.8) which discusses security considerations and defence on SameSite cookies in depth.
