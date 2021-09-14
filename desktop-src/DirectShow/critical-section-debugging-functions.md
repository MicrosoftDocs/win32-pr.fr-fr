---
description: Fonctions de débogage des sections critiques
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Fonctions de débogage des sections critiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094782"
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

 

 



