---
description: Spécifie la façon dont les étiquettes de la propriété sont affichées.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d2d358270bfdf231f990feee54d90f6f39f16fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220580"
---
# <a name="labelinfo"></a>labelInfo

Spécifie la façon dont les étiquettes de la propriété sont affichées. Il ne doit y avoir qu’un seul élément [labelInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [labelInfo]() n’est fourni, l’étiquette de la propriété n’est pas affichée ; Toutefois, il s’agit généralement d’un défaut.

## <a name="syntax"></a>Syntaxe


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | None           |



 

## <a name="attributes"></a>Attributs




| Attribut | Description | 
|-----------|-------------|
| label | Public. Optionnel. Étiquette telle qu’elle s’affiche dans l’interface utilisateur (par exemple, l’étiquette de la colonne Détails ou le volet de visualisation). La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte. Utilisez la chaîne d’affichage indirecte, car elle peut être localisée. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription :: GetDisplayName</strong></a> retourne le nom complet résolu. | 
| sortDescription | Optionnel. Spécifie les chaînes proposées en tant qu’options de tri. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription :: GetSortDescription</strong></a> retourne cette description de tri. Les valeurs suivantes fournissent les chaînes d’interface utilisateur correspondantes.<ul><li>Général : « tri en cours »/« tri en cours »</li><li>AToZ : « A en haut »/« Z en haut »</li><li>LowestHighest : « la plus petite en haut »/« la plus élevée en haut »</li><li>OldestNewest : « le plus ancien en haut »/« plus récent en haut »</li><li>SmallestLargest : « plus petit en haut »/« plus grand en haut »</li></ul> | 
| invitationText | Optionnel. Texte de la chaîne d’aide affiché en tant qu’instruction à l’utilisateur pour le contrôle ou l’info-bulle (par exemple, « entrer le nom de l’auteur. »). La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte. Utilisez la chaîne d’affichage indirecte, car elle peut être localisée. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription :: GetEditInvitation</strong></a> retourne le texte d’invitation résolu. | 
| hideLabel | Optionnel. La valeur par défaut est « false ». Indique si l’étiquette est masquée. | 




 

 

 
