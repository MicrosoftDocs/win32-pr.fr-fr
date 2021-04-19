---
title: Élément TrustedRootCA (ServerValidationParameters)-connexion
description: Capture le curseur de l’impression des autorités de certification racines approuvées par le client. | Élément TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Élément TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106522401"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a>Élément TrustedRootCA (ServerValidationParameters) pour les propriétés de connexion

L’élément **TrustedRootCA (ServerValidationParameters)** capture l’impression Thumb des autorités de certification racines approuvées par le client.

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

L’élément **TrustedRootCA** est défini par le type complexe [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Notes

Le curseur d’impression est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat. L’élément **TrustedRootCA** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Éléments parents immédiats possibles dans l’instance de schéma**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





