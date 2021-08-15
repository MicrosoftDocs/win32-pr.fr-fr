---
title: Élément Password (EapType)
description: En savoir plus sur l’élément Password (EapType). Cet élément identifie le mot de passe de l’utilisateur ou de l’ordinateur en cours d’authentification.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Élément Password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbbcb7b0acd372bbe71ee6d22f44a736948b145378f62f40820e3de53d77b875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273198"
---
# <a name="password-eaptype-element"></a>Élément Password (EapType)

L’élément **Password (EapType)** identifie le mot de passe de l’utilisateur ou de l’ordinateur en cours d’authentification.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

L’élément **Password** est défini par l’élément [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

Si l’élément **Password (EapType)** n’est pas présent, le hachage de mot de passe est obtenu à partir de Winlogon. Cet élément est facultatif.

## <a name="requirements"></a>Configuration requise



| Rôle | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 





