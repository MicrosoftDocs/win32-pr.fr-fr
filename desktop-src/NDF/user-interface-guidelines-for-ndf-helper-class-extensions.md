---
title: Instructions relatives à l’interface utilisateur pour les extensions de classe d’assistance NDF
description: Lors de la création de votre classe d’assistance, vous devrez créer du texte pour aider l’utilisateur à comprendre la cause d’un incident et les étapes de réparation possibles qui peuvent être effectuées.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0094dbee5410d512cfa85f9c227d4b0217f1c507662addb4735023a2ba5833eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801719"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a>Instructions relatives à l’interface utilisateur pour les extensions de classe d’assistance NDF

Lors de la création de votre classe d’assistance, vous devrez créer du texte pour aider l’utilisateur à comprendre la cause d’un incident et les étapes de réparation possibles qui peuvent être effectuées.

## <a name="root-cause-and-repair"></a>Cause racine et réparation

Lorsqu’un incident se produit, une boîte de dialogue s’affiche pour informer l’utilisateur sur ce qui s’est produit. Le texte que vous créez apparaît dans deux zones distinctes.

-   **Cause racine**: brève description de la cause du problème. Contient des informations pour aider un administrateur ou un utilisateur expérimenté à résoudre le problème.
-   **Réparation**: se développe à la cause racine pour fournir plus de détails sur les étapes qu’un utilisateur peut effectuer, sans trop dépasser.

Chaque cause racine ou réparation doit avoir un titre et une description. Tout le texte avant le premier \\ caractère « n » sera utilisé pour le titre. Tout le texte qui suit le premier \\ caractère « n » (y compris les sauts de ligne suivants) sera utilisé pour la description.

## <a name="title-guidelines"></a>Directives relatives aux titres

Le titre d’une cause racine ou d’une réparation doit suivre les instructions suivantes :

-   Doit avoir 128 caractères au maximum. (40 caractères ou moins est recommandé.)
-   Ne doit pas se terminer par un point.

## <a name="description-guidelines"></a>Instructions de description

La description d’une cause racine ou d’une réparation doit suivre les instructions suivantes :

-   Doit avoir 512 caractères au maximum.
-   Chaque phrase doit se terminer par un point.
-   Le \\ caractère « n » peut être utilisé pour créer un saut de ligne dans la description.

 

 




