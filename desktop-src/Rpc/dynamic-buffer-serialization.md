---
title: Sérialisation de mémoire tampon dynamique
description: Lors de l’utilisation du style de mémoire tampon dynamique de la sérialisation, la mémoire tampon de marshaling est allouée par le stub, et les données sont encodées dans cette mémoire tampon et retournées. Lors du démarshaling, vous fournissez la mémoire tampon qui contient les données.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462215"
---
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="8e126-104">Sérialisation de mémoire tampon dynamique</span><span class="sxs-lookup"><span data-stu-id="8e126-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="8e126-105">Lors de l’utilisation du style de mémoire tampon dynamique de la sérialisation, la mémoire tampon de marshaling est allouée par le stub, et les données sont encodées dans cette mémoire tampon et retournées.</span><span class="sxs-lookup"><span data-stu-id="8e126-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="8e126-106">Lors du démarshaling, vous fournissez la mémoire tampon qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="8e126-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="8e126-107">Le style de mémoire tampon dynamique de la sérialisation utilise les routines suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e126-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="8e126-108">**MesEncodeDynBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="8e126-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="8e126-109">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="8e126-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="8e126-110">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="8e126-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="8e126-111">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="8e126-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="8e126-112">La fonction [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) alloue la mémoire nécessaire pour le handle d’encodage, puis l’initialise.</span><span class="sxs-lookup"><span data-stu-id="8e126-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="8e126-113">L’application peut appeler [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) pour réinitialiser le descripteur.</span><span class="sxs-lookup"><span data-stu-id="8e126-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="8e126-114">Elle appelle [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) pour libérer la mémoire du handle.</span><span class="sxs-lookup"><span data-stu-id="8e126-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="8e126-115">Pour créer un descripteur de décodage correspondant au handle d’encodage de mémoire tampon dynamique, utilisez [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="8e126-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




