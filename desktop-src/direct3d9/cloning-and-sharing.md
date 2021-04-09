---
description: Clonage et partage (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonage et partage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861630"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="4edfd-103">Clonage et partage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4edfd-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="4edfd-104">Clonage des paramètres</span><span class="sxs-lookup"><span data-stu-id="4edfd-104">Cloning Parameters</span></span>

<span data-ttu-id="4edfd-105">Le clonage a les restrictions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4edfd-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="4edfd-106">Les clones héritent du pool de l’effet d’origine.</span><span class="sxs-lookup"><span data-stu-id="4edfd-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="4edfd-107">Consultez la section paramètres de partage.</span><span class="sxs-lookup"><span data-stu-id="4edfd-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="4edfd-108">Les clones héritent des techniques, des passes, des paramètres et des annotations de l’effet d’origine (y compris toutes les annotations ajoutées à [**ID3DXEffect**](id3dxeffect.md)).</span><span class="sxs-lookup"><span data-stu-id="4edfd-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="4edfd-109">Les clones héritent des annotations ajoutées dynamiquement de l’effet d’origine.</span><span class="sxs-lookup"><span data-stu-id="4edfd-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="4edfd-110">Le clonage sur un nouvel appareil échoue si le pool de l’effet d’origine n’était pas **null** et que l’effet d’origine contenait un paramètre dépendant du périphérique partagé (tel qu’une texture ou un nuanceur).</span><span class="sxs-lookup"><span data-stu-id="4edfd-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="4edfd-111">Paramètres de partage</span><span class="sxs-lookup"><span data-stu-id="4edfd-111">Sharing Parameters</span></span>

<span data-ttu-id="4edfd-112">Un pool est une mémoire tampon qui partage des paramètres d’effet entre différents effets.</span><span class="sxs-lookup"><span data-stu-id="4edfd-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="4edfd-113">Pour ajouter des paramètres à un pool, spécifiez une utilisation partagée lors de la création de l’effet.</span><span class="sxs-lookup"><span data-stu-id="4edfd-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="4edfd-114">Un pool a les restrictions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4edfd-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="4edfd-115">Un paramètre est ajouté au pool la première fois qu’un effet contenant ce paramètre (partagé) est ajouté au pool.</span><span class="sxs-lookup"><span data-stu-id="4edfd-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="4edfd-116">Un pool obtient les valeurs initiales du premier paramètre partagé ; les paramètres partagés reçoivent ensuite leurs valeurs à partir du pool.</span><span class="sxs-lookup"><span data-stu-id="4edfd-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="4edfd-117">Un paramètre est supprimé du pool lorsque toutes les références d’effet au paramètre Shared sont libérées.</span><span class="sxs-lookup"><span data-stu-id="4edfd-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="4edfd-118">Tous les effets du pool qui contiennent le même paramètre dépendant du périphérique (partagé) doivent avoir le même appareil.</span><span class="sxs-lookup"><span data-stu-id="4edfd-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="4edfd-119">La **valeur null** peut être utilisée pour ne spécifier aucun pool, auquel cas aucun paramètre n’est partagé.</span><span class="sxs-lookup"><span data-stu-id="4edfd-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="4edfd-120">Cela revient presque à spécifier un pool unique uniquement pour cet effet.</span><span class="sxs-lookup"><span data-stu-id="4edfd-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="4edfd-121">La seule différence est que, lorsque l’effet est cloné, le clone ne partage pas ses paramètres partagés avec le d’origine.</span><span class="sxs-lookup"><span data-stu-id="4edfd-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4edfd-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4edfd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4edfd-123">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="4edfd-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



