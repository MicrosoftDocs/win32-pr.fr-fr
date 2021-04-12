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
# <a name="call-less-asynchronous-operations"></a><span data-ttu-id="20774-103">Opérations asynchrones sans appel</span><span class="sxs-lookup"><span data-stu-id="20774-103">Call-less Asynchronous Operations</span></span>

<span data-ttu-id="20774-104">Cinq opérations asynchrones ne sont pas liées à un appel particulier.</span><span class="sxs-lookup"><span data-stu-id="20774-104">There are five asynchronous operations that are not related to any particular call.</span></span> <span data-ttu-id="20774-105">Les fonctions TAPI 2. x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)et [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) lancent ces opérations.</span><span class="sxs-lookup"><span data-stu-id="20774-105">The TAPI 2.x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal), and [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) functions initiate these operations.</span></span> <span data-ttu-id="20774-106">Si une application lance l’une de ces opérations asynchrones et appelle [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), le fournisseur de services peut ne pas recevoir d’indication que l’application a abandonné la fonction.</span><span class="sxs-lookup"><span data-stu-id="20774-106">If an application initiates one of these asynchronous operations and calls [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), the service provider may receive no indication that the application has abandoned the function.</span></span> <span data-ttu-id="20774-107">Cela peut se produire si l’application n’était pas la seule application pour ouvrir la ligne.</span><span class="sxs-lookup"><span data-stu-id="20774-107">This can occur if the application was not the only application to have the line open.</span></span> <span data-ttu-id="20774-108">Si l’application appelle **lineClose** avec l’une de ces opérations en attente et qu’il s’agit de la seule application avec un handle vers la ligne, TAPI appelle la fonction [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) et le fournisseur de services doit mettre fin à l’opération asynchrone, en appelant la fonction de rappel de [*\_ procédure d’achèvement*](/windows/win32/api/tspi/nc-tspi-async_completion) pour chaque opération en suspens avec la \_ valeur d’erreur LINEERR OPERATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="20774-108">If the application calls **lineClose** with one of these operations pending, and it is the only application with a handle to the line, TAPI calls the [**TSPI\_lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) function and the service provider should terminate the asynchronous operation, calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function for each such outstanding operation with the LINEERR\_OPERATIONFAILED error value.</span></span>

 

 
