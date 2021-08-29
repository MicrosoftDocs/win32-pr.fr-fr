---
description: Dans d’autres cas, une opération de lecture ou d’écriture peut être effectuée avec un nombre de caractères inférieur au nombre demandé, même si aucun délai d’attente n’a été dépassé.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Erreurs de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e946d5cb97122c35a5ec09978508e86724290307e514576482f535b1f3493418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874589"
---
# <a name="communications-errors"></a>Erreurs de communication

Dans d’autres cas, une opération de lecture ou d’écriture peut être effectuée avec un nombre de caractères inférieur au nombre demandé, même si aucun délai d’attente n’a été dépassé. En voici quelques exemples :

-   Certains pilotes prennent en charge l’utilisation de caractères spéciaux, qui effectuent immédiatement une opération de lecture avec uniquement les caractères qui ont été lus jusqu’au moment où ils sont reçus.
-   La fonction [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) peut être appelée pour terminer prématurément les opérations de lecture ou d’écriture en attente. Cette fonction peut également supprimer le contenu des mémoires tampons de sortie ou d’entrée, ou les deux.
-   Si une erreur de communication se produit pendant une opération de lecture ou d’écriture, toutes les opérations d’e/s sur la ressource de communication sont arrêtées. Les conditions d’arrêt, les erreurs de parité ou les erreurs de trame sont des exemples de telles erreurs. Lorsqu’une erreur se produit, le processus doit appeler la fonction [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) pour effacer l’indicateur d’erreur avant de pouvoir commencer des opérations d’e/s supplémentaires. **ClearCommError** signale l’erreur spécifique qui s’est produite et l’état actuel de l’appareil.

 

 



