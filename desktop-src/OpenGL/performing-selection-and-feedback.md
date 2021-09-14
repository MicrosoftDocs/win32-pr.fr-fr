---
title: Sélection et commentaires
description: Sélection et commentaires
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, sélection
- OpenGL, commentaires
- OpenGL, rendu
- mode de sélection OpenGL
- mode Commentaires OpenGL
- mode de rendu OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096569"
---
# <a name="performing-selection-and-feedback"></a>Sélection et commentaires

La sélection, les commentaires et le rendu sont des modes d’opération qui s’excluent mutuellement. Le rendu est le mode par défaut normal pendant lequel les fragments sont produits par pixellisation.

En mode de sélection et de commentaires, aucun fragment n’est produit. par conséquent, aucune modification de trame ne se produit. En mode de sélection, vous pouvez déterminer les primitives qui seront dessinées dans une région d’une fenêtre. en mode commentaires, les informations sur les primitives qui seront pixellisées sont renvoyées à l’application.

Vous pouvez choisir parmi ces trois modes avec [**glRenderMode**](glrendermode.md).

-   [Sélection](selection.md)
-   [Commentaires](feedback.md)
-   [Référence de sélection et de commentaires](selection-and-feedback-reference.md)

 

 




