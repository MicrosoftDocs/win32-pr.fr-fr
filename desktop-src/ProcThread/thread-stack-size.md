---
description: Chaque nouveau thread ou fibre reçoit son propre espace de pile constitué de la mémoire réservée et de la mémoire initialement validée.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Taille de la pile des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff392577d529ab03a3859a0c6b0a94057ff8d8e0dc3c09fef86176d5c8950ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031409"
---
# <a name="thread-stack-size"></a>Taille de la pile des threads

Chaque nouveau thread ou fibre reçoit son propre espace de pile constitué de la mémoire réservée et de la mémoire initialement validée. La taille de mémoire réservée représente le nombre total d’allocations de piles dans la mémoire virtuelle. Par conséquent, la taille réservée est limitée à la plage d’adresses virtuelles. Les pages initialement validées n’utilisent pas de mémoire physique tant qu’elles ne sont pas référencées ; Toutefois, ils suppriment les pages de la limite de validation totale du système, qui est la taille du fichier d’échange et la taille de la mémoire physique. Le système valide les pages supplémentaires à partir de la mémoire réservée de la pile lorsqu’elles sont nécessaires, jusqu’à ce que la pile atteigne la taille réservée moins une page (qui est utilisée comme page de garde pour empêcher le dépassement de capacité de la pile) ou que le système manque de mémoire en cas d’échec de l’opération.

Il est préférable de choisir une taille de pile aussi petite que possible et de valider la pile nécessaire au thread ou à la fibre pour s’exécuter de manière fiable. Chaque page réservée pour la pile ne peut pas être utilisée à d’autres fins.

Une pile est libérée lorsque son thread se termine. Elle n’est pas libérée si le thread est arrêté par un autre thread.

La taille par défaut de la mémoire de pile réservée et initialement validée est spécifiée dans l’en-tête du fichier exécutable. La création d’un thread ou d’une fibre échoue s’il n’y a pas assez de mémoire pour réserver ou valider le nombre d’octets demandés. La taille de réservation de pile par défaut utilisée par l’éditeur de liens est de 1 Mo. Pour spécifier une autre taille de réservation de pile par défaut pour tous les threads et les fibres, utilisez l’instruction STACKSIZE dans le fichier de définition de module (. def). Le système d’exploitation arrondit la taille spécifiée au multiple le plus proche de la granularité d’allocation du système (en général 64 Ko). Pour récupérer la granularité d’allocation du système actuel, utilisez la fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Pour modifier l’espace de pile initialement validé, utilisez le paramètre *dwStackSize* de la fonction [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)ou [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) . Cette valeur est arrondie à la page la plus proche. En règle générale, la taille de réserve correspond à la taille de réserve par défaut spécifiée dans l’en-tête de l’exécutable. Toutefois, si la taille initialement validée spécifiée par *dwStackSize* est supérieure ou égale à la taille de réserve par défaut, la taille de réserve est cette nouvelle taille de validation arrondie au multiple le plus proche de 1 Mo.

Pour modifier la taille de pile réservée, définissez le paramètre *dwCreationFlags* de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) sur Stack \_ size \_ param \_ est \_ une \_ réservation et utilisez le paramètre *dwStackSize* . Dans ce cas, la taille initialement validée est la taille par défaut spécifiée dans l’en-tête de l’exécutable. Pour les fibres, utilisez le paramètre *dwStackReserveSize* de [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex). La taille validée est spécifiée dans le paramètre *dwStackCommitSize* .

La fonction [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) définit la taille minimale de la pile associée au thread appelant ou à la fibre qui sera disponible pendant les exceptions de dépassement de capacité de la pile.

 

 
