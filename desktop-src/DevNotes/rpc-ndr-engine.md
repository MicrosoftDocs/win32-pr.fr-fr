---
description: Moteur de rapport de non-remise RPC
ms.assetid: FD6365A9-6EC2-407D-B397-09A91BF02379
title: Moteur de rapport de non-remise RPC (remarques pour les développeurs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39eeb38d99e01dd8ab5683cf0289b3e7e09d45f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515777"
---
# <a name="rpc-ndr-engine-developer-notes"></a><span data-ttu-id="5ebf2-103">Moteur de rapport de non-remise RPC (remarques pour les développeurs)</span><span class="sxs-lookup"><span data-stu-id="5ebf2-103">RPC NDR Engine (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5ebf2-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5ebf2-104">In this section</span></span>

-   [<span data-ttu-id="5ebf2-105">**NdrComplexArrayBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-105">**NdrComplexArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraybuffersize)
-   [<span data-ttu-id="5ebf2-106">**NdrComplexArrayMarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-106">**NdrComplexArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraymarshall)
-   [<span data-ttu-id="5ebf2-107">**NdrComplexArrayUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-107">**NdrComplexArrayUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarrayunmarshall)
-   [<span data-ttu-id="5ebf2-108">**NdrComplexStructBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-108">**NdrComplexStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructbuffersize)
-   [<span data-ttu-id="5ebf2-109">**NdrComplexStructMarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-109">**NdrComplexStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructmarshall)
-   [<span data-ttu-id="5ebf2-110">**NdrComplexStructUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-110">**NdrComplexStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructunmarshall)
-   [<span data-ttu-id="5ebf2-111">**NdrComformantArrayBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-111">**NdrComformantArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraybuffersize)
-   [<span data-ttu-id="5ebf2-112">**NdrComformantArrayMarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-112">**NdrComformantArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraymarshall)
-   [<span data-ttu-id="5ebf2-113">**NdrSimpleStructBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-113">**NdrSimpleStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructbuffersize)
-   [<span data-ttu-id="5ebf2-114">**NdrSimpleStructMarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-114">**NdrSimpleStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructmarshall)
-   [<span data-ttu-id="5ebf2-115">**NdrSimpleStructUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-115">**NdrSimpleStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructunmarshall)
-   [<span data-ttu-id="5ebf2-116">**NdrUserMarshalUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5ebf2-116">**NdrUserMarshalUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalunmarshall)

 

 



