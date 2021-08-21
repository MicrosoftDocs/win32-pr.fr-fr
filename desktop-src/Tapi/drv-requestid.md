---
description: Le \_ type de données DRV REQUESTID est utilisé pour fournir un identificateur unique pour une demande au fournisseur de services.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e75e593ccbf2d9d8135fbb52762a83a539dc29f8ef9446735d0898d3437e37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866539"
---
# <a name="drv_requestid"></a>DRV \_ REQUESTID

Le type de données **DRV \_ REQUESTID** est utilisé pour fournir un identificateur unique pour une demande au fournisseur de services. Une valeur de ce type est passée en tant que paramètre à chaque fonction qui autorise l’opération asynchrone. Si l’opération est asynchrone, le fournisseur de services retourne cette valeur comme valeur de retour de la fonction. Chaque fois que le fournisseur de services marque une requête comme asynchrone de cette manière, il doit finalement signaler que l’opération est terminée en appelant la fonction de rappel de la [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) .

L’interface TAPI garantit que les valeurs du **DRV \_ REQUESTID** fournies sont strictement positives, c’est-à-dire entre les valeurs 0x00000001 et 0x7FFFFFFF incluses. En outre, les valeurs sont uniques dans la mesure où aucune valeur retournée par une fonction pour marquer la requête comme asynchrone est réutilisée avant que l’opération ne soit signalée comme terminée.

 

 
