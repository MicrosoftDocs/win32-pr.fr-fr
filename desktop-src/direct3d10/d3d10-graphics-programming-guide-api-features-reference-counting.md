---
description: Les fonctions set de Direct3D 10 ne contiennent pas de référence à un objet enfant d’appareil.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Comptage de références (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335453"
---
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="38038-103">Comptage de références (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="38038-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="38038-104">Les fonctions set de Direct3D 10 ne contiennent pas de référence à un objet enfant d’appareil.</span><span class="sxs-lookup"><span data-stu-id="38038-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="38038-105">Cela signifie que chaque application doit contenir une référence à un objet enfant d’appareil tant que l’objet doit être lié au pipeline.</span><span class="sxs-lookup"><span data-stu-id="38038-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="38038-106">Lorsque le décompte de références d’un objet tombe à zéro, l’objet est supprimé du pipeline et détruit.</span><span class="sxs-lookup"><span data-stu-id="38038-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="38038-107">Ce style d’exploitation de référence est également connu sous le nom d’exploitation de référence faible, car chaque emplacement de liaison de pipeline contient une référence faible à l’interface/l’objet qui lui est lié.</span><span class="sxs-lookup"><span data-stu-id="38038-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="38038-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="38038-108">For example:</span></span>


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





<span data-ttu-id="38038-109">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="38038-109">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="38038-110">Dans Direct3D 9, les fonctions set contiennent une référence aux objets appareil ; dans Direct3D 10, les fonctions set ne contiennent pas de référence aux objets enfants de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="38038-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="38038-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38038-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38038-112">Fonctionnalités de l’API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="38038-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




