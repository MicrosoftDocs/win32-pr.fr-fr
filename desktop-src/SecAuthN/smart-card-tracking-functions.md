---
description: Vous permettent d’effectuer le suivi des cartes au sein des lecteurs. Ces routines utilisent généralement la \_ structure READERSTATE de cicatrices dans un tableau.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Fonctions de suivi des cartes à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867457"
---
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="17817-104">Fonctions de suivi des cartes à puce</span><span class="sxs-lookup"><span data-stu-id="17817-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="17817-105">Les fonctions suivantes vous permettent d’effectuer le suivi des cartes au sein des lecteurs.</span><span class="sxs-lookup"><span data-stu-id="17817-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="17817-106">Ces routines utilisent généralement la structure [**\_ READERSTATE de cicatrices**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="17817-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="17817-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="17817-107">Topic</span></span>                                                | <span data-ttu-id="17817-108">Description</span><span class="sxs-lookup"><span data-stu-id="17817-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17817-109">**SCardLocateCards**</span><span class="sxs-lookup"><span data-stu-id="17817-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="17817-110">Recherchez une carte dont la [*chaîne ATR*](../secgloss/a-gly.md) correspond à un nom de carte fourni.</span><span class="sxs-lookup"><span data-stu-id="17817-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="17817-111">**SCardGetStatusChange**</span><span class="sxs-lookup"><span data-stu-id="17817-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="17817-112">Bloquer l’exécution jusqu’à ce que la disponibilité actuelle des cartes change.</span><span class="sxs-lookup"><span data-stu-id="17817-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="17817-113">**SCardCancel**</span><span class="sxs-lookup"><span data-stu-id="17817-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="17817-114">Terminez les actions en suspens.</span><span class="sxs-lookup"><span data-stu-id="17817-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
