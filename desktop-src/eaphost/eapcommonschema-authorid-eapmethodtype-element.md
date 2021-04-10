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
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941374"
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

## <a name="remarks"></a>Notes

Il n’est pas **nécessaire que les** éléments de réfaut de réfaut et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de données soient identiques pour une méthode particulière.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 





