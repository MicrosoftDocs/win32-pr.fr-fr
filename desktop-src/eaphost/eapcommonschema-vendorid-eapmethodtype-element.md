---
title: Élément ID de l’élément (EapMethodType)
description: Fait référence au fournisseur qui a défini la méthode si l’élément de type (EapMethodType) est 254 (méthode EAP développée).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Élément ID de l’élément EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508650"
---
# <a name="vendorid-eapmethodtype-element"></a>Élément ID de l’élément (EapMethodType)

L’élément **ID de fournisseur (EapMethodType)** fait référence au fournisseur qui a défini la méthode si l’élément de [**type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) est 254 (méthode EAP développée).

Le **ID** de l’argument est facultatif. S’il est utilisé, le **ID** de certificat est un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

L’élément **ID** de type est défini par le type complexe [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Notes

Il n’est pas [**nécessaire que les**](eapcommonschema-authorid-eapmethodtype-element.md) éléments de réfaut de réfaut et **ID** de données soient identiques pour une méthode particulière.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



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

 

 





