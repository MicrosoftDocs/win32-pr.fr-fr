---
description: La prise en charge des pages de grande taille permet aux applications serveur d’établir des régions de mémoire de grande page, ce qui est particulièrement utile sur les Windowss de 64 bits.
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Support Large-Page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad61873c80d2d3fe8de6a915f5eb93f527049a437860deabedbe232cdf9cb885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869679"
---
# <a name="large-page-support"></a>Support Large-Page

La prise en charge des pages de grande taille permet aux applications serveur d’établir des régions de mémoire de grande page, ce qui est particulièrement utile sur les Windowss de 64 bits. Chaque traduction de grande page utilise un seul tampon de traduction à l’intérieur de l’UC. La taille de cette mémoire tampon est généralement de trois ordres de grandeur supérieurs à la taille de page native. Cela augmente l’efficacité de la mémoire tampon de traduction, ce qui peut améliorer les performances de la mémoire fréquemment utilisée.

La procédure suivante décrit comment utiliser la prise en charge des pages de grande taille.

**Pour utiliser la prise en charge des pages de grande taille**

1.  Obtenez le privilège **SeLockMemoryPrivilege** en appelant la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) . Pour plus d’informations, consultez [attribution de privilèges à un compte](../secbp/assigning-privileges-to-an-account.md) et [modification des privilèges dans un jeton](../secbp/changing-privileges-in-a-token.md).
2.  Récupérez la taille de page minimale minimale en appelant la fonction [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) .
3.  Incluez la valeur **MEM \_ large \_ pages** lors de l’appel de la fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) . La taille et l’alignement doivent être un multiple du nombre minimal de pages de grande taille.

Lorsque vous écrivez des applications qui utilisent de la mémoire de pages de grande taille, gardez à l’esprit les considérations suivantes :

-   Les régions de mémoire de pages de grande taille peuvent être difficiles à obtenir après l’exécution du système pendant une longue période, car l’espace physique pour chaque page volumineuse doit être contigu, mais la mémoire peut être fragmentée. L’allocation de pages de grande taille dans ces conditions peut avoir un impact significatif sur les performances du système. Par conséquent, les applications doivent éviter d’allouer des allocations de pages de grande taille et d’allouer à la place toutes les grandes pages une fois au démarrage.
-   La mémoire est toujours en lecture/écriture et non paginable (toujours résident dans la mémoire physique).
-   La mémoire fait partie des octets privés du processus, mais ne fait pas partie de la plage de travail, car la plage de travail de la définition contient uniquement de la mémoire paginable.
-   Les allocations de pages de grande taille ne sont pas soumises aux limites du travail.
-   La mémoire de pages volumineuses doit être réservée et validée en tant qu’opération unique. En d’autres termes, les pages de grande taille ne peuvent pas être utilisées pour valider une plage de mémoire précédemment réservée.
-   WOW64 sur les systèmes Intel Itanium ne prend pas en charge les applications 32 bits qui utilisent cette fonctionnalité. Les applications doivent être recompilées en tant qu’applications 64 bits natives.

 

 
