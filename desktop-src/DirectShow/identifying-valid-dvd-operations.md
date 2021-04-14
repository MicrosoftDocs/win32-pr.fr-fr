---
description: Identification des opérations DVD valides
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identification des opérations DVD valides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392768"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="ac260-103">Identification des opérations DVD valides</span><span class="sxs-lookup"><span data-stu-id="ac260-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="ac260-104">Plusieurs facteurs déterminent si vous pouvez effectuer une opération DVD donnée :</span><span class="sxs-lookup"><span data-stu-id="ac260-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="ac260-105">Domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="ac260-105">The current domain.</span></span> <span data-ttu-id="ac260-106">Certaines commandes ne sont valides que dans certains domaines.</span><span class="sxs-lookup"><span data-stu-id="ac260-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="ac260-107">Lorsque le domaine change, le navigateur envoie un \_ événement de modification de domaine de DVD EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ac260-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="ac260-108">Vous pouvez également appeler [**IDvdInfo2 :: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) pour accéder au domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="ac260-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="ac260-109">Indicateurs UOPS.</span><span class="sxs-lookup"><span data-stu-id="ac260-109">UOPS flags.</span></span> <span data-ttu-id="ac260-110">Il s’agit d’indicateurs écrits sur le disque, indiquant les opérations autorisées.</span><span class="sxs-lookup"><span data-stu-id="ac260-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="ac260-111">Chaque fois que les indicateurs changent, le navigateur envoie un \_ événement de modification UOPs de DVD ce DVD \_ \_ \_ avec les nouveaux indicateurs.</span><span class="sxs-lookup"><span data-stu-id="ac260-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="ac260-112">Vous pouvez également appeler [**IDvdInfo2 :: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) pour récupérer les indicateurs UOPs actuels.</span><span class="sxs-lookup"><span data-stu-id="ac260-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="ac260-113">Contenu du DVD.</span><span class="sxs-lookup"><span data-stu-id="ac260-113">DVD content.</span></span> <span data-ttu-id="ac260-114">Certaines commandes peuvent ne pas être pertinentes en fonction du contenu du DVD.</span><span class="sxs-lookup"><span data-stu-id="ac260-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="ac260-115">Par exemple, la méthode [**IDvdControl2 :: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) peut être autorisée en fonction du domaine actuel et des indicateurs UOPs, mais la vidéo peut avoir un seul angle.</span><span class="sxs-lookup"><span data-stu-id="ac260-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="ac260-116">Dans ce cas, l’appel **SelectAngle** est autorisé, mais n’est pas une option significative.</span><span class="sxs-lookup"><span data-stu-id="ac260-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="ac260-117">En cas de doute, autoriser une action.</span><span class="sxs-lookup"><span data-stu-id="ac260-117">When in doubt, permit an action.</span></span> <span data-ttu-id="ac260-118">Au pire, la méthode [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) échoue et vous pouvez fournir des commentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ac260-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="ac260-119">Les commentaires doivent être relativement discrets.</span><span class="sxs-lookup"><span data-stu-id="ac260-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="ac260-120">Par exemple, vous pouvez faire clignoter un petit X rouge pour alerter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ac260-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="ac260-121">Le navigateur DVD retourne VFW \_ e \_ DVD \_ INVALIDDOMAIN lorsque le domaine interdit une opération, et que le \_ fonctionnement du DVD VFW e est \_ \_ \_ bloqué lorsque les indicateurs UOPs interdisent une opération.</span><span class="sxs-lookup"><span data-stu-id="ac260-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac260-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac260-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac260-123">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="ac260-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



