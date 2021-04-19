---
description: Comme mentionné dans la vue d’ensemble de l’identificateur de session, un descripteur d’appel est le moyen par lequel une application TAPI 2,2 identifie une session de communication particulière.
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: Handles d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacad5b73d9d22caa006b734acaf8b992203d7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516702"
---
# <a name="call-handles"></a>Handles d’appel

Comme mentionné dans la vue d’ensemble de l' [identificateur de session](./session-identifier-ovr.md) , un descripteur d’appel est le moyen par lequel une application TAPI 2,2 identifie une session de communication particulière. Quand une application initie une session, TAPI retourne un handle d’appel à utiliser dans d’autres opérations ou requêtes. Lorsqu’une application est avertie d’une session entrante, l’interface TAPI transmet également un handle d’appel.

Une fois qu’une session est terminée et que l’état de session est inactif, le descripteur d’appel reste valide jusqu’à ce que l’application libère le descripteur ou que la ligne soit fermée. La ligne peut être fermée par l’application ou un message de fermeture de [**ligne \_**](line-close.md) peut s’afficher. Si une ligne est fermée, tous les descripteurs d’appel des appels sur la ligne deviennent instantanément non valides.

Lorsqu’un appel revient à l’état *inactif* , l’application est toujours autorisée à lire la structure et l’état des informations de l’appel. Cela permet aux applications d’utiliser des opérations telles que [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) pour récupérer des informations d’appel à des fins de journalisation.

Lorsque l’application ne peut plus utiliser le handle d’un appel inactif, elle doit appeler [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) pour libérer de la mémoire allouée par le système liée à l’appel. L’interface TAPI alloue de la mémoire pour chaque appel de chaque application ayant un handle vers l’appel. Il est probable que les fournisseurs de services allouent de la mémoire pour stocker également les informations sur les appels. La désallocation du descripteur d’appel d’une application permet à la bibliothèque et au fournisseur de services de récupérer ces ressources mémoire. Le descripteur d’une application pour un appel devient void après une désallocation réussie.

L’application doit lui-même libérer de la mémoire en rapport avec l’appel qu’elle a alloué pour ses propres besoins.

 

 
