---
description: spécifie la configuration EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Élément EAPConfig (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 539f30d6730ec0735006f9dd3812322468ce71c7b0fbd90610b6cd589e0d60bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684879"
---
# <a name="eapconfig-onex-element"></a>Élément EAPConfig (OneX)

L’élément **EAPConfig** (Onex) spécifie la configuration EAPHost.

Contrairement à la plupart des éléments du schéma de profil 802.1 X, cet élément se trouve dans l' `https://www.microsoft.com/provisioning/EapHostConfig` espace de noms. Ses éléments enfants sont définis dans le [schéma eaphostconfig](../eaphost/eaphostconfigschema-schema.md). L’élément [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) est un enfant de l’élément **EAPConfig** .

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **EAPConfig** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



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

 

 
