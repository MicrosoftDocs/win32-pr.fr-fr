---
description: Dans d’autres cas, une opération de lecture ou d’écriture peut être effectuée avec un nombre de caractères inférieur au nombre demandé, même si aucun délai d’attente n’a été dépassé.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Erreurs de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114473"
---
# <a name="communications-errors"></a>Erreurs de communication

Dans d’autres cas, une opération de lecture ou d’écriture peut être effectuée avec un nombre de caractères inférieur au nombre demandé, même si aucun délai d’attente n’a été dépassé. En voici quelques exemples :

-   Certains pilotes prennent en charge l’utilisation de caractères spéciaux, qui effectuent immédiatement une opération de lecture avec uniquement les caractères qui ont été lus jusqu’au moment où ils sont reçus.
-   La fonction [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) peut être appelée pour terminer prématurément les opérations de lecture ou d’écriture en attente. Cette fonction peut également supprimer le contenu des mémoires tampons de sortie ou d’entrée, ou les deux.
-   Si une erreur de communication se produit pendant une opération de lecture ou d’écriture, toutes les opérations d’e/s sur la ressource de communication sont arrêtées. Les conditions d’arrêt, les erreurs de parité ou les erreurs de trame sont des exemples de telles erreurs. Lorsqu’une erreur se produit, le processus doit appeler la fonction [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) pour effacer l’indicateur d’erreur avant de pouvoir commencer des opérations d’e/s supplémentaires. **ClearCommError** signale l’erreur spécifique qui s’est produite et l’état actuel de l’appareil.

 

 



