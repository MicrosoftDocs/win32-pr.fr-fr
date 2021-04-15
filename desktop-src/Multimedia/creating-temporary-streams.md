---
title: Création de flux temporaires
description: Création de flux temporaires
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- AVIStreamCreate fonction)
- AVIStreamRelease fonction)
- AVIMakeCompressedStream fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462183"
---
# <a name="creating-temporary-streams"></a><span data-ttu-id="f9288-106">Création de flux temporaires</span><span class="sxs-lookup"><span data-stu-id="f9288-106">Creating Temporary Streams</span></span>

<span data-ttu-id="f9288-107">Les flux temporaires peuvent être bénéfiques de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="f9288-107">Temporary streams can be beneficial in several ways.</span></span> <span data-ttu-id="f9288-108">Vous pouvez utiliser un flux temporaire comme flux de travail, par exemple, lors de la modification du format de flux.</span><span class="sxs-lookup"><span data-stu-id="f9288-108">You can use a temporary stream as a work stream, for example, when changing the stream format.</span></span> <span data-ttu-id="f9288-109">Ou vous pouvez créer un flux temporaire pour contenir des parties d’autres flux qui ont été copiés.</span><span class="sxs-lookup"><span data-stu-id="f9288-109">Or you can create a temporary stream to hold portions of other streams that have been copied.</span></span>

<span data-ttu-id="f9288-110">Vous pouvez créer un flux en mémoire qui n’est associé à aucun fichier à l’aide de la fonction [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) .</span><span class="sxs-lookup"><span data-stu-id="f9288-110">You can create a stream in memory that is not associated with any file by using the [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) function.</span></span> <span data-ttu-id="f9288-111">Cette fonction retourne l’adresse de l’interface au nouveau flux à un emplacement spécifié et est utilisée en interne par d’autres fonctions qui créent des flux temporaires.</span><span class="sxs-lookup"><span data-stu-id="f9288-111">This function returns the address of the interface to the new stream in a specified location and is used internally by other functions that create temporary streams.</span></span>

<span data-ttu-id="f9288-112">Vous pouvez créer un flux compressé à partir d’un flux non compressé à l’aide de la fonction [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) .</span><span class="sxs-lookup"><span data-stu-id="f9288-112">You can create a compressed stream from an uncompressed stream by using the [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) function.</span></span> <span data-ttu-id="f9288-113">Vous identifiez le flux à compresser, la méthode de compression et les options de compression, ainsi que le gestionnaire du nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="f9288-113">You identify the stream to compress, the compression method and compression options, and the handler for the new stream.</span></span>

<span data-ttu-id="f9288-114">Lorsque vous avez fini d’utiliser un flux créé avec **AVIStreamCreate** ou **AVIMakeCompressedStream**, fermez le flux à l’aide de la fonction [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="f9288-114">When you finish using a stream created with **AVIStreamCreate** or **AVIMakeCompressedStream**, close the stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="f9288-115">**AVIStreamRelease** libère les ressources utilisées par le flux temporaire.</span><span class="sxs-lookup"><span data-stu-id="f9288-115">**AVIStreamRelease** frees the resources the temporary stream used.</span></span>

 

 




