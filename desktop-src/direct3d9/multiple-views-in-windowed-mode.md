---
description: 'En plus de la chaîne de permutation qui est détenue et manipulée par l’intermédiaire de l’objet Direct3DDevice, une application peut utiliser la méthode IDirect3DDevice9 :: CreateAdditionalSwapChain pour créer des chaînes de permutation supplémentaires pour présenter plusieurs vues à partir du même appareil.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Plusieurs vues en mode fenêtre (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106541173"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="ed9eb-103">Plusieurs vues en mode fenêtre (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ed9eb-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="ed9eb-104">En plus de la chaîne de permutation qui est détenue et manipulée par l’intermédiaire de l’objet Direct3DDevice, une application peut utiliser la méthode [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) pour créer des chaînes de permutation supplémentaires pour présenter plusieurs vues à partir du même appareil.</span><span class="sxs-lookup"><span data-stu-id="ed9eb-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="ed9eb-105">En règle générale, l’application crée une chaîne de permutation par vue et associe chaque chaîne de permutation à une vue particulière.</span><span class="sxs-lookup"><span data-stu-id="ed9eb-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="ed9eb-106">L’application restitue des images dans les mémoires tampons d’arrière-plan de chaque chaîne de permutation, puis utilise la méthode [**IDirect3DDevice9 ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) replaced pour les présenter individuellement.</span><span class="sxs-lookup"><span data-stu-id="ed9eb-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="ed9eb-107">Notez qu’une seule chaîne de permutation à la fois peut être en plein écran sur chaque carte.</span><span class="sxs-lookup"><span data-stu-id="ed9eb-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed9eb-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed9eb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed9eb-109">Présentation d’une scène</span><span class="sxs-lookup"><span data-stu-id="ed9eb-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 
