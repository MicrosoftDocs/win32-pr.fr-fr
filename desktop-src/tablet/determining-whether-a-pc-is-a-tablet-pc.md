---
description: Vous pouvez parfois être amené à déterminer si votre application s’exécute sur un Tablet PC, car vous souhaiterez peut-être que vos applications tirent parti des fonctionnalités d’encre, de reconnaissance et de stylet inhérentes.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Déterminer si un PC est un Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545047"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="e64c8-103">Déterminer si un PC est un Tablet PC</span><span class="sxs-lookup"><span data-stu-id="e64c8-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="e64c8-104">Vous pouvez parfois être amené à déterminer si votre application s’exécute sur un Tablet PC, car vous souhaiterez peut-être que vos applications tirent parti des fonctionnalités d’encre, de reconnaissance et de stylet inhérentes.</span><span class="sxs-lookup"><span data-stu-id="e64c8-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="e64c8-105">Pour vous aider à déterminer si votre application a accès aux fonctionnalités Tablet PC, vous pouvez utiliser l’appel d’API Windows GetSystemMetrics () comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e64c8-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="e64c8-106">Applications Client-Side</span><span class="sxs-lookup"><span data-stu-id="e64c8-106">Client-Side Applications</span></span>

<span data-ttu-id="e64c8-107">Vous pouvez utiliser les techniques suivantes pour déterminer si votre code s’exécute sur un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e64c8-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="e64c8-108">Utilisation de GetSystemMetrics (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="e64c8-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="e64c8-109">Utilisation de la présence de fichiers binaires de plateforme de tablette</span><span class="sxs-lookup"><span data-stu-id="e64c8-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="e64c8-110">Applications Web</span><span class="sxs-lookup"><span data-stu-id="e64c8-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="e64c8-111">Utilisation de GetSystemMetrics (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="e64c8-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="e64c8-112">Windows XP Édition Tablet PC</span><span class="sxs-lookup"><span data-stu-id="e64c8-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="e64c8-113">Dans Microsoft Windows XP Tablet PC Edition, utilisez la fonction GetSystemMetrics (SM \_ TABLETPC) pour déterminer si un ordinateur est un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e64c8-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="e64c8-114">GetSystemMetrics (SM \_ TABLETPC) est conçu pour retourner la valeur true sur un ordinateur exécutant Windows XP Édition Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e64c8-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="e64c8-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e64c8-115">Windows Vista</span></span>

<span data-ttu-id="e64c8-116">Dans Windows Vista, il n’existe plus de kit de développement logiciel (SDK) Tablet PC distinct.</span><span class="sxs-lookup"><span data-stu-id="e64c8-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="e64c8-117">Le SDK Windows contient maintenant une section appelée « technologie Tablet PC et Touch », et la logique de GetSystemMetrics (SM \_ TABLETPC) a été modifiée pour en tenir compte.</span><span class="sxs-lookup"><span data-stu-id="e64c8-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="e64c8-118">GetSystemMetrics (SM \_ TABLETPC) renvoie désormais la valeur true si toutes les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="e64c8-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="e64c8-119">Il existe un digitaliseur intégré, à savoir PEN ou Touch, sur le système.</span><span class="sxs-lookup"><span data-stu-id="e64c8-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="e64c8-120">Le composant facultatif Tablet PC est installé.</span><span class="sxs-lookup"><span data-stu-id="e64c8-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="e64c8-121">Ce composant contient des fonctionnalités telles que le panneau de saisie Tablet PC et le journal Windows.</span><span class="sxs-lookup"><span data-stu-id="e64c8-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="e64c8-122">L’ordinateur est concédé sous licence pour utiliser le composant facultatif.</span><span class="sxs-lookup"><span data-stu-id="e64c8-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="e64c8-123">Les versions Premium de Windows Vista, telles que Windows Vista Édition familiale Premium, Windows Vista petite entreprise, Windows Vista Professionnel, Windows Vista entreprise et Windows Vista Édition intégrale, sont concédées sous licence pour utiliser le composant facultatif.</span><span class="sxs-lookup"><span data-stu-id="e64c8-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="e64c8-124">Le service d’entrée du Tablet PC est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e64c8-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="e64c8-125">Tablet PC Input service est un nouveau service pour Windows Vista qui contrôle l’entrée Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e64c8-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="e64c8-126">Avec cette précision accrue, GetSystemMetrics (SM \_ TABLETPC) continue d’être la méthode recommandée pour déterminer si un ordinateur exécutant Windows Vista est un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e64c8-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="e64c8-127">Utilisation de la présence de fichiers binaires de plateforme de tablette</span><span class="sxs-lookup"><span data-stu-id="e64c8-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="e64c8-128">Dans Windows XP Édition Tablet PC et Windows Vista, vous pouvez rechercher la présence des binaires manuscrits, tels que inkobj.dll et Microsoft.Ink.dll, et utiliser leurs fonctionnalités prises en charge si elles sont présentes.</span><span class="sxs-lookup"><span data-stu-id="e64c8-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="e64c8-129">Dans Windows Vista, les fichiers binaires de la plateforme Tablet PC sont installés par défaut sur toutes les versions du client.</span><span class="sxs-lookup"><span data-stu-id="e64c8-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="e64c8-130">Les fonctionnalités d’entrée et d’entrée manuscrite sont disponibles sur ces versions.</span><span class="sxs-lookup"><span data-stu-id="e64c8-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="e64c8-131">La reconnaissance n’est disponible que dans les versions Premium de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e64c8-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="e64c8-132">Applications Web-Based</span><span class="sxs-lookup"><span data-stu-id="e64c8-132">Web-Based Applications</span></span>

<span data-ttu-id="e64c8-133">Dans Windows Vista, la chaîne de l’agent utilisateur signalée par Internet Explorer comprend « Tablet PC 2,0 » si, selon GetSystemMetrics (SM \_ TABLETPC), l’appareil est un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="e64c8-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="e64c8-134">Dans Windows XP Édition Tablet PC 2005, la chaîne User-agent comprend Tablet PC 1,7.</span><span class="sxs-lookup"><span data-stu-id="e64c8-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="e64c8-135">La chaîne User-agent ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e64c8-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="e64c8-136">Utilisez cette valeur pour déterminer si l’ordinateur client est un Tablet PC et prend en charge les contrôles d’encrage basés sur le Web.</span><span class="sxs-lookup"><span data-stu-id="e64c8-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e64c8-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e64c8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e64c8-138">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="e64c8-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
