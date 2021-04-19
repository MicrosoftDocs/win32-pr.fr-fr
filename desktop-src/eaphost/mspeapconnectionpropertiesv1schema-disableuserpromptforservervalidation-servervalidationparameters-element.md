---
title: Élément DisableUserPromptForServerValidation (PEAP)
description: En savoir plus sur l’élément DisableUserPromptForServerValidation (ServerValidationParameters). Elle indique si la validation du serveur doit être demandée à l’utilisateur. | Élément DisableUserPromptForServerValidation (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524813"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a>DisableUserPromptForServerValidation (ServerValidationParameters), élément (PEAP)

L’élément **DisableUserPromptForServerValidation (ServerValidationParameters)** indique si la validation du serveur doit être demandée à l’utilisateur.

Si **DisableUserPromptForServerValidation** a la valeur true, EAP-TLS effectue la validation du serveur sans entrée d’utilisateur ; Si la validation échoue, l’authentification EAP-TLS échoue. Si **DisableUserPromptForServerValidation** a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine.

L’élément **DisableUserPromptForServerValidation** est facultatif.

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

L’élément **DisableUserPromptForServerValidation** est défini par le type complexe [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Éléments parents immédiats possibles dans l’instance de schéma**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





