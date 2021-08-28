---
description: Quand une application appelle la fonction lineClose avec une ou plusieurs opérations asynchrones en suspens, TAPI peut demander au fournisseur de services d’arrêter les opérations asynchrones associées à un appel.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Fin des opérations asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d026754af75743314fbdbf7a2a3c82f9935f9b053f2a7186f095e4f452a0bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772999"
---
# <a name="termination-of-asynchronous-operations"></a>Fin des opérations asynchrones

Lorsqu’une application appelle la fonction [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) avec une ou plusieurs opérations asynchrones en suspens, TAPI peut demander au fournisseur de services d’arrêter les opérations asynchrones associées à un appel, selon que l’application est le seul propriétaire de l’appel et qu’elle a le seul descripteur à l’appel.

Si l’application est le seul propriétaire d’un appel, TAPI appelle [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (selon le fournisseur) pour chacun de ces appels. Le fournisseur de services doit vérifier toutes les opérations asynchrones en attente associées à l’appel en cours de suppression. Si une opération en attente existe, le fournisseur de services doit prendre l’action appropriée, ce qui peut entraîner l’arrêt de l’opération en cours.

Si l’application a le seul descripteur d’un appel (c’est-à-dire qu’il n’y a pas d’autres propriétaires ou analyses), TAPI appelle la fonction [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Le fournisseur de services doit considérer cet appel comme l’indication absolue que les opérations asynchrones en attente doivent être abandonnées. Le fournisseur de services doit garantir une achèvement ordonné de l’appel et doit appeler la fonction de rappel d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) pour toutes les opérations asynchrones en suspens, en spécifiant la \_ valeur d’erreur LINEERR OPERATIONFAILED. Si TAPI avait précédemment appelé la fonction [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) , il appelle **TSPI \_ lineCloseCall** immédiatement après le retour du fournisseur de services de l’autre appel ; il n’attend pas la fin de l’opération asynchrone associée à la fonction TSPI **\_ lineDrop** .

Si l’application n’est pas le seul propriétaire de l’appel, TAPI n’appelle pas [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop). Si l’application n’a pas le seul descripteur de l’appel, TAPI n’appelle pas la fonction [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Si l’application n’est ni le seul propriétaire, ni le seul possesseur d’un descripteur de l’appel, TAPI n’envoie aucune notification au fournisseur de services, et par conséquent, les opérations asynchrones en attente restent intactes. Cela signifie que ces applications ne peuvent pas terminer les opérations asynchrones qu’elles ont démarrées à l’aide de la fonction [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) . Toutefois, étant donné que chaque opération asynchrone requiert que l’application appelante soit propriétaire de l’appel, la probabilité qu’une application ne soit pas en mesure de terminer les opérations asynchrones soit très rare. Si c’est le cas, les autres propriétaires du ou des appels doivent assumer la responsabilité de la disposition du ou des appels.

Si TAPI appelle [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) ou [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop), le fournisseur de services doit finalement envoyer un \_ message LINECALLSTATE Idle pour l’appel associé (sauf si [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) est appelé en premier) afin que les analyses de l’appel puissent être nettoyées. Lorsque le dernier analyseur a appelé la fonction [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) , l’interface TAPI appelle la fonction **TSPI \_ lineCloseCall** . toutes les opérations en attente doivent être terminées ou terminées et l' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) appelé, comme décrit précédemment.

 

 
