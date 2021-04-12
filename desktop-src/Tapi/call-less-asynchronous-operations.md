---
description: Cinq opérations asynchrones ne sont pas liées à un appel particulier.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Opérations asynchrones sans appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319254"
---
# <a name="call-less-asynchronous-operations"></a>Opérations asynchrones sans appel

Cinq opérations asynchrones ne sont pas liées à un appel particulier. Les fonctions TAPI 2. x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)et [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) lancent ces opérations. Si une application lance l’une de ces opérations asynchrones et appelle [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), le fournisseur de services peut ne pas recevoir d’indication que l’application a abandonné la fonction. Cela peut se produire si l’application n’était pas la seule application pour ouvrir la ligne. Si l’application appelle **lineClose** avec l’une de ces opérations en attente et qu’il s’agit de la seule application avec un handle vers la ligne, TAPI appelle la fonction [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) et le fournisseur de services doit mettre fin à l’opération asynchrone, en appelant la fonction de rappel de [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) pour chaque opération en suspens avec la \_ valeur d’erreur LINEERR OPERATIONFAILED.

 

 
