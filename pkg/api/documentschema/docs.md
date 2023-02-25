# Protocol Documentation
<a name="top"></a>

## Table of Contents

- [documentschema.proto](#documentschema.proto)
    - [CollectionCreateRequest](#immudb.documentschema.CollectionCreateRequest)
    - [CollectionCreateRequest.IndexKeysEntry](#immudb.documentschema.CollectionCreateRequest.IndexKeysEntry)
    - [CollectionCreateRequest.PrimaryKeysEntry](#immudb.documentschema.CollectionCreateRequest.PrimaryKeysEntry)
    - [CollectionCreateResponse](#immudb.documentschema.CollectionCreateResponse)
    - [CollectionDeleteRequest](#immudb.documentschema.CollectionDeleteRequest)
    - [CollectionDeleteResponse](#immudb.documentschema.CollectionDeleteResponse)
    - [CollectionGetRequest](#immudb.documentschema.CollectionGetRequest)
    - [CollectionGetResponse](#immudb.documentschema.CollectionGetResponse)
    - [CollectionInformation](#immudb.documentschema.CollectionInformation)
    - [CollectionInformation.IndexKeysEntry](#immudb.documentschema.CollectionInformation.IndexKeysEntry)
    - [CollectionInformation.PrimaryKeysEntry](#immudb.documentschema.CollectionInformation.PrimaryKeysEntry)
    - [CollectionListRequest](#immudb.documentschema.CollectionListRequest)
    - [CollectionListResponse](#immudb.documentschema.CollectionListResponse)
    - [DocumentAudit](#immudb.documentschema.DocumentAudit)
    - [DocumentAuditRequest](#immudb.documentschema.DocumentAuditRequest)
    - [DocumentAuditRequest.PrimaryKeysEntry](#immudb.documentschema.DocumentAuditRequest.PrimaryKeysEntry)
    - [DocumentAuditResponse](#immudb.documentschema.DocumentAuditResponse)
    - [DocumentInsertRequest](#immudb.documentschema.DocumentInsertRequest)
    - [DocumentInsertResponse](#immudb.documentschema.DocumentInsertResponse)
    - [DocumentProofRequest](#immudb.documentschema.DocumentProofRequest)
    - [DocumentProofRequest.PrimaryKeysEntry](#immudb.documentschema.DocumentProofRequest.PrimaryKeysEntry)
    - [DocumentProofResponse](#immudb.documentschema.DocumentProofResponse)
    - [DocumentQuery](#immudb.documentschema.DocumentQuery)
    - [DocumentSearchRequest](#immudb.documentschema.DocumentSearchRequest)
    - [DocumentSearchResponse](#immudb.documentschema.DocumentSearchResponse)
    - [IndexOption](#immudb.documentschema.IndexOption)
    - [IndexValue](#immudb.documentschema.IndexValue)
    - [Proof](#immudb.documentschema.Proof)
  
    - [IndexType](#immudb.documentschema.IndexType)
    - [QueryOperator](#immudb.documentschema.QueryOperator)
  
    - [DocumentService](#immudb.documentschema.DocumentService)
  
- [Scalar Value Types](#scalar-value-types)



<a name="documentschema.proto"></a>
<p align="right"><a href="#top">Top</a></p>

## documentschema.proto



<a name="immudb.documentschema.CollectionCreateRequest"></a>

### CollectionCreateRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |
| primaryKeys | [CollectionCreateRequest.PrimaryKeysEntry](#immudb.documentschema.CollectionCreateRequest.PrimaryKeysEntry) | repeated |  |
| indexKeys | [CollectionCreateRequest.IndexKeysEntry](#immudb.documentschema.CollectionCreateRequest.IndexKeysEntry) | repeated |  |






<a name="immudb.documentschema.CollectionCreateRequest.IndexKeysEntry"></a>

### CollectionCreateRequest.IndexKeysEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [IndexOption](#immudb.documentschema.IndexOption) |  |  |






<a name="immudb.documentschema.CollectionCreateRequest.PrimaryKeysEntry"></a>

### CollectionCreateRequest.PrimaryKeysEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [IndexOption](#immudb.documentschema.IndexOption) |  |  |






<a name="immudb.documentschema.CollectionCreateResponse"></a>

### CollectionCreateResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collection | [CollectionInformation](#immudb.documentschema.CollectionInformation) |  |  |






<a name="immudb.documentschema.CollectionDeleteRequest"></a>

### CollectionDeleteRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |






<a name="immudb.documentschema.CollectionDeleteResponse"></a>

### CollectionDeleteResponse







<a name="immudb.documentschema.CollectionGetRequest"></a>

### CollectionGetRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |






<a name="immudb.documentschema.CollectionGetResponse"></a>

### CollectionGetResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collection | [CollectionInformation](#immudb.documentschema.CollectionInformation) |  |  |






<a name="immudb.documentschema.CollectionInformation"></a>

### CollectionInformation



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |
| primaryKeys | [CollectionInformation.PrimaryKeysEntry](#immudb.documentschema.CollectionInformation.PrimaryKeysEntry) | repeated |  |
| indexKeys | [CollectionInformation.IndexKeysEntry](#immudb.documentschema.CollectionInformation.IndexKeysEntry) | repeated |  |






<a name="immudb.documentschema.CollectionInformation.IndexKeysEntry"></a>

### CollectionInformation.IndexKeysEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [IndexOption](#immudb.documentschema.IndexOption) |  |  |






<a name="immudb.documentschema.CollectionInformation.PrimaryKeysEntry"></a>

### CollectionInformation.PrimaryKeysEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [IndexOption](#immudb.documentschema.IndexOption) |  |  |






<a name="immudb.documentschema.CollectionListRequest"></a>

### CollectionListRequest







<a name="immudb.documentschema.CollectionListResponse"></a>

### CollectionListResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collections | [CollectionInformation](#immudb.documentschema.CollectionInformation) | repeated |  |






<a name="immudb.documentschema.DocumentAudit"></a>

### DocumentAudit



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| value | [google.protobuf.Struct](#google.protobuf.Struct) |  |  |
| transactionID | [uint64](#uint64) |  |  |






<a name="immudb.documentschema.DocumentAuditRequest"></a>

### DocumentAuditRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collection | [string](#string) |  |  |
| primaryKeys | [DocumentAuditRequest.PrimaryKeysEntry](#immudb.documentschema.DocumentAuditRequest.PrimaryKeysEntry) | repeated |  |
| page | [uint32](#uint32) |  |  |
| perPage | [uint32](#uint32) |  |  |






<a name="immudb.documentschema.DocumentAuditRequest.PrimaryKeysEntry"></a>

### DocumentAuditRequest.PrimaryKeysEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [IndexValue](#immudb.documentschema.IndexValue) |  |  |






<a name="immudb.documentschema.DocumentAuditResponse"></a>

### DocumentAuditResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| results | [DocumentAudit](#immudb.documentschema.DocumentAudit) | repeated |  |
| page | [uint32](#uint32) |  |  |
| perPage | [uint32](#uint32) |  |  |
| entriesLeft | [uint32](#uint32) |  |  |






<a name="immudb.documentschema.DocumentInsertRequest"></a>

### DocumentInsertRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collection | [string](#string) |  |  |
| document | [google.protobuf.Struct](#google.protobuf.Struct) | repeated |  |






<a name="immudb.documentschema.DocumentInsertResponse"></a>

### DocumentInsertResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| proof | [immudb.schema.VerifiableTx](#immudb.schema.VerifiableTx) |  |  |






<a name="immudb.documentschema.DocumentProofRequest"></a>

### DocumentProofRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collection | [string](#string) |  |  |
| primaryKeys | [DocumentProofRequest.PrimaryKeysEntry](#immudb.documentschema.DocumentProofRequest.PrimaryKeysEntry) | repeated |  |
| atRevision | [int64](#int64) |  |  |






<a name="immudb.documentschema.DocumentProofRequest.PrimaryKeysEntry"></a>

### DocumentProofRequest.PrimaryKeysEntry



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| key | [string](#string) |  |  |
| value | [IndexValue](#immudb.documentschema.IndexValue) |  |  |






<a name="immudb.documentschema.DocumentProofResponse"></a>

### DocumentProofResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| proof | [immudb.schema.VerifiableTx](#immudb.schema.VerifiableTx) |  |  |






<a name="immudb.documentschema.DocumentQuery"></a>

### DocumentQuery



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| field | [string](#string) |  |  |
| operator | [QueryOperator](#immudb.documentschema.QueryOperator) |  |  |
| value | [google.protobuf.Value](#google.protobuf.Value) |  |  |






<a name="immudb.documentschema.DocumentSearchRequest"></a>

### DocumentSearchRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| collection | [string](#string) |  |  |
| query | [DocumentQuery](#immudb.documentschema.DocumentQuery) | repeated |  |
| page | [uint32](#uint32) |  |  |
| perPage | [uint32](#uint32) |  |  |






<a name="immudb.documentschema.DocumentSearchResponse"></a>

### DocumentSearchResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| results | [google.protobuf.Struct](#google.protobuf.Struct) | repeated |  |
| page | [uint32](#uint32) |  |  |
| perPage | [uint32](#uint32) |  |  |
| entriesLeft | [uint32](#uint32) |  |  |






<a name="immudb.documentschema.IndexOption"></a>

### IndexOption



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| type | [IndexType](#immudb.documentschema.IndexType) |  |  |






<a name="immudb.documentschema.IndexValue"></a>

### IndexValue



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| null_value | [google.protobuf.NullValue](#google.protobuf.NullValue) |  |  |
| number_value | [double](#double) |  |  |
| string_value | [string](#string) |  |  |
| bool_value | [bool](#bool) |  |  |






<a name="immudb.documentschema.Proof"></a>

### Proof



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  |  |





 


<a name="immudb.documentschema.IndexType"></a>

### IndexType


| Name | Number | Description |
| ---- | ------ | ----------- |
| DOUBLE | 0 |  |
| INTEGER | 1 |  |
| STRING | 2 |  |



<a name="immudb.documentschema.QueryOperator"></a>

### QueryOperator


| Name | Number | Description |
| ---- | ------ | ----------- |
| EQ | 0 |  |
| GT | 1 |  |
| GTE | 2 |  |
| LT | 3 |  |
| LTE | 4 |  |
| LIKE | 5 |  |


 

 


<a name="immudb.documentschema.DocumentService"></a>

### DocumentService


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| DocumentInsert | [DocumentInsertRequest](#immudb.documentschema.DocumentInsertRequest) | [DocumentInsertResponse](#immudb.documentschema.DocumentInsertResponse) |  |
| DocumentSearch | [DocumentSearchRequest](#immudb.documentschema.DocumentSearchRequest) | [DocumentSearchResponse](#immudb.documentschema.DocumentSearchResponse) |  |
| DocumentAudit | [DocumentAuditRequest](#immudb.documentschema.DocumentAuditRequest) | [DocumentAuditResponse](#immudb.documentschema.DocumentAuditResponse) |  |
| DocumentProof | [DocumentProofRequest](#immudb.documentschema.DocumentProofRequest) | [DocumentProofResponse](#immudb.documentschema.DocumentProofResponse) |  |
| CollectionCreate | [CollectionCreateRequest](#immudb.documentschema.CollectionCreateRequest) | [CollectionCreateResponse](#immudb.documentschema.CollectionCreateResponse) |  |
| CollectionGet | [CollectionGetRequest](#immudb.documentschema.CollectionGetRequest) | [CollectionGetResponse](#immudb.documentschema.CollectionGetResponse) |  |
| CollectionList | [CollectionListRequest](#immudb.documentschema.CollectionListRequest) | [CollectionListResponse](#immudb.documentschema.CollectionListResponse) |  |
| CollectionDelete | [CollectionDeleteRequest](#immudb.documentschema.CollectionDeleteRequest) | [CollectionDeleteResponse](#immudb.documentschema.CollectionDeleteResponse) |  |

 



## Scalar Value Types

| .proto Type | Notes | C++ | Java | Python | Go | C# | PHP | Ruby |
| ----------- | ----- | --- | ---- | ------ | -- | -- | --- | ---- |
| <a name="double" /> double |  | double | double | float | float64 | double | float | Float |
| <a name="float" /> float |  | float | float | float | float32 | float | float | Float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum or Fixnum (as required) |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int | uint32 | uint | integer | Bignum or Fixnum (as required) |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long | uint64 | ulong | integer/string | Bignum |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int | int32 | int | integer | Bignum or Fixnum (as required) |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long | int64 | long | integer/string | Bignum |
| <a name="bool" /> bool |  | bool | boolean | boolean | bool | bool | boolean | TrueClass/FalseClass |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode | string | string | string | String (UTF-8) |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str | []byte | ByteString | string | String (ASCII-8BIT) |
