---
description: Spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Élément startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2d21381939348ce8c37a9b23abb2283ab209e766bbce452c3802b8c5defe0872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800719"
---
# <a name="startperiod-onex-element"></a>Élément startPeriod (OneX)

L’élément startPeriod (OneX) spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start. Un message de EAPOL-Start est envoyé pour démarrer le processus d’authentification 802.1 X.

Cet élément est facultatif. Quand startPeriod n’est pas spécifié dans un profil, une valeur de 5 secondes est utilisée.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="startPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **startPeriod** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

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

 

 




