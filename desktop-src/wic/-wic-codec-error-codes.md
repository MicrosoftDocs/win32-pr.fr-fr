---
description: ce document contient la liste des codes d’erreur définis par le composant WIC (Windows Imaging Component).
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: Codes d’erreur du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb8f3911516f11c4a0614461786d6f94eaf00e038e53babb47d4df595797bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207258"
---
# <a name="codec-error-codes"></a>Codes d’erreur du codec

ce document contient la liste des codes d’erreur définis par le composant WIC (Windows Imaging Component).

-   [Erreurs WIC par code](#wic-errors-by-code)
-   [Erreurs WIC par valeur](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>Erreurs WIC par code

Le tableau suivant répertorie les codes d’erreur utilisés par le WICAPIs triés par ordre alphabétique. 

| Code d’erreur                                      | Valeur d’erreur                      |
|-------------------------------------------------|----------------------------------|
| \_Err WINCODEC \_ abandonnée                          | 0x80004004 (E \_ Abort)            |
| WINCODEC \_ Err \_ ACCESSDENIED                     | 0x80070005 (E \_ ACCESSDENIED)     |
| WINCODEC \_ Err \_ ALREADYLOCKED                    | 0x88982f0D                       |
| WINCODEC \_ Err \_ BADHEADER                        | 0x88982f61                       |
| WINCODEC \_ Err \_ BADIMAGE                         | 0x88982f60                       |
| WINCODEC \_ Err \_ BADMETADATAHEADER                | 0x88982f63                       |
| WINCODEC \_ Err \_ BADSTREAMDATA                    | 0x88982f70                       |
| WINCODEC \_ Err \_ CODECNOTHUMBNAIL                 | 0x88982f44                       |
| WINCODEC \_ Err \_ CODECPRESENT                     | 0x88982f43                       |
| WINCODEC \_ Err \_ CODECTOOMANYSCANLINES            | 0x88982f46                       |
| WINCODEC \_ Err \_ COMPONENTINITIALIZEFAILURE       | 0x88982f8B                       |
| WINCODEC \_ Err \_ COMPONENTNOTFOUND                | 0x88982f50                       |
| WINCODEC \_ Err \_ DUPLICATEMETADATAPRESENT         | 0x88982f8D                       |
| WINCODEC \_ Err \_ FRAMEMISSING                     | 0x88982f62                       |
| \_ \_ erreur générique WINCODEC \_ Err                   | 0x80004005 (E \_ Fail)             |
| WINCODEC \_ Err \_ IMAGESIZEOUTOFRANGE              | 0x88982f51                       |
| WINCODEC \_ Err \_ INSUFFICIENTBUFFER               | 0x88982f8C                       |
| WINCODEC \_ Err \_ INTERNALERROR                    | 0x88982f48                       |
| WINCODEC \_ Err \_ INVALIDPARAMETER                 | 0x80070057 (E \_ INVALIDARG)       |
| WINCODEC \_ Err \_ INVALIDQUERYCHARACTER            | 0x88982f93                       |
| WINCODEC \_ Err \_ INVALIDQUERYREQUEST              | 0x88982f90                       |
| WINCODEC \_ Err \_ INVALIDREGISTRATION              | 0x88982f8A                       |
| WINCODEC \_ Err \_ non implémenté                   | 0x80004001 (E \_ NOTIMPL)          |
| WINCODEC \_ Err \_ NOTINITIALIZED                   | 0x88982f0C                       |
| WINCODEC \_ Err \_ OUTOFMEMORY                      | 0x8007000E (E \_ OUTOFMEMORY)      |
| WINCODEC \_ Err \_ PALETTEUNAVAILABLE               | 0x88982f45                       |
| WINCODEC \_ Err \_ PROPERTYNOTFOUND                 | 0x88982f40                       |
| WINCODEC \_ Err \_ PROPERTYNOTSUPPORTED             | 0x88982f41                       |
| WINCODEC \_ Err \_ PROPERTYSIZE                     | 0x88982f42                       |
| WINCODEC \_ Err \_ PROPERTYUNEXPECTEDTYPE           | 0x88982f8E                       |
| WINCODEC \_ Err \_ REQUESTONLYVALIDATMETADATAROOT   | 0x88982f92                       |
| WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS | 0x88982f49                       |
| WINCODEC \_ Err \_ STREAMWRITE                      | 0x88982f71                       |
| WINCODEC \_ Err \_ STREAMREAD                       | 0x88982f72                       |
| WINCODEC \_ Err \_ STREAMNOTAVAILABLE               | 0x88982f73                       |
| WINCODEC \_ Err \_ TOOMUCHMETADATA                  | 0x88982f52                       |
| WINCODEC \_ Err \_ UNKNOWNIMAGEFORMAT               | 0x88982f07                       |
| WINCODEC \_ Err \_ UNEXPECTEDMETADATATYPE           | 0x88982f91                       |
| WINCODEC \_ Err \_ UNEXPECTEDSIZE                   | 0x88982f8F                       |
| WINCODEC \_ Err \_ UNSUPPORTEDOPERATION             | 0x88982f81                       |
| WINCODEC \_ Err \_ UNSUPPORTEDPIXELFORMAT           | 0x88982f80                       |
| WINCODEC \_ Err \_ UNSUPPORTEDVERSION               | 0x88982f0B                       |
| WINCODEC \_ Err \_ VALUEOUTOFRANGE                  | 0x88982f05                       |
| WINCODEC \_ Err \_ VALUEOVERFLOW                    | \_ \_ débordement arithmétique INTSAFE E \_ |
| WINCODEC \_ Err \_ WRONGSTATE                       | 0x88982f04                       |



 

## <a name="wic-errors-by-value"></a>Erreurs WIC par valeur

Le tableau suivant répertorie les codes d’erreur utilisés par le WICAPIs triés dans l’ordre numérique. 

| Code d’erreur                       | Valeur d’erreur                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_ Fail)             | \_ \_ erreur générique WINCODEC \_ Err                   |
| 0x80070057 (E \_ INVALIDARG)       | WINCODEC \_ Err \_ INVALIDPARAMETER                 |
| 0x8007000E (E \_ OUTOFMEMORY)      | WINCODEC \_ Err \_ OUTOFMEMORY                      |
| 0x80004001 (E \_ NOTIMPL)          | WINCODEC \_ Err \_ non implémenté                   |
| 0x80004004 (E \_ Abort)            | \_Err WINCODEC \_ abandonnée                          |
| 0x80070005 (E \_ ACCESSDENIED)     | WINCODEC \_ Err \_ ACCESSDENIED                     |
| \_ \_ débordement arithmétique INTSAFE E \_ | WINCODEC \_ Err \_ VALUEOVERFLOW                    |
| 0x88982f04                       | WINCODEC \_ Err \_ WRONGSTATE                       |
| 0x88982f05                       | WINCODEC \_ Err \_ VALUEOUTOFRANGE                  |
| 0x88982f07                       | WINCODEC \_ Err \_ UNKNOWNIMAGEFORMAT               |
| 0x88982f0B                       | WINCODEC \_ Err \_ UNSUPPORTEDVERSION               |
| 0x88982f0C                       | WINCODEC \_ Err \_ NOTINITIALIZED                   |
| 0x88982f0D                       | WINCODEC \_ Err \_ ALREADYLOCKED                    |
| 0x88982f40                       | WINCODEC \_ Err \_ PROPERTYNOTFOUND                 |
| 0x88982f41                       | WINCODEC \_ Err \_ PROPERTYNOTSUPPORTED             |
| 0x88982f42                       | WINCODEC \_ Err \_ PROPERTYSIZE                     |
| 0x88982f43                       | WINCODEC \_ Err \_ CODECPRESENT                     |
| 0x88982f44                       | WINCODEC \_ Err \_ CODECNOTHUMBNAIL                 |
| 0x88982f45                       | WINCODEC \_ Err \_ PALETTEUNAVAILABLE               |
| 0x88982f46                       | WINCODEC \_ Err \_ CODECTOOMANYSCANLINES            |
| 0x88982f48                       | WINCODEC \_ Err \_ INTERNALERROR                    |
| 0x88982f49                       | WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS |
| 0x88982f50                       | WINCODEC \_ Err \_ COMPONENTNOTFOUND                |
| 0x88982f51                       | WINCODEC \_ Err \_ IMAGESIZEOUTOFRANGE              |
| 0x88982f52                       | WINCODEC \_ Err \_ TOOMUCHMETADATA                  |
| 0x88982f60                       | WINCODEC \_ Err \_ BADIMAGE                         |
| 0x88982f61                       | WINCODEC \_ Err \_ BADHEADER                        |
| 0x88982f62                       | WINCODEC \_ Err \_ FRAMEMISSING                     |
| 0x88982f63                       | WINCODEC \_ Err \_ BADMETADATAHEADER                |
| 0x88982f70                       | WINCODEC \_ Err \_ BADSTREAMDATA                    |
| 0x88982f71                       | WINCODEC \_ Err \_ STREAMWRITE                      |
| 0x88982f72                       | WINCODEC \_ Err \_ STREAMREAD                       |
| 0x88982f73                       | WINCODEC \_ Err \_ STREAMNOTAVAILABLE               |
| 0x88982f80                       | WINCODEC \_ Err \_ UNSUPPORTEDPIXELFORMAT           |
| 0x88982f81                       | WINCODEC \_ Err \_ UNSUPPORTEDOPERATION             |
| 0x88982f8A                       | WINCODEC \_ Err \_ INVALIDREGISTRATION              |
| 0x88982f8B                       | WINCODEC \_ Err \_ COMPONENTINITIALIZEFAILURE       |
| 0x88982f8C                       | WINCODEC \_ Err \_ INSUFFICIENTBUFFER               |
| 0x88982f8D                       | WINCODEC \_ Err \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f8E                       | WINCODEC \_ Err \_ PROPERTYUNEXPECTEDTYPE           |
| 0x88982f8F                       | WINCODEC \_ Err \_ UNEXPECTEDSIZE                   |
| 0x88982f90                       | WINCODEC \_ Err \_ INVALIDQUERYREQUEST              |
| 0x88982f91                       | WINCODEC \_ Err \_ UNEXPECTEDMETADATATYPE           |
| 0x88982f92                       | WINCODEC \_ Err \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982f93                       | WINCODEC \_ Err \_ INVALIDQUERYCHARACTER            |



 

 

 



