---
description: Pour déterminer si un compteur est installé sur un ordinateur particulier, appelez PdhValidatePath avec le chemin d’accès complet du compteur. La fonction retourne une erreur \_ de réussite si le compteur se trouve sur l’ordinateur spécifié.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Détermination de l’emplacement d’un compteur sur un ordinateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2cc6672125f961fc2759d264caa6c33ab68f46347c915e82d1666f667692fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061197"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Détermination de l’emplacement d’un compteur sur un ordinateur

Pour déterminer si un compteur est installé sur un ordinateur particulier, appelez [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) avec le chemin d’accès complet du compteur. La fonction retourne une erreur \_ de réussite si le compteur se trouve sur l’ordinateur spécifié.

[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) valide le chemin d’accès entier ; par conséquent, si un objet, une instance ou un compteur du chemin d’accès n’existe pas, la valeur de retour le indique. **PdhValidatePath** vérifie le chemin d’accès au compteur spécifié dans cet ordre : ordinateur, objet de performance, instance et compteur.

 

 



