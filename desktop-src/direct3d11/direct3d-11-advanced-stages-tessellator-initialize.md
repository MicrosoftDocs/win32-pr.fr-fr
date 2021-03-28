---
title: Comment initialiser l’étape du paveur
description: Cette rubrique montre comment initialiser l’étape du paveur.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990593"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="4af08-103">Comment : initialiser l’étape du paveur</span><span class="sxs-lookup"><span data-stu-id="4af08-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="4af08-104">En général, la facettisation étend le modèle compact, défini par l’utilisateur, d’un correctif dans une géométrie qui contient une quantité programmable de détails.</span><span class="sxs-lookup"><span data-stu-id="4af08-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="4af08-105">La géométrie est généralement un ensemble de triangles qui représente une géométrie de surface détaillée.</span><span class="sxs-lookup"><span data-stu-id="4af08-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="4af08-106">Cette rubrique montre comment initialiser l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="4af08-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="4af08-107">L’étape du paveur est la seconde des trois étapes qui fonctionnent ensemble pour paver ou juxtaposer une surface.</span><span class="sxs-lookup"><span data-stu-id="4af08-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="4af08-108">La première étape est l’étape de nuanceur de coque ; Il fonctionne une fois par correctif et configure la façon dont l’étape suivante (la fonction fixe du paveur) se comporte.</span><span class="sxs-lookup"><span data-stu-id="4af08-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="4af08-109">Un nuanceur de coque génère également des sorties définies par l’utilisateur, telles que des points de contrôle de sortie et des constantes de correction qui sont envoyées au-delà du du paveur directement à la troisième étape, l’étape de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="4af08-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="4af08-110">Un nuanceur de domaine est appelé une fois par point de du paveur et évalue les positions de surface.</span><span class="sxs-lookup"><span data-stu-id="4af08-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="4af08-111">L’étape du paveur est une étape de fonction fixe, aucun nuanceur à générer et aucun État à définir.</span><span class="sxs-lookup"><span data-stu-id="4af08-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="4af08-112">Elle reçoit tout son état d’installation à partir de l’étape de nuanceur de coque ; une fois que l’étape de nuanceur de coque a été initialisée, l’étape du paveur est initialisée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4af08-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="4af08-113">**Pour initialiser l’étape du paveur**</span><span class="sxs-lookup"><span data-stu-id="4af08-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="4af08-114">Initialisez l’étape de nuanceur de coque à l’aide de [**ID3D11DeviceContext :: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="4af08-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="4af08-115">*ppClassInstances* est un pointeur vers un tableau d’interfaces de nuanceur, représenté par les pointeurs [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) et le nombre d’interfaces, représenté par *NumClassInstances*.</span><span class="sxs-lookup"><span data-stu-id="4af08-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="4af08-116">Si ce paramètre n’est pas utilisé, ces paramètres peuvent avoir la valeur **null** et la valeur 0 respectivement.</span><span class="sxs-lookup"><span data-stu-id="4af08-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="4af08-117">Après l’initialisation de l’étape de nuanceur de coque, vous devez également initialiser l’étape de nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="4af08-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4af08-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4af08-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4af08-119">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4af08-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="4af08-120">Vue d’ensemble de la polygonalisation</span><span class="sxs-lookup"><span data-stu-id="4af08-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




