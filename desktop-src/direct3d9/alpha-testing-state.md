---
description: Les applications C++ peuvent utiliser le test alpha pour contrôler le moment où les pixels sont écrits dans la surface de cible de rendu.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: État des tests alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514755"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="3f42f-103">État des tests alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3f42f-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="3f42f-104">Les applications C++ peuvent utiliser le test alpha pour contrôler le moment où les pixels sont écrits dans la surface de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="3f42f-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="3f42f-105">En utilisant l’état de rendu [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) , votre application définit l’appareil Direct3D actuel pour qu’il teste chaque pixel en fonction d’une fonction de test alpha.</span><span class="sxs-lookup"><span data-stu-id="3f42f-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="3f42f-106">Si le test a abouti, le pixel est écrit sur l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="3f42f-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="3f42f-107">Si ce n’est pas le cas, Direct3D ignore le pixel.</span><span class="sxs-lookup"><span data-stu-id="3f42f-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="3f42f-108">Sélectionnez la fonction de test alpha avec l’état de rendu **D3DRS \_ ALPHAFUNC** .</span><span class="sxs-lookup"><span data-stu-id="3f42f-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="3f42f-109">Votre application peut définir une valeur alpha de référence pour tous les pixels à comparer à l’aide de l’état de rendu **D3DRS \_ ALPHAREF** .</span><span class="sxs-lookup"><span data-stu-id="3f42f-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="3f42f-110">L’utilisation la plus courante pour le test alpha consiste à améliorer les performances lors de la pixellisation d’objets presque transparents.</span><span class="sxs-lookup"><span data-stu-id="3f42f-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="3f42f-111">Si les données de couleur en cours de pixellisation sont plus opaques que la couleur à un pixel donné (D3DPCMPCAPS \_ greaterequal à), le pixel est alors écrit.</span><span class="sxs-lookup"><span data-stu-id="3f42f-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="3f42f-112">Dans le cas contraire, le rastériseur ignore complètement le pixel, en enregistrant le traitement requis pour mélanger les deux couleurs.</span><span class="sxs-lookup"><span data-stu-id="3f42f-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="3f42f-113">L’exemple de code suivant vérifie si une fonction de comparaison donnée est prise en charge et, si c’est le cas, elle définit les paramètres de fonction de comparaison requis pour améliorer les performances lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="3f42f-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="3f42f-114">Tous les matériels ne prennent pas en charge toutes les fonctionnalités de test alpha.</span><span class="sxs-lookup"><span data-stu-id="3f42f-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="3f42f-115">Vous pouvez vérifier les fonctionnalités de l’appareil en appelant la méthode [**IDirect3D9 :: GetDeviceCaps**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="3f42f-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="3f42f-116">Après avoir récupéré les fonctionnalités de l’appareil, vérifiez le membre AlphaCmpCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associé pour la fonction de comparaison souhaitée.</span><span class="sxs-lookup"><span data-stu-id="3f42f-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="3f42f-117">Si le membre AlphaCmpCaps contient uniquement la \_ fonctionnalité D3DPCMPCAPS Always ou seulement le D3DPCMPCAPS ne \_ fonctionne jamais, le pilote ne prend pas en charge les tests alpha.</span><span class="sxs-lookup"><span data-stu-id="3f42f-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f42f-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f42f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f42f-119">États de rendu</span><span class="sxs-lookup"><span data-stu-id="3f42f-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
