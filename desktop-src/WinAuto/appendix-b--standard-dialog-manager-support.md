---
title: Annexe B prise en charge du gestionnaire de boîtes de dialogue standard
description: Microsoft Active Accessibility fournit une prise en charge complète des contrôles de boîte de dialogue du gestionnaire de boîtes de dialogue standard (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673445"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Annexe B : prise en charge du gestionnaire de boîtes de dialogue standard

Microsoft Active Accessibility fournit une prise en charge complète des contrôles de boîte de dialogue du gestionnaire de boîtes de dialogue standard (SDM). Le SDM est une bibliothèque de code interne Microsoft qui fournit aux applications Microsoft un degré d’indépendance par rapport aux différences entre les systèmes d’exploitation Macintosh et Microsoft Windows. Le SDM est principalement utilisé pour les boîtes de dialogue dans Microsoft Excel et Microsoft Word.

Le SDM présente des problèmes pour les aides à l’accessibilité, car il utilise des implémentations non standard de boîtes de dialogue. Par exemple, les boutons de la boîte de dialogue SDM n’utilisent pas les handles de fenêtre de la même façon que les éléments d’interface utilisateur standard. Vous ne pouvez pas envoyer de messages à des boutons et les boutons ne sont pas contenus dans la liste des fenêtres. Une application utilisant le SDM communique avec le contrôle par le biais d’une interface privée.

L’illustration suivante montre un exemple de boîte de dialogue à partir de Word. Bien qu’il ressemble à une boîte de dialogue Windows normale qui utilise le contrôle onglet, il s’agit en réalité d’une boîte de dialogue SDM.

![capture d’écran de la boîte de dialogue Options avec l’onglet Affichage sélectionné](images/dialog.gif)

 

 




