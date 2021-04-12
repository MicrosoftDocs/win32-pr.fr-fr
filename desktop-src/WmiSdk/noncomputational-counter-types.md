---
description: Les types de compteurs non calculés n’ont pas de formule associée. La valeur brute est directement explicite.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Types de compteurs décalculés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203735"
---
# <a name="noncomputational-counter-types"></a><span data-ttu-id="aa209-104">Types de compteurs décalculés</span><span class="sxs-lookup"><span data-stu-id="aa209-104">Noncomputational Counter Types</span></span>

<span data-ttu-id="aa209-105">Les types de compteurs non calculés n’ont pas de formule associée.</span><span class="sxs-lookup"><span data-stu-id="aa209-105">Noncomputational counter types do not have an associated formula.</span></span> <span data-ttu-id="aa209-106">La valeur brute est directement explicite.</span><span class="sxs-lookup"><span data-stu-id="aa209-106">The raw value is directly meaningful.</span></span>

<span data-ttu-id="aa209-107">La propriété **FilesToBeIndexed** de la [**classe \_ \_ \_ IndexingService Win32 PerfRawData ContentIndex**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) est un exemple du type de compteur de **performance \_ \_ RAWCOUNT du compteur de performances** .</span><span class="sxs-lookup"><span data-stu-id="aa209-107">The **FilesToBeIndexed** property in the [**Win32\_PerfRawData\_ContentIndex\_IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class is an example of the **PERF\_COUNTER\_RAWCOUNT** counter type.</span></span> <span data-ttu-id="aa209-108">Il contient le nombre de fichiers qui n’ont pas été indexés.</span><span class="sxs-lookup"><span data-stu-id="aa209-108">It contains a count of files that have not been indexed.</span></span>

<span data-ttu-id="aa209-109">Les types de compteurs sont désignés par la constante définie dans Winperf. h situé dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aa209-109">Counter types are designated by the constant defined in Winperf.h located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aa209-110">Le tableau suivant répertorie les types de compteurs décalculés qui sont fournis.</span><span class="sxs-lookup"><span data-stu-id="aa209-110">The following table lists the noncomputational counter types that are provided.</span></span>



| <span data-ttu-id="aa209-111">CounterType</span><span class="sxs-lookup"><span data-stu-id="aa209-111">CounterType</span></span>                                                                                                 | <span data-ttu-id="aa209-112">Description</span><span class="sxs-lookup"><span data-stu-id="aa209-112">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa209-113">[Performances \_ \_Texte du compteur](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 2816</span><span class="sxs-lookup"><span data-stu-id="aa209-113">[PERF\_COUNTER\_TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816</span></span><br/>                | <span data-ttu-id="aa209-114">Ce type de compteur affiche une chaîne de texte de longueur variable en Unicode.</span><span class="sxs-lookup"><span data-stu-id="aa209-114">This counter type shows a variable-length text string in Unicode.</span></span> <span data-ttu-id="aa209-115">Elle n’affiche pas les valeurs calculées.</span><span class="sxs-lookup"><span data-stu-id="aa209-115">It does not display calculated values.</span></span>               |
| <span data-ttu-id="aa209-116">[Performances \_ COMPTEUR \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 65536</span><span class="sxs-lookup"><span data-stu-id="aa209-116">[PERF\_COUNTER\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536</span></span><br/>           | <span data-ttu-id="aa209-117">Valeur de compteur brute qui ne nécessite pas de calculs, et représente un échantillon qui est la dernière valeur observée uniquement.</span><span class="sxs-lookup"><span data-stu-id="aa209-117">Raw counter value that does not require calculations, and represents one sample which is the last observed value only.</span></span> |
| <span data-ttu-id="aa209-118">[Performances \_ COUNTER \_ \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span><span class="sxs-lookup"><span data-stu-id="aa209-118">[PERF\_COUNTER\_LARGE\_RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792</span></span><br/>    | <span data-ttu-id="aa209-119">Identique au **compteur de performances \_ \_ RAWCOUNT**, mais une représentation 64 bits pour les valeurs plus élevées.</span><span class="sxs-lookup"><span data-stu-id="aa209-119">Same as **PERF\_COUNTER\_RAWCOUNT**, but a 64-bit representation for larger values.</span></span>                                    |
| <span data-ttu-id="aa209-120">[Performances \_ COMPTEUR \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span><span class="sxs-lookup"><span data-stu-id="aa209-120">[PERF\_COUNTER\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0</span></span><br/>                  | <span data-ttu-id="aa209-121">Valeur la plus récemment observée au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="aa209-121">Most recently observed value in hexadecimal format.</span></span> <span data-ttu-id="aa209-122">Il n'affiche pas une moyenne.</span><span class="sxs-lookup"><span data-stu-id="aa209-122">It does not display an average.</span></span>                                    |
| <span data-ttu-id="aa209-123">[Performances \_ COUNTER \_ grand \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 256</span><span class="sxs-lookup"><span data-stu-id="aa209-123">[PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256</span></span><br/> | <span data-ttu-id="aa209-124">Identique au **compteur de performances \_ \_ RAWCOUNT \_ Hex**, mais une représentation 64 bits au format hexadécimal pour une utilisation avec des valeurs élevées.</span><span class="sxs-lookup"><span data-stu-id="aa209-124">Same as **PERF\_COUNTER\_RAWCOUNT\_HEX**, but a 64-bit representation in hexadecimal for use with large values.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa209-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa209-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa209-126">Types de compteurs de performance WMI</span><span class="sxs-lookup"><span data-stu-id="aa209-126">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

