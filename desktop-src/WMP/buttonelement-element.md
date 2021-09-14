---
title: Élément BUTTONELEMENT
description: Élément BUTTONELEMENT
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- habillages Lecteur Windows Media, élément BUTTONELEMENT
- Skins, BUTTONELEMENT, élément
- Élément BUTTONELEMENT
- référence pour les habillages, élément BUTTONELEMENT
- éléments, BUTTONELEMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855687"
---
# <a name="buttonelement-element"></a>Élément BUTTONELEMENT

L’élément **BUTTONELEMENT** définit un bouton unique dans un élément **BUTTONGROUP** parent. Il prend en charge les attributs suivants. Les éléments **BUTTONELEMENT** prédéfinis sont également fournis pour des raisons pratiques.

L’élément **BUTTONELEMENT** prend en charge les attributs suivants.



| Attribut                                      | Description                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](buttonelement-cursor.md)             | Spécifie ou récupère la valeur du curseur **BUTTONELEMENT** qui apparaît lorsque la souris se trouve sur le **BUTTONELEMENT**.                                                                                      |
| [baisse](buttonelement-down.md)                 | Spécifie ou récupère la valeur vers le haut ou vers le haut du **BUTTONELEMENT**.                                                                                                                                            |
| [downToolTip](buttonelement-downtooltip.md)   | Spécifie ou récupère le texte info-bulle qui apparaît lorsque la souris se trouve sur le **ButtonElement** et que le **ButtonElement** est à l’état inactif.                                                                |
| [index](buttonelement-index.md)               | Récupère l’index du **BUTTONELEMENT** dans le **BUTTONGROUP**.                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | Spécifie ou récupère la clé de couleur qui identifie ce **BUTTONELEMENT** dans le groupe **ButtonElement** .                                                                                                      |
| [pense-bête](buttonelement-sticky.md)             | Spécifie ou récupère une valeur indiquant si le **BUTTONELEMENT** est rémanent. Lorsqu’il est collant, un **BUTTONELEMENT** change d’État après un clic et reste dans le nouvel État jusqu’à ce que l’utilisateur clique à nouveau dessus. |
| [Info-bulle](buttonelement-uptooltip.md)       | Spécifie ou récupère le texte info-bulle qui apparaît lorsque la souris se trouve sur le **ButtonElement** et que le **ButtonElement** est à l’état actif ou actif.                                                        |



 

L’élément **BUTTONELEMENT** prend en charge la méthode suivante.



| Méthode                           | Description                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [Cliquez sur](buttonelement-click.md) | Appelle le gestionnaire d’événements **OnClick** défini pour **BUTTONELEMENT**. |



 

L’élément **BUTTONELEMENT** peut implémenter les gestionnaires d’événements ambiants. Pour plus d’informations, consultez [gestionnaires d’événements ambiants](ambient-event-handlers.md).

L’élément **BUTTONELEMENT** prend en charge les attributs ambiants suivants : [Enabled](ambientattributes-enabled.md) et [tabStop](ambientattributes-tabstop.md).

Les effets prédéfinis sont des éléments d' **effet** normal avec différents paramètres d’attribut communs spécifiés par défaut. Les éléments **BUTTONELEMENT** prédéfinis suivants sont disponibles.



| BUTTONELEMENT prédéfini         | Description                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [FFWDELEMENT](ffwdelement.md)   | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. fastForward**. |
| [NEXTELEMENT](nextelement.md)   | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. Next**.        |
| [PAUSEELEMENT](pauseelement.md) | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. pause**.       |
| [PLAYELEMENT](playerelement.md) | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. Play**.        |
| [PREVELEMENT](prevelement.md)   | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. Previous**.    |
| [REWELEMENT](rewelement.md)     | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. rembobiner**.      |
| [STOPELEMENT](stopelement.md)   | **BUTTONELEMENT** avec un gestionnaire d’événements **OnClick** intégré qui appelle **Player. Controls. Stop**.        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




