---
description: Fonctions de débogage des sections critiques
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Fonctions de débogage des sections critiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65834d84900ad3ac893cb75493a59902629fec15523cfaca8974a6684ba9c409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908069"
---
# <a name="critical-section-debugging-functions"></a>Fonctions de débogage des sections critiques

Ces fonctions permettent de déboguer des sections critiques dans votre code, ce qui peut faciliter la recherche de la cause d’un blocage. Ces fonctions utilisent la classe d’assistance [**CCritSec**](ccritsec.md) .



| Fonction                             | Description                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**CritCheckIn**](critcheckin.md)   | Retourne la **valeur true** si le thread actuel possède la section critique spécifiée.  |
| [**CritCheckOut**](critcheckout.md) | Retourne la **valeur false** si le thread actuel possède la section critique spécifiée. |
| [**DbgLockTrace**](dbglocktrace.md) | Active ou désactive la journalisation du débogage pour une section critique donnée.              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilitaires de débogage](debugging-utilities.md)
</dt> </dl>

 

 



