---
title: Obtention des modes d’affichage de l’adaptateur
description: Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour obtenir les modes d’affichage valides associés à un adaptateur.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315209"
---
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="67415-103">Comment : obtenir les modes d’affichage de l’adaptateur</span><span class="sxs-lookup"><span data-stu-id="67415-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="67415-104">Cette rubrique montre comment utiliser Microsoft DirectX Graphics infrastructure (DXGI) pour obtenir les modes d’affichage valides associés à un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="67415-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="67415-105">DirectX 10 et 11 peuvent utiliser DXGI pour obtenir les modes d’affichage valides.</span><span class="sxs-lookup"><span data-stu-id="67415-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="67415-106">Le fait de connaître les modes d’affichage valides garantit que votre application peut choisir correctement un mode plein écran valide.</span><span class="sxs-lookup"><span data-stu-id="67415-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="67415-107">**Pour obtenir les modes d’affichage de l’adaptateur**</span><span class="sxs-lookup"><span data-stu-id="67415-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="67415-108">Créez un objet [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) et utilisez-le pour énumérer les adaptateurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="67415-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="67415-109">Pour plus d’informations, consultez [Comment : énumérer des adaptateurs](overviews-direct3d-11-devices-enum.md).</span><span class="sxs-lookup"><span data-stu-id="67415-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="67415-110">Appelez IDXGIAdapter :: EnumOutputs pour énumérer les sorties de chaque adaptateur.</span><span class="sxs-lookup"><span data-stu-id="67415-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="67415-111">Appelez IDXGIOutput :: GetDisplayModeList pour récupérer un tableau de [**structures \_ \_ desc en mode dxgi**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) et le nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="67415-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="67415-112">Chaque **structure \_ \_ desc mode dxgi** représente un mode d’affichage valide pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="67415-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="67415-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67415-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67415-114">Appareils</span><span class="sxs-lookup"><span data-stu-id="67415-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="67415-115">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="67415-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 