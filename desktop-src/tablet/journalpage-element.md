---
description: Contient les détails relatifs à une page individuelle dans une note du journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Élément JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866774"
---
# <a name="journalpage-element"></a>Élément JournalPage

Contient les détails relatifs à une page individuelle dans une note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>Éléments enfants

[**Stationnaire**](stationery-element.md)

[**DocImage**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**Content**](content-element--journal-reader.md)

## <a name="attributes"></a>Attributs



| Attribut      | Type                      | Obligatoire | Description                                                                        | Valeurs possibles                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Nombre**     | **xs:nonNegativeInteger** | Obligatoire | Numéro ordinal de la page dans le document Journal, commençant par un (1). | Entier non négatif.                                |
| **Width**      | **xs:nonNegativeInteger** | Obligatoire | Largeur de la page.                                                             | Entier non négatif.                                |
| **Height**     | **xs:nonNegativeInteger** | Obligatoire | Hauteur de la page.                                                            | Entier non négatif.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Facultatif | Hauteur de la ligne utilisée sur la page.                                           | Entier non négatif.                                |
| **LanguageId** | **xs:nonNegativeInteger** | Facultatif | ID de langue utilisé pour la page.                                                 | Entier non négatif représentant un ID de langue valide. |



 

## <a name="element-information"></a>Informations sur les éléments



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| Type d'élément | ComplexType [**JournalPageType**](journalpagetype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                          |
| Nom du schéma  | Lecteur de journal                                                      |



 

 

 



