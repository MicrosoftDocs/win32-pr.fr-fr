---
description: Élément de niveau supérieur dans un fichier de note XML de journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Élément JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523156"
---
# <a name="journaldocument-element"></a>Élément JournalDocument

Élément de niveau supérieur dans un fichier de note XML de journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>Éléments parents

Aucun.

## <a name="child-elements"></a>Éléments enfants

[**Stationery**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>Attributs



| Attribut             | Type                      | Obligatoire | Description                                                      | Valeurs possibles           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Version**           | **xs:string**             | Obligatoire | Version du document journal représenté dans le fichier XML. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Obligatoire | Largeur par défaut de la page pour le document journal.          | Entier non négatif. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Obligatoire | Hauteur par défaut de la page pour le document journal.         | Entier non négatif. |



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|--------------------------------------------|
| Type d'élément | **JournalDocument**                        |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk |
| Nom du schéma  | Lecteur de journal                             |



 

 

 



