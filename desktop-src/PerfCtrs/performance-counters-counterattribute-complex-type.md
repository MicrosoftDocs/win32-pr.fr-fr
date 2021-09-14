---
description: Définit un attribut d’un compteur qui spécifie le mode d’affichage des données de compteur dans une application consommateur.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: Type complexe counterAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218489"
---
# <a name="counterattribute-complex-type"></a>Type complexe counterAttribute

Définit un attribut d’un compteur qui spécifie le mode d’affichage des données de compteur dans une application consommateur.

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom | Type | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name |      | Nom de l’attribut d’affichage à appliquer. Vous pouvez spécifier l’un des noms suivants :<br/> <dl> <dt><span id="reference"></span><span id="REFERENCE"></span>faire</dt> <dd> Récupérez la valeur du compteur par référence et non par valeur.<br/> </dd> <dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>nodisplay</dt> <dd> N’affiche pas la valeur de compteur. En général, vous utilisez cet attribut si les données du compteur sont utilisées comme entrée pour calculer la valeur d’un autre compteur. <br/> </dd> <dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt> <dd> Les applications de consommateur ou de surveillance ne doivent pas utiliser de séparateurs de chiffres lors de l’affichage des valeurs de compteur. <br/> </dd> <dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt> <dd> Les applications de consommateur ou de surveillance doivent afficher la valeur de compteur en tant que valeur hexadécimale, au lieu de la valeur entière par défaut.<br/> </dd> <dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt> <dd> Les applications de consommateur ou de surveillance doivent afficher la valeur de compteur sous la forme d’un nombre réel, au lieu de la valeur entière par défaut. <br/> </dd> </dl> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




