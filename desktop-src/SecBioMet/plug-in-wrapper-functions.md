---
title: Fonctions wrapper de plug-in
description: Fonctions wrapper qui vous permettent d’appeler une fonction publique sur n’importe quel adaptateur attaché au pipeline sans acquérir manuellement un pointeur vers l’adaptateur.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- API de Windows Biometric Framework API Windows Biometric Framework, fonctions wrapper de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840594"
---
# <a name="plug-in-wrapper-functions"></a><span data-ttu-id="97e14-104">Fonctions wrapper de plug-in</span><span class="sxs-lookup"><span data-stu-id="97e14-104">Plug-in Wrapper Functions</span></span>

<span data-ttu-id="97e14-105">L’API Windows Biometric Framework comprend des fonctions wrapper qui vous permettent d’appeler une fonction publique sur n’importe quel adaptateur attaché au pipeline sans avoir à acquérir manuellement un pointeur vers l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="97e14-105">The Windows Biometric Framework API includes wrapper functions that allow you to call a public function on any adapter attached to the pipeline without manually acquiring a pointer to the adapter.</span></span> <span data-ttu-id="97e14-106">Chaque Wrapper vérifie les arguments d’entrée, récupère un pointeur d’adaptateur et appelle la fonction demandée.</span><span class="sxs-lookup"><span data-stu-id="97e14-106">Each wrapper checks the input arguments, retrieves an adapter pointer, and calls the requested function.</span></span> <span data-ttu-id="97e14-107">Par exemple, le wrapper **WbioEngineSetHashAlgorithm** a la signature suivante.</span><span class="sxs-lookup"><span data-stu-id="97e14-107">For example, the **WbioEngineSetHashAlgorithm** wrapper has the following signature.</span></span>


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



<span data-ttu-id="97e14-108">La fonction vérifie que l’argument de *pipeline* n’est pas **null**, qu’il existe un adaptateur de moteur et que la fonction [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) existe.</span><span class="sxs-lookup"><span data-stu-id="97e14-108">The function verifies that the *Pipeline* argument is not **NULL**, that an engine adapter exists, and that the [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) function exists.</span></span> <span data-ttu-id="97e14-109">Toutes les fonctions wrapper sont définies dans le \_ fichier d’en-tête WinBio adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97e14-109">All wrapper functions are defined in the Winbio\_adapter.h header file.</span></span> <span data-ttu-id="97e14-110">Les rubriques suivantes décrivent les wrappers disponibles.</span><span class="sxs-lookup"><span data-stu-id="97e14-110">The following topics discuss the available wrappers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="97e14-111">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="97e14-111">In this section</span></span>



| <span data-ttu-id="97e14-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="97e14-112">Topic</span></span>                                                               | <span data-ttu-id="97e14-113">Description</span><span class="sxs-lookup"><span data-stu-id="97e14-113">Description</span></span>                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97e14-114">Wrappers d’adaptateur de moteur</span><span class="sxs-lookup"><span data-stu-id="97e14-114">Engine Adapter Wrappers</span></span>](engine-adapter-wrappers.md)<br/>   | <span data-ttu-id="97e14-115">Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de moteur.</span><span class="sxs-lookup"><span data-stu-id="97e14-115">Functions that you can use to call functions on your engine adapter.</span></span> <span data-ttu-id="97e14-116">Ces fonctions sont définies dans WinBio \_ adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97e14-116">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="97e14-117">Wrappers d’adaptateur de capteur</span><span class="sxs-lookup"><span data-stu-id="97e14-117">Sensor Adapter Wrappers</span></span>](sensor-adapter-wrappers.md)<br/>   | <span data-ttu-id="97e14-118">Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de capteur.</span><span class="sxs-lookup"><span data-stu-id="97e14-118">Functions that you can use to call functions on your sensor adapter.</span></span> <span data-ttu-id="97e14-119">Ces fonctions sont définies dans WinBio \_ adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97e14-119">These functions are defined in Winbio\_adapter.h.</span></span><br/>  |
| [<span data-ttu-id="97e14-120">Wrappers d’adaptateur de stockage</span><span class="sxs-lookup"><span data-stu-id="97e14-120">Storage Adapter Wrappers</span></span>](storage-adapter-wrappers.md)<br/> | <span data-ttu-id="97e14-121">Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de stockage.</span><span class="sxs-lookup"><span data-stu-id="97e14-121">Functions that you can use to call functions on your storage adapter.</span></span> <span data-ttu-id="97e14-122">Ces fonctions sont définies dans WinBio \_ adapter. h.</span><span class="sxs-lookup"><span data-stu-id="97e14-122">These functions are defined in Winbio\_adapter.h.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="97e14-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97e14-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97e14-124">Référence du plug-in</span><span class="sxs-lookup"><span data-stu-id="97e14-124">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> </dl>

 

 





