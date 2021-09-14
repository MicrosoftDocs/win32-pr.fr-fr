---
description: Contient le contenu d’une page de journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Élément de contenu [lecteur de journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d544aebac1292a81c9a4acd05cb25da80977027e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293323"
---
# <a name="content-element-journal-reader"></a>Lecteur du journal des éléments de contenu \[\]

Contient le contenu d’une page de journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Éléments enfants

[**, Nœud**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Dessin**](drawing-element.md)

[**Financière**](text-element.md)

[**Image**](image-element.md)

[**Indicateur**](flag-element.md)

## <a name="attributes"></a>Attributs




| Attribut | Type | Obligatoire | Description | PossibleValues | 
|-----------|------|----------|-------------|----------------|
| <strong>Type</strong> | <a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a> | Obligatoire | Si le type est « inerte », le contenu ne peut pas être modifié.<br /> | <ul><li>Normal</li><li>Inertes</li></ul> | 




 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-------------------------------------------------------------|
| Type d'élément | ComplexType [**ContentType**](contenttype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                  |
| Nom du schéma  | Lecteur de journal                                              |



 

 

 




