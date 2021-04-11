---
description: Résumé des mécanismes d’indication de la saisie semi-automatique avec chevauchement dans le SPI de Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Résumé des mécanismes d’indication de la saisie semi-automatique avec chevauchement dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112999"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="792c1-103">Résumé des mécanismes d’indication de la saisie semi-automatique avec chevauchement dans le SPI</span><span class="sxs-lookup"><span data-stu-id="792c1-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="792c1-104">Le tableau suivant résume la sémantique de saisie semi-automatique pour un socket Overlapped, en présentant les différentes combinaisons de *lpOverlapped*, **hEvent** et *lpCompletionRoutine*.</span><span class="sxs-lookup"><span data-stu-id="792c1-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="792c1-105">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="792c1-105">*lpOverlapped*</span></span> | <span data-ttu-id="792c1-106">**hEvent**</span><span class="sxs-lookup"><span data-stu-id="792c1-106">**hEvent**</span></span>     | <span data-ttu-id="792c1-107">*lpCompletionRoutine*</span><span class="sxs-lookup"><span data-stu-id="792c1-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="792c1-108">Indication de la saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="792c1-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="792c1-109">NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-109">NULL</span></span>           | <span data-ttu-id="792c1-110">Non applicable</span><span class="sxs-lookup"><span data-stu-id="792c1-110">Not applicable</span></span> | <span data-ttu-id="792c1-111">Ignoré</span><span class="sxs-lookup"><span data-stu-id="792c1-111">Ignored</span></span>               | <span data-ttu-id="792c1-112">L’opération se termine de façon synchrone, autrement dit, elle se comporte comme s’il s’agissait d’un socket nonoverlapped.</span><span class="sxs-lookup"><span data-stu-id="792c1-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="792c1-113">non NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-113">not NULL</span></span>       | <span data-ttu-id="792c1-114">NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-114">NULL</span></span>           | <span data-ttu-id="792c1-115">NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-115">NULL</span></span>                  | <span data-ttu-id="792c1-116">L’opération se termine, mais il n’existe pas de mécanisme de saisie semi-automatique pris en charge par Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="792c1-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="792c1-117">Le mécanisme de port de terminaison (s’il est pris en charge) peut être utilisé dans ce cas, sinon aucune notification de fin d’exécution n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="792c1-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="792c1-118">non NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-118">not NULL</span></span>       | <span data-ttu-id="792c1-119">non NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-119">not NULL</span></span>       | <span data-ttu-id="792c1-120">NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-120">NULL</span></span>                  | <span data-ttu-id="792c1-121">L’opération termine la superposition, la notification par l’objet d’événement de signalisation.</span><span class="sxs-lookup"><span data-stu-id="792c1-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="792c1-122">non NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-122">not NULL</span></span>       | <span data-ttu-id="792c1-123">Ignoré</span><span class="sxs-lookup"><span data-stu-id="792c1-123">Ignored</span></span>        | <span data-ttu-id="792c1-124">non NULL</span><span class="sxs-lookup"><span data-stu-id="792c1-124">not NULL</span></span>              | <span data-ttu-id="792c1-125">L’opération se termine par la routine de fin de la planification.</span><span class="sxs-lookup"><span data-stu-id="792c1-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



