---
title: Élément LogonDomain (EapType)
description: En savoir plus sur l’élément LogonDomain (EapType). Cet élément identifie le domaine de l’utilisateur ou de l’ordinateur en cours d’authentification.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Élément LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031844"
---
# <a name="logondomain-eaptype-element"></a>Élément LogonDomain (EapType)

L’élément **LogonDomain (EapType)** identifie le domaine de l’utilisateur ou de l’ordinateur en cours d’authentification.

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

L’élément **LogonDomain** est défini par l’élément [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

Si l’élément **LogonDomain (EapType)** n’est pas présent, le domaine de Winlogon est utilisé. Cet élément est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





