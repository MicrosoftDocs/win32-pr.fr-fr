---
description: Un terminal multipiste peut être considéré comme un terminal qui est une collection d’autres terminaux. Chaque terminal enfant (un &\# 0034 ; track&\# 0034 ;) peut être un terminal multipiste ou un seul terminal.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: À propos des terminaux multipiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517070"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="73b8b-104">À propos des terminaux multipiste</span><span class="sxs-lookup"><span data-stu-id="73b8b-104">About Multitrack Terminals</span></span>

<span data-ttu-id="73b8b-105">Un terminal multipiste peut être considéré comme un terminal qui est une collection d’autres terminaux.</span><span class="sxs-lookup"><span data-stu-id="73b8b-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="73b8b-106">Chaque terminal enfant (une « piste ») peut être un terminal multipiste ou un terminal simple.</span><span class="sxs-lookup"><span data-stu-id="73b8b-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="73b8b-107">Tous les terminaux multipiste exposent l’interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , qui comprend des méthodes génériques pour énumérer, créer et supprimer des terminaux de suivi d’un terminal multipiste.</span><span class="sxs-lookup"><span data-stu-id="73b8b-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="73b8b-108">Tous les terminaux, une seule piste et multipiste, exposent l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="73b8b-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="73b8b-109">Un client qui a un pointeur vers une interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) peut déterminer si le terminal est multipiste ou à une seule piste en interrogeant le terminal pour l’interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , qui est exposée uniquement sur les terminaux multipiste.</span><span class="sxs-lookup"><span data-stu-id="73b8b-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="73b8b-110">Le terminal parent peut utiliser l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de ses terminaux de suivi, ou il peut nécessiter le suivi des terminaux pour exposer des interfaces privées.</span><span class="sxs-lookup"><span data-stu-id="73b8b-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="73b8b-111">Pour plus d’informations, consultez [suivre des terminaux](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="73b8b-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 
