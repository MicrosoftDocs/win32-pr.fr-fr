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
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118098"
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

## <a name="requirements"></a>Spécifications



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

 

 




