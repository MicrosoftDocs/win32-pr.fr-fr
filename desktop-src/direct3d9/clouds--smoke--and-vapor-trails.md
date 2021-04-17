---
description: Les Clouds, les fumées et les traces de vapeur peuvent tous être créés par une extension de la technique de l’interrogation.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, fumées et traces de vapeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566698"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="f2648-103">Clouds, fumées et traces de vapeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f2648-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="f2648-104">Les Clouds, les fumées et les traces de vapeur peuvent tous être créés par une extension de la technique de l’interrogation.</span><span class="sxs-lookup"><span data-stu-id="f2648-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="f2648-105">Voir la rubrique sur les [panneaux (Direct3D 9)](billboarding.md).</span><span class="sxs-lookup"><span data-stu-id="f2648-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="f2648-106">En faisant pivoter le panneau sur deux axes au lieu d’un, votre application peut permettre à l’utilisateur d’afficher un panneau à partir de n’importe quel angle.</span><span class="sxs-lookup"><span data-stu-id="f2648-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="f2648-107">En règle générale, une application fait pivoter le panneau sur les axes horizontal et vertical.</span><span class="sxs-lookup"><span data-stu-id="f2648-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="f2648-108">Pour créer un Cloud simple, votre application peut faire pivoter une primitive rectangulaire sur un ou deux axes afin que la primitive soit face à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f2648-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="f2648-109">Une texture de type Cloud peut ensuite être appliquée à la primitive avec transparence.</span><span class="sxs-lookup"><span data-stu-id="f2648-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="f2648-110">Pour plus d’informations sur l’application de textures transparentes aux primitives, consultez [fusion de textures (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="f2648-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="f2648-111">Vous pouvez animer le Cloud en appliquant une série de textures au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="f2648-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="f2648-112">Une application peut créer des clouds plus complexes en les formant à partir d’un groupe de Primitives.</span><span class="sxs-lookup"><span data-stu-id="f2648-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="f2648-113">Chaque partie du Cloud est une primitive rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="f2648-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="f2648-114">Les primitives peuvent être déplacées indépendamment dans le temps pour obtenir l’apparence d’un brouillard dynamique.</span><span class="sxs-lookup"><span data-stu-id="f2648-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="f2648-115">L’illustration suivante montre ce concept.</span><span class="sxs-lookup"><span data-stu-id="f2648-115">The following illustration shows this concept.</span></span>

![illustration des primitives qui forment des clouds plus complexes](images/cloud.png)

<span data-ttu-id="f2648-117">L’apparence de la fumée est affichée de manière similaire aux clouds.</span><span class="sxs-lookup"><span data-stu-id="f2648-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="f2648-118">Elle nécessite généralement plusieurs panneaux, comme des clouds complexes.</span><span class="sxs-lookup"><span data-stu-id="f2648-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="f2648-119">En général, la fumée Billows et augmente au fil du temps, de sorte que les panneaux qui composent la prune de fumée doivent se déplacer en conséquence.</span><span class="sxs-lookup"><span data-stu-id="f2648-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="f2648-120">Vous devrez peut-être ajouter d’autres panneaux au fur et à mesure de l’augmentation et de la dispersion du prune.</span><span class="sxs-lookup"><span data-stu-id="f2648-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="f2648-121">Une piste de vapeur est un prune de fumée qui n’augmente pas.</span><span class="sxs-lookup"><span data-stu-id="f2648-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="f2648-122">Toutefois, comme une sorte de fumée, elle est dispersée dans le temps.</span><span class="sxs-lookup"><span data-stu-id="f2648-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="f2648-123">L’illustration suivante montre la technique consistant à utiliser des panneaux pour simuler une piste de vapeur.</span><span class="sxs-lookup"><span data-stu-id="f2648-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![illustration des panneaux qui simulent une piste de vapeur](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="f2648-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2648-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2648-126">Exemples alpha</span><span class="sxs-lookup"><span data-stu-id="f2648-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



