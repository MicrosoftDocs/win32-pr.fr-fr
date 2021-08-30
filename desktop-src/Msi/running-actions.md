---
description: Les fonctions du programme d’installation peuvent être utilisées pour exécuter des actions ou des séquences d’action spécifiques.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Actions en cours d’exécution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9e167144a620589bc6f0641d7344a2d31254cd003412e746a41759c1143506
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039649"
---
# <a name="running-actions"></a>Actions en cours d’exécution

Les fonctions du programme d’installation peuvent être utilisées pour exécuter des actions ou des séquences d’action spécifiques. Ces actions peuvent être des actions [standard](standard-actions.md) ou [personnalisées](custom-actions.md) . La procédure suivante décrit comment exécuter des actions :

**Pour exécuter une séquence d’action**

1.  Exécutez une séquence d’actions définie dans une table en appelant la fonction [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .

    Le programme d’installation interroge la table indiquée et exécute chaque action si son expression conditionnelle prend la valeur TRUE.

2.  Vérifiez les expressions conditionnelles en appelant la fonction [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .
3.  Exécutez l’action en appelant la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) . L’action peut être une action standard, une action personnalisée ou une boîte de dialogue d’interface utilisateur.
4.  Si une erreur s’est produite lors de l’exécution de cette action, appelez la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . Le programme d’installation traitera l’erreur.

 

 



