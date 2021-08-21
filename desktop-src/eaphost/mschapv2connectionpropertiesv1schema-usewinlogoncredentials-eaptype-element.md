---
title: Élément UseWinLogonCredentials (EapType)
description: En savoir plus sur l’élément UseWinLogonCredentials (EapType). Cet élément contrôle l’utilisation des informations d’identification winlogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Élément UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a407c505139562a155e5aa9d7ed57fed5d15077cf5d035ea8bb7bbe0e177363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086190"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Élément UseWinLogonCredentials (EapType)

L’élément **UseWinLogonCredentials (EapType)** contrôle l’utilisation des informations d’identification winlogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

L’élément **UseWinLogonCredentials** est défini par l’élément [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarques

Si la valeur est TRUE, EAP MS-CHAPv2 obtient les informations d’identification de Winlogon. Si la valeur est FALSe, EAP MS-CHAPv2 obtient les informations d’identification de l’utilisateur. L’élément **UseWinLogonCredentials (EapType)** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Versions de système d’exploitation minimales prises en charge |
|------|-------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





