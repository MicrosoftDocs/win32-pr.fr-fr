---
title: Élément d’auteur d’EapMethodType
description: En savoir plus sur l’élément de reEapMethodTypement. L’élément de réutilisation (EapMethodType) fait référence à l’auteur de la méthode.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Élément d’auteur EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f15c5fc981592bb82f9ad52d590f12ac0b1f4b20af3537a511d01dd0a8cc15e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021749"
---
# <a name="authorid-eapmethodtype-element"></a>Élément d’auteur d’EapMethodType

L’élément de réutilisation **(EapMethodType)** fait référence à l’auteur de la méthode.

L’identificateur d’auteur est un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

L’élément d’un élément d' **auteur** est défini par le type complexe [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Remarques

Il n’est pas **nécessaire que les** éléments de réfaut de réfaut et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de données soient identiques pour une méthode particulière.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





