---
description: Mode exclusif DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Mode exclusif DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513116"
---
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="3ad0b-103">Mode exclusif DirectDraw</span><span class="sxs-lookup"><span data-stu-id="3ad0b-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="3ad0b-104">Cette rubrique s’applique uniquement à VMR-7.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="3ad0b-105">Dans VMR-9, vous activez le mode exclusif en fournissant votre propre allocateur en mode exclusif-présentateur.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="3ad0b-106">Cela est relativement simple si vous utilisez la méthode [**IVMRSurfaceAllocatorNotify9 :: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) .</span><span class="sxs-lookup"><span data-stu-id="3ad0b-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="3ad0b-107">L’exemple VMR9Allocator montre comment implémenter un Allocator-Presenter personnalisé.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="3ad0b-108">En mode exclusif DirectDraw, une application prend le contrôle exclusif du matériel graphique.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="3ad0b-109">Cela est utile pour les applications telles que les jeux, ou peut-être des applications vidéo plein écran.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="3ad0b-110">Normalement, VMR crée les objets DirectDraw et définit le niveau coopératif sur normal.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="3ad0b-111">Toutefois, pour exécuter VMR en mode exclusif DirectDraw, l’application elle-même doit créer l’objet DirectDraw et la surface principale, puis appeler **SetCooperativeLevel** pour spécifier le mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="3ad0b-112">VMR possède un Allocator-Presenter spécial qui lui permet de s’exécuter en mode exclusif DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="3ad0b-113">Pour configurer VMR afin d’utiliser cet Allocator-presenter :</span><span class="sxs-lookup"><span data-stu-id="3ad0b-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="3ad0b-114">Créez le graphique de filtre et ajoutez VMR à celui-ci à l’aide de la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) .</span><span class="sxs-lookup"><span data-stu-id="3ad0b-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="3ad0b-115">Pour obtenir un exemple de code, consultez [mode sans fenêtre VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="3ad0b-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="3ad0b-116">Créer l’allocateur en mode exclusif-présentateur :</span><span class="sxs-lookup"><span data-stu-id="3ad0b-116">Create the Exclusive Mode allocator-presenter:</span></span>
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  <span data-ttu-id="3ad0b-117">Configurer le nouvel Allocator-présentateur :</span><span class="sxs-lookup"><span data-stu-id="3ad0b-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="3ad0b-118">Branchez le nouvel Allocator-Presenter dans VMR.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="3ad0b-119">Générez le reste du graphique de filtre de la manière habituelle.</span><span class="sxs-lookup"><span data-stu-id="3ad0b-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ad0b-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ad0b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad0b-121">Modes de fonctionnement VMR</span><span class="sxs-lookup"><span data-stu-id="3ad0b-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 



