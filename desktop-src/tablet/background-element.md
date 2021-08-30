---
description: Contient l’arrière-plan d’un élément JournalDocument ou d’un élément JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Élément d’arrière-plan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3585b8ca37fe86bd1c687601975ea0ad189d5746
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473895"
---
# <a name="background-element"></a>Élément d’arrière-plan

Contient l’arrière-plan d’un élément [**JournalDocument**](journaldocument-element.md) ou d’un élément [**JournalPage**](journalpage-element.md) .

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**Stationery**](stationery-element.md)

## <a name="child-elements"></a>Éléments enfants

[**Image**](image-element.md)

## <a name="attributes"></a>Attributs




| Attribut | Type | Obligatoire | Description | Valeurs possibles | 
|-----------|------|----------|-------------|-----------------|
| <strong>Style</strong> | <strong>xs:string</strong> | Obligatoire | Spécifie le style de l’arrière-plan. | <ul><li>Aucun</li><li>Unie</li></ul> | 
| <strong>Couleur</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType | Facultatif | Spécifie la couleur de l'arrière-plan. | Voir <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType. | 




 

## <a name="element-information"></a>Informations sur les éléments



|                  | Valeur                                                             |
|------------------|-------------------------------------------------------------------|
| **Type d’élément** | ComplexType [**BackgroundType**](backgroundtype-complex-type.md) |
| **Espace de noms**    | urn : schemas-microsoft-com : TabletPC : RichInk                        |
| **Nom du schéma**  | Lecteur de journal                                                    |



 

 

 



