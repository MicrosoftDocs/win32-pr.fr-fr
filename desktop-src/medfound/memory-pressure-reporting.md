---
description: La création de rapports sur la sollicitation de la mémoire permet à une application Direct3D de déterminer quand sa plage de travail de la mémoire vidéo est devenue trop importante.
ms.assetid: 3aa2f81e-81a1-40a3-ad24-72781d36f713
title: Rapport de sollicitation de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d380a4c9f88fca3d25eebfcfaf67759226ab040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519007"
---
# <a name="memory-pressure-reporting"></a><span data-ttu-id="38fcd-103">Rapport de sollicitation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="38fcd-103">Memory Pressure Reporting</span></span>

<span data-ttu-id="38fcd-104">La création de rapports sur la sollicitation de la mémoire permet à une application Direct3D de déterminer quand sa plage de travail de la mémoire vidéo est devenue trop importante.</span><span class="sxs-lookup"><span data-stu-id="38fcd-104">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span>

<span data-ttu-id="38fcd-105">La *sollicitation* de la mémoire est la demande placée sur le sous-système de mémoire par une application.</span><span class="sxs-lookup"><span data-stu-id="38fcd-105">*Memory pressure* is the demand placed on the memory subsystem by an application.</span></span> <span data-ttu-id="38fcd-106">Si une application Direct3D peut utiliser la création de rapports de sollicitation de la mémoire, cette fonctionnalité est particulièrement utile pour les applications qui affichent des vidéos à l’aide de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="38fcd-106">While any Direct3D application can use memory pressure reporting, this feature is especially useful for applications that render video by using Direct3D.</span></span> <span data-ttu-id="38fcd-107">La lecture vidéo tire généralement parti de grandes quantités de mémoire tampon, afin que les frames puissent être décodés à l’avance.</span><span class="sxs-lookup"><span data-stu-id="38fcd-107">Video playback typically benefits from large amounts of buffering, so that frames can be decoded in advance.</span></span> <span data-ttu-id="38fcd-108">Si la mise en mémoire tampon entraîne généralement une lecture plus lisse, elle peut en fait dégrader les performances si la plage de travail devient trop volumineuse, en raison des facteurs suivants :</span><span class="sxs-lookup"><span data-stu-id="38fcd-108">While buffering generally results in smoother playback, it can actually degrade performance if the working set grows too large, due to the following factors:</span></span>

-   <span data-ttu-id="38fcd-109">La mémoire peut être expulsée du cache.</span><span class="sxs-lookup"><span data-stu-id="38fcd-109">Memory might be evicted from the cache.</span></span> <span data-ttu-id="38fcd-110">Dans le pire des cas, cela peut se produire sur chaque image vidéo.</span><span class="sxs-lookup"><span data-stu-id="38fcd-110">In the worst case, this can occur on every video frame.</span></span>
-   <span data-ttu-id="38fcd-111">Les allocations de mémoire peuvent être placées dans des segments de mémoire non optimaux.</span><span class="sxs-lookup"><span data-stu-id="38fcd-111">Memory allocations might be placed in nonoptimal memory segments.</span></span>

<span data-ttu-id="38fcd-112">À compter de Windows 7, Direct3D peut signaler des statistiques sur la sollicitation de la mémoire vidéo :</span><span class="sxs-lookup"><span data-stu-id="38fcd-112">Starting in Windows 7, Direct3D can report some statistics about the video memory pressure:</span></span>

-   <span data-ttu-id="38fcd-113">Nombre d’octets évincés par le processus sur un intervalle de temps.</span><span class="sxs-lookup"><span data-stu-id="38fcd-113">The number of bytes evicted by the process over an interval of time.</span></span>
-   <span data-ttu-id="38fcd-114">Quantité de mémoire placée dans des segments de mémoire non optimaux.</span><span class="sxs-lookup"><span data-stu-id="38fcd-114">The amount of memory placed in nonoptimal memory segments.</span></span>
-   <span data-ttu-id="38fcd-115">Une indication approximative de l’efficacité globale des allocations de mémoire placées dans une mémoire non optimale.</span><span class="sxs-lookup"><span data-stu-id="38fcd-115">A rough indication of the overall efficiency of the memory allocations placed in nonoptimal memory.</span></span>

<span data-ttu-id="38fcd-116">Ces informations peuvent aider une application à conserver une plage de travail raisonnable.</span><span class="sxs-lookup"><span data-stu-id="38fcd-116">This information can help an application to maintain a reasonable working set.</span></span>

