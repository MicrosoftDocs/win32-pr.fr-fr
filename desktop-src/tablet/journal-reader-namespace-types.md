---
description: Cette section documente les types XML utilisés par le composant de lecture du journal.
ms.assetid: 08b45fe0-a505-4cc0-9791-764a87e8f1eb
title: Types d’espaces de noms de lecteur de journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e8e3d812eea879ca9dd31680aa2834d6dfe50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203242"
---
# <a name="journal-reader-namespace-types"></a>Types d’espaces de noms de lecteur de journal

Cette section documente les types XML utilisés par le composant de lecture du journal.

## <a name="in-this-section"></a>Dans cette section



| Type                                                                                  | Description                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComplexType AlternatesListType**](alternateslisttype-complex-type.md)             | Définit le type qui contient la liste des alternatives de reconnaissance pour un mot Ink.<br/>                                                                                                                  |
| [**ComplexType BackgroundImageType**](backgroundimagetype-complex-type.md)           | Définit le type qui contient des informations sur l’image d’arrière-plan utilisée par la note du journal, le cas échéant.<br/>                                                                                                |
| [**ComplexType BackgroundType**](backgroundtype-complex-type.md)                     | Définit le type qui contient les informations générales pour la note du journal.<br/>                                                                                                                     |
| [**ComplexType BaselineType**](baselinetype-complex-type.md)                         | Définit le type qui contient des informations sur la ligne de base d’un paragraphe.<br/>                                                                                                                       |
| [BoundsType attributeGroup](boundstype-attributegroup.md)                            | Définit un groupe d’attributs utilisé par divers éléments dans un fichier journal XML.<br/>                                                                                                             |
| [**ColorType, simpleType**](colortype-simple-type.md)                                 | Définit le type utilisé pour spécifier des valeurs valides pour la couleur de certains éléments dans un fichier journal XML.<br/>                                                                                      |
| [Groupe ContentGroup](contentgroup-group.md)                                          | Définit le type qui contient un jeu de contenu groupé dans une note du journal.<br/>                                                                                                                          |
| [**ComplexType ContentType**](contenttype-complex-type.md)                           | Définit le type qui contient une forme de contenu dans un fichier journal XML.<br/>                                                                                                                      |
| [**SimpleType ContentTypeType**](contenttypetype-simple-type.md)                     | Définit le type qui définit des valeurs valides pour l’attribut de **type** du [ \[ lecteur \] du journal des éléments de contenu](content-element--journal-reader.md).<br/>                                             |
| [**ComplexType DrawingType**](drawingtype-complex-type.md)                           | Définit le type qui contient l’encre qui a été classifiée par le moteur d’analyse du journal en tant qu' [élément de dessin](drawing-element.md) (par opposition à un [élément InkWord](inkword-element.md)).<br/>  |
| [**ComplexType FlagType**](flagtype-complex-type.md)                                 | Définit le type qui contient l’image binaire encodée et les informations de position pour un indicateur incorporé dans un document journal.<br/>                                                                         |
| [**ComplexType GroupNodeType**](groupnodetype-complex-type.md)                       | Définit le type qui contient un jeu de contenu groupé dans une note du journal.<br/>                                                                                                                          |
| [**ComplexType HorizontalType**](horizontaltype-complex-type.md)                     | Définit le type qui contient des informations sur les lignes horizontales utilisées par le papier à lettres dans une note du journal.<br/>                                                                                         |
| [**complexType ImageType**](imagetype-complex-type.md)                               | Définit le type qui contient les informations binaires pour une image dans une note du journal. Consultez également le [**complexType BackgroundImageType**](backgroundimagetype-complex-type.md).<br/>                     |
| [**ComplexType InkWordType**](inkwordtype-complex-type.md)                           | Définit le type qui contient les données d’encre, les alternatives et la confiance pour le contenu d’encre qui est un [élément InkWord](inkword-element.md) (par opposition à un [élément de dessin](drawing-element.md)).<br/> |
| [**ComplexType JournalPageType**](journalpagetype-complex-type.md)                   | Définit le type qui contient une page individuelle dans une note du journal.<br/>                                                                                                                                |
| [**ComplexType LineLayoutType**](linelayouttype-complex-type.md)                     | Définit le type qui contient des informations sur les lignes utilisées dans le papier à lettres d’une note de journal donnée.<br/>                                                                                      |
| [**SimpleType LineLayoutStyleType**](linelayoutstyletype-simple-type.md)             | Définit les valeurs valides pour l’attribut **style** de l' [élément LineLayout](linelayout-element.md).<br/>                                                                                           |
| [**ComplexType LineType**](linetype-complex-type.md)                                 | Définit le type qui contient une ligne de paragraphe.<br/>                                                                                                                                                 |
| [**ComplexType MarginType**](margintype-complex-type.md)                             | Définit le type qui contient les détails sur toutes les marges dans la note du journal, telles que le style, la couleur et la position.<br/>                                                                               |
| [**SimpleType MarginTypeType**](margintypetype-simple-type.md)                       | Définit le type qui contient des valeurs valides pour l’attribut de **type** de l' [élément Margin](margin-element.md).<br/>                                                                                |
| [**ComplexType ParagraphType**](paragraphtype-complex-type.md)                       | Définit le type qui contient un paragraphe dans une note du journal.<br/>                                                                                                                                          |
| [**ComplexType ParagraphLineMetricsType**](paragraphlinemetricstype-complex-type.md) | Définit le type qui contient des informations sur les métriques de ligne d’un paragraphe, telles que la ligne de base.<br/>                                                                                             |
| [**ComplexType ReflowType**](reflowtype-complex-type.md)                             | Définit le type qui indique que le groupe a été redistribué.<br/>                                                                                                                                        |
| [**ComplexType ScalarTransformType**](scalartransformtype-complex-type.md)           | Définit le type qui contient les informations sur les transformations appliquées à l’encre.<br/>                                                                                                                |
| [**ComplexType StationeryType**](stationerytype-complex-type.md)                     | Définit le type qui contient le papier à lettres utilisé par la note du journal.<br/>                                                                                                                             |
| [**ComplexType TextType**](texttype-complex-type.md)                                 | Définit le type qui contient la valeur de texte dans un [ \[ lecteur \] du journal des éléments de contenu](content-element--journal-reader.md).<br/>                                                                       |
| [**ComplexType TitleAreaType**](titleareatype-complex-type.md)                       | Définit le type qui contient les informations relatives à la position et aux limites pour le titre dans une note du journal.<br/>                                                                                                     |
| [**ComplexType TitleInfoType**](titleinfotype-complex-type.md)                       | Définit le type qui contient des informations sur le titre dans une note du journal.<br/>                                                                                                                       |
| [**ComplexType TitleType**](titletype-complex-type.md)                               | Définit le type qui contient les informations de titre pour la note du journal.<br/>                                                                                                                              |
| [**ComplexType VerticalType**](verticaltype-complex-type.md)                         | Définit le type qui contient des détails sur les lignes verticales utilisées dans le papier à lettres d’une note de journal.<br/>                                                                                                |



 

 

 




