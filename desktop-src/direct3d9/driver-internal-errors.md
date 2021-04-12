---
description: Dans Direct3D 9, Direct3D autorise le pilote à retourner des codes d’erreur tels que E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY et D3DERR \_ UNSUPPORTEDCOLORARG afin qu’une application puisse y répondre.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Erreurs internes du pilote (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109342"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="e3805-103">Erreurs internes du pilote (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e3805-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="e3805-104">Dans Direct3D 9, Direct3D autorise le pilote à retourner des codes d’erreur tels que E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY et D3DERR \_ UNSUPPORTEDCOLORARG afin qu’une application puisse y répondre.</span><span class="sxs-lookup"><span data-stu-id="e3805-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="e3805-105">Toutefois, parfois, les appels d’API qui ont généré ces types de retour sont chargés dans une mémoire tampon de commande et sont traités par lot pour être envoyés au GPU (consultez [contrôle des optimisations du runtime et du pilote](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="e3805-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="e3805-106">Dans ce cas, les erreurs ne peuvent pas être relayées à l’application lorsque l’action doit être exécutée. le code d’erreur est donc consommé par le runtime et une remarque est faite sur l’objet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e3805-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="e3805-107">Plus tard, quand l’application appelle [**IDirect3DDevice9 ::P renvoyée**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9 ::P renvoyée** renverra D3DERR \_ DRIVERINTERNALERROR.</span><span class="sxs-lookup"><span data-stu-id="e3805-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="e3805-108">C’est pour cette raison que la meilleure approche pour une application de recevoir un \_ DRIVERINTERNALERROR D3DERR à partir de **IDirect3DDevice9 ::P renvoyée** consiste à détruire et à recréer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e3805-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="e3805-109">Si vous souhaitez essayer de déboguer davantage, voici quelques suggestions pour tenter de déterminer l’appel d’API qui génère l’erreur :</span><span class="sxs-lookup"><span data-stu-id="e3805-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="e3805-110">Étant donné que la liste des valeurs de retour possibles n’est pas complète, vous pouvez essayer de trouver l’appel qui échoue en entourant chaque appel d’API comme suit :</span><span class="sxs-lookup"><span data-stu-id="e3805-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="e3805-111">Le flux de débogage de sortie doit ensuite afficher l’appel qui est à l’origine du problème.</span><span class="sxs-lookup"><span data-stu-id="e3805-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="e3805-112">En outre, à des fins de débogage, essayez d’appeler [**IDirect3DDevice9 :: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immédiatement avant chaque [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) pour voir s’il existe un problème supplémentaire avec le pilote de périphérique (opération non prise en charge, combinaison inutilisable de formats de texture, etc.).</span><span class="sxs-lookup"><span data-stu-id="e3805-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="e3805-113">[**IDirect3DDevice9 :: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) doit être utilisé avec soin et avec modération en raison de la quantité de travail de validation que le pilote doit effectuer pour retourner une réponse.</span><span class="sxs-lookup"><span data-stu-id="e3805-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="e3805-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3805-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3805-115">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="e3805-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
