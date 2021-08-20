---
description: les mises à jour qui nécessitent une intervention de l’utilisateur ne peuvent pas être installées par Windows Update les applications de l’Agent (wua) si les applications wua s’exécutent dans le contexte du service d’ouverture de session secondaire.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Utilisation de WUA à partir d’un processus d’ouverture de session secondaire (exécuter en tant que)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a659b9c46429100393138751039fdc1ce529191970a35c76d36e45bb16eb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049087"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Utilisation de WUA à partir d’un processus d’ouverture de session secondaire (exécuter en tant que)

les mises à jour qui nécessitent une intervention de l’utilisateur ne peuvent pas être installées par Windows Update les applications de l’Agent (wua) si les applications wua s’exécutent dans le contexte du service d’ouverture de session secondaire.

Si le processus qui appelle WUA s’exécute dans le contexte du service RunAs ou du service d’ouverture de session secondaire, une tentative d’installation d’une mise à jour nécessitant une interaction avec l’utilisateur échoue et renvoie l’erreur de l' **\_ utilisateur Wu E \_ no \_ interactive \_** .

dans Microsoft Windows, vous pouvez exécuter des programmes en tant qu’utilisateur qui diffère de l’utilisateur actuellement connecté. Pour ce faire, le service d’ouverture de session secondaire doit être en cours d’exécution.

 

 



