---
title: DisableUserPromptForServerValidation (ServerValidationParameters)
description: En savoir plus sur l’élément DisableUserPromptForServerValidation (ServerValidationParameters). Elle indique si la validation du serveur doit être demandée à l’utilisateur. | DisableUserPromptForServerValidation (ServerValidationParameters)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Élément DisableUserPromptForServerValidation EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37f412f9c6200e7d2a54d624d0a77b4df5316ea7edd0ab75b69f92c753abbcff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273717"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a>DisableUserPromptForServerValidation (ServerValidationParameters), élément (TLS)

L’élément **DisableUserPromptForServerValidation (ServerValidationParameters)** indique si la validation du serveur doit être demandée à l’utilisateur.

Si **DisableUserPromptForServerValidation** a la valeur true, EAP-TLS effectue la validation du serveur sans entrée d’utilisateur ; Si la validation échoue, l’authentification EAP-TLS échoue. Si **DisableUserPromptForServerValidation** a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine.

L’élément **DisableUserPromptForServerValidation** est facultatif.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

L’élément **DisableUserPromptForServerValidation** est défini par le type complexe [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Rôle | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





