---
title: Annexe B prise en charge du gestionnaire de boîtes de dialogue standard
description: Microsoft Active Accessibility fournit une prise en charge complète des contrôles de boîte de dialogue du gestionnaire de boîtes de dialogue standard (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b6500cabf4820fffe12b7ef160f2e494e43db067f6b96409dee02bbfd6119e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326819"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Annexe B : prise en charge du gestionnaire de boîtes de dialogue standard

Microsoft Active Accessibility fournit une prise en charge complète des contrôles de boîte de dialogue du gestionnaire de boîtes de dialogue standard (SDM). le SDM est une bibliothèque de code interne microsoft qui fournit aux applications microsoft un degré d’indépendance par rapport aux différences entre les systèmes d’exploitation Macintosh et Microsoft Windows. le SDM est principalement utilisé pour les boîtes de dialogue dans Microsoft Excel et Microsoft Word.

Le SDM présente des problèmes pour les aides à l’accessibilité, car il utilise des implémentations non standard de boîtes de dialogue. Par exemple, les boutons de la boîte de dialogue SDM n’utilisent pas les handles de fenêtre de la même façon que les éléments d’interface utilisateur standard. Vous ne pouvez pas envoyer de messages à des boutons et les boutons ne sont pas contenus dans la liste des fenêtres. Une application utilisant le SDM communique avec le contrôle par le biais d’une interface privée.

L’illustration suivante montre un exemple de boîte de dialogue à partir de Word. bien qu’il ressemble à une boîte de dialogue de Windows normale qui utilise le contrôle onglet, il s’agit en réalité d’une boîte de dialogue SDM.

![capture d’écran de la boîte de dialogue Options avec l’onglet Affichage sélectionné](images/dialog.gif)

 

 




