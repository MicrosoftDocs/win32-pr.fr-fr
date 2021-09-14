---
description: Contient les informations d’identification d’ouverture de session pour une connexion.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Élément UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415861"
---
# <a name="userlogoncred-contexttype-element"></a>Élément UserLogonCred (contextType)

L’élément **UserLogonCred (ContextType)** contient les informations d’identification d’ouverture de session pour une connexion.

Cet élément peut avoir les éléments enfants suivants.

-   [**Nom d’utilisateur**](schema-username-userlogoncred-element.md)
-   [**Mot de passe**](schema-password-userlogoncred-element.md)
-   [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md)

Cet élément peut avoir au maximum une occurrence.

Cet élément est facultatif.

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **UserLogonCred** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type                                           | Description                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Comment gérer les mots de passe lors de la mise à niveau des profils.<br/> |
| [**De**](schema-password-userlogoncred-element.md)             | string                                         | Mot de passe utilisateur.<br/>                                   |
| [**Nom d’utilisateur**](schema-username-userlogoncred-element.md)             | [**nameType**](schema-nametype-simpletype.md) | Nom d’utilisateur.<br/>                                       |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Contexte (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