## <a name="using-memory-pressure-reporting"></a><span data-ttu-id="38fcd-117">Utilisation des rapports de sollicitation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="38fcd-117">Using Memory Pressure Reporting</span></span>

<span data-ttu-id="38fcd-118">La signalisation de sollicitation de la mémoire utilise l’interface **IDirect3DQuery9** existante pour interroger l’appareil.</span><span class="sxs-lookup"><span data-stu-id="38fcd-118">Memory pressure reporting uses the existing **IDirect3DQuery9** interface to query the device.</span></span> <span data-ttu-id="38fcd-119">Un nouveau type de requête a été ajouté à l’énumération **D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="38fcd-119">A new query type has been added to the **D3DQUERYTYPE** enumeration.</span></span>


```C++
D3DQUERYTYPE_MEMORYPRESSURE        = 19,
```



<span data-ttu-id="38fcd-120">Pour utiliser cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="38fcd-120">To use this query, perform the following steps:</span></span>

1.  <span data-ttu-id="38fcd-121">Appelez **IDirect3DDevice9Ex :: CreateQuery** avec l' **indicateur \_ MEMORYPRESSURE D3DQUERYTYPE** .</span><span class="sxs-lookup"><span data-stu-id="38fcd-121">Call **IDirect3DDevice9Ex::CreateQuery** with the **D3DQUERYTYPE\_MEMORYPRESSURE** flag.</span></span> <span data-ttu-id="38fcd-122">Cette méthode retourne un pointeur vers l’interface **IDirect3DQuery9** .</span><span class="sxs-lookup"><span data-stu-id="38fcd-122">This method returns a pointer to the **IDirect3DQuery9** interface.</span></span>
2.  <span data-ttu-id="38fcd-123">Appelez **IDirect3DQuery9 :: issue** avec l’indicateur de **\_ début D3DISSUE** pour commencer l’intervalle de mesure.</span><span class="sxs-lookup"><span data-stu-id="38fcd-123">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_BEGIN** flag to begin the measurement interval.</span></span>
3.  <span data-ttu-id="38fcd-124">Appelez **IDirect3DQuery9 :: issue** avec l’indicateur de **\_ fin D3DISSUE** .</span><span class="sxs-lookup"><span data-stu-id="38fcd-124">Call **IDirect3DQuery9::Issue** with the **D3DISSUE\_END** flag.</span></span>
4.  <span data-ttu-id="38fcd-125">Appelez **IDirect3DQuery9 :: GetData** pour obtenir le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="38fcd-125">Call **IDirect3DQuery9::GetData** to get the query result.</span></span> <span data-ttu-id="38fcd-126">La requête retourne une structure [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .</span><span class="sxs-lookup"><span data-stu-id="38fcd-126">The query returns a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

## <a name="example-code"></a><span data-ttu-id="38fcd-127">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="38fcd-127">Example Code</span></span>

<span data-ttu-id="38fcd-128">L’exemple suivant montre deux fonctions qui mesurent la sollicitation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="38fcd-128">The following example shows two functions that measure memory pressure.</span></span> <span data-ttu-id="38fcd-129">Le premier commence l’intervalle de mesure, tandis que le second extrait les résultats de la mesure.</span><span class="sxs-lookup"><span data-stu-id="38fcd-129">The first begins the measurement interval, and the second retrieves the results of the measurement.</span></span>


```C++
HRESULT BeginMemoryPressureQuery(
    IDirect3DDevice9Ex *pDevice, 
    IDirect3DQuery9 **ppQuery
    )
{
    HRESULT hr = pDevice->CreateQuery(D3DQUERYTYPE_MEMORYPRESSURE, ppQuery);

    if (SUCCEEDED(hr))
    {
        hr = (*ppQuery)->Issue(D3DISSUE_BEGIN);
        if (FAILED(hr))
        {
            (*ppQuery)->Release();
            *ppQuery = NULL;
        }
    }
    return hr;
}

HRESULT EndMemoryPressureQuery(
    IDirect3DQuery9 *pQuery, 
    D3DMEMORYPRESSURE *pResult
    )
{
    HRESULT hr = pQuery->Issue(D3DISSUE_END);
    if (SUCCEEDED(hr))
    {
        hr = pQuery->GetData(pResult, sizeof(*pResult), D3DGETDATA_FLUSH);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="38fcd-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38fcd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38fcd-131">API vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="38fcd-131">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 



