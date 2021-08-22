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
ms.openlocfilehash: 95efe3f07e86056cd0364daaed1e6a9c0ef402afc18b14d74cca313c9835479f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936284"
---
# <a name="performing-selection-and-feedback"></a>Sélection et commentaires

La sélection, les commentaires et le rendu sont des modes d’opération qui s’excluent mutuellement. Le rendu est le mode par défaut normal pendant lequel les fragments sont produits par pixellisation.

En mode de sélection et de commentaires, aucun fragment n’est produit. par conséquent, aucune modification de trame ne se produit. En mode de sélection, vous pouvez déterminer les primitives qui seront dessinées dans une région d’une fenêtre. en mode commentaires, les informations sur les primitives qui seront pixellisées sont renvoyées à l’application.

Vous pouvez choisir parmi ces trois modes avec [**glRenderMode**](glrendermode.md).

-   [Sélection](selection.md)
-   [Commentaires](feedback.md)
-   [Référence de sélection et de commentaires](selection-and-feedback-reference.md)

 

 




