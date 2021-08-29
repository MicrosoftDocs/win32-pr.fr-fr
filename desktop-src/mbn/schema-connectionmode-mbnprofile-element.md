---
description: Spécifie le paramètre de connexion automatique à utiliser pour un appareil haut débit mobile.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Élément ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d0f2290928fba4be65d39129017a171fbd3d1e66e6ebab715f616e4edec9b13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607139"
---
# <a name="connectionmode-mbnprofile-element"></a>Élément ConnectionMode (MBNProfile)

L’élément **ConnectionMode (MBNProfile)** spécifie le paramètre de connexion automatique à utiliser pour un appareil haut débit mobile.

Cet élément peut avoir l’une des valeurs suivantes.



| Valeur       | Signification                                                                |
|-------------|------------------------------------------------------------------------|
| opération    | Ne jamais se connecter automatiquement au réseau.                            |
| saisie      | Toujours se connecter automatiquement au réseau.                           |
| « Auto-démarrage » | Se connecter automatiquement au réseau sauf dans un réseau itinérant. |



 

Cet élément peut avoir au maximum une occurrence.

Cet élément est obligatoire.

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **ConnectionMode** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




