---
description: Spécifie si les informations d’identification de l’utilisateur sont mises en cache pour les connexions suivantes.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Élément cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f4663153fa9aff176180387ebaf0321ab3d48ec2c382e9e84c0f524d6e0ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800869"
---
# <a name="cacheuserdata-onex-element"></a>Élément cacheUserData (OneX)

L’élément cacheUserData (OneX) spécifie si les informations d’identification de l’utilisateur sont mises en cache pour les connexions suivantes. Quand cacheUserData a la valeur TRUE, les informations d’identification sont mises en cache. Quand cacheUserData a la valeur FALSe, les informations d’identification ne sont pas mises en cache et l’utilisateur peut être invité à entrer des informations d’identification lors des tentatives de connexion suivantes.

Cet élément est facultatif. Quand cacheUserData n’est pas spécifié dans un profil, les informations d’identification de l’utilisateur sont mises en cache.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

L’élément **cacheUserData** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 




