---
title: Le modèle actuel mis en file d’attente est déconseillé
description: Le modèle actuel mis en file d’attente est déconseillé
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "106511108"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="ded77-103">Le modèle actuel mis en file d’attente est déconseillé</span><span class="sxs-lookup"><span data-stu-id="ded77-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="ded77-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="ded77-104">Platforms</span></span>

<span data-ttu-id="ded77-105">**Clients** – après Windows 8</span><span class="sxs-lookup"><span data-stu-id="ded77-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="ded77-106">**Serveurs** – après Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ded77-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="ded77-107">Description</span><span class="sxs-lookup"><span data-stu-id="ded77-107">Description</span></span>

<span data-ttu-id="ded77-108">Dans la version Windows ultérieure à Windows 8, ces API retournent E \_ NOTIMPL :</span><span class="sxs-lookup"><span data-stu-id="ded77-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="ded77-109">DwmSetPresentParameters</span><span class="sxs-lookup"><span data-stu-id="ded77-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="ded77-110">DwmSetDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="ded77-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="ded77-111">DwmModifyPreviousDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="ded77-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="ded77-112">En outre, cette API n’accepte que la valeur NULL pour le paramètre HWND :</span><span class="sxs-lookup"><span data-stu-id="ded77-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="ded77-113">DwmGetCompositionTimingInfo</span><span class="sxs-lookup"><span data-stu-id="ded77-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="ded77-114">Nous allons arrêter de prendre en charge DwmGetCompositionTimingInfo avec HWND ! = NULL et supprimer les fonctionnalités associées.</span><span class="sxs-lookup"><span data-stu-id="ded77-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="ded77-115">Si vous spécifiez une valeur non NULL pour HWND, cette API retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ded77-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="ded77-116">Nous déconseillons également l’utilisation de l’API DwmGetCompositionTimingInfo et suggérons que les développeurs basculent vers le modèle de retournement DXGI et l’API de statistiques de présentation de DX associée.</span><span class="sxs-lookup"><span data-stu-id="ded77-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ded77-117">Manifestation</span><span class="sxs-lookup"><span data-stu-id="ded77-117">Manifestation</span></span>

<span data-ttu-id="ded77-118">Les applications qui utilisent le modèle présent mis en file d’attente ne fonctionneront pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ded77-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="ded77-119">La manifeste exacte dépend de l’application particulière, mais peut aller de la durée de présentation incorrecte à l’application se ferme de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="ded77-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="ded77-120">Dans la pratique, nous ne pensons pas que de nombreuses applications (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="ded77-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="ded77-121">Ce modèle a été utilisé par Vista Media Player, qui ne sera pas utilisé sur Windows 8 (et éventuellement l’ancien lecteur Zune).</span><span class="sxs-lookup"><span data-stu-id="ded77-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="ded77-122">À ce stade, nous n’avons pas d’informations sur les autres applications qui utilisent réellement ce modèle.</span><span class="sxs-lookup"><span data-stu-id="ded77-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="ded77-123">Solution</span><span class="sxs-lookup"><span data-stu-id="ded77-123">Solution</span></span>

<span data-ttu-id="ded77-124">Les développeurs doivent utiliser le mode de présentation DXGI à la place de la mise en file d’attente (disponible dans le runtime virtuel DX9 depuis Windows 7, ainsi que sur les runtimes facilement et DX11 dans Windows 8).</span><span class="sxs-lookup"><span data-stu-id="ded77-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="ded77-125">Tests</span><span class="sxs-lookup"><span data-stu-id="ded77-125">Tests</span></span>

<span data-ttu-id="ded77-126">Exécutez des tests généraux pour vous assurer que les composants Windows de la boîte de réception et les produits principaux continuent de fonctionner sur la prochaine version de Windows.</span><span class="sxs-lookup"><span data-stu-id="ded77-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 




