---
description: Représente un handle vers une réponse OCSP associée à une chaîne de certificat de serveur.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233358"
---
# <a name="hcert_server_ocsp_response"></a>\_ \_ réponse OCSP du serveur HCERT \_

Le type de données de **\_ \_ \_ réponse OCSP du serveur HCERT** représente un handle vers une réponse OCSP associée à une chaîne de certificat de serveur.

Ce type est utilisé par les API suivantes.

-   [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [**CertGetServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 




