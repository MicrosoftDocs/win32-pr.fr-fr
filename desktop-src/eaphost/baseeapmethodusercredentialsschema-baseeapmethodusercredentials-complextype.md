---
title: Type complexe BaseEapMethodUserCredentials
description: En savoir plus sur le type complexe BaseEapMethodUserCredentials. Ce type est un élément d’espace réservé pour les données d’informations d’identification de méthode.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8102f095ca7d4b1ada6db3c21fbe55e73a98ed6d06d2d6b99032f1a21a344527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094419"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Type complexe BaseEapMethodUserCredentials

Le type complexe **BaseEapMethodUserCredentials** est un élément d’espace réservé pour les données d’informations d’identification de méthode.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Remarques

La méthode EAP effectue une validation de schéma sur le contenu de **BaseEapMethodUserCredentials**.

## <a name="requirements"></a>Configuration requise



| Fonction | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





