---
description: Contient des données de jeu d’animations.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033748"
---
# <a name="compressedanimationset"></a><span data-ttu-id="3b501-103">CompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="3b501-103">CompressedAnimationSet</span></span>

<span data-ttu-id="3b501-104">Contient des données de jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="3b501-104">Contains animation set data.</span></span>

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

<span data-ttu-id="3b501-105">Où :</span><span class="sxs-lookup"><span data-stu-id="3b501-105">Where:</span></span>

-   <span data-ttu-id="3b501-106">CompressedBlockSize : taille totale, en octets, des données compressées dans le tampon de données d’animation d’image clé compressée.</span><span class="sxs-lookup"><span data-stu-id="3b501-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="3b501-107">TicksPerSec : nombre de battements d’image clé d’animation qui se produisent par seconde.</span><span class="sxs-lookup"><span data-stu-id="3b501-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="3b501-108">PlaybackType : type de la boucle de lecture du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="3b501-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="3b501-109">Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="3b501-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="3b501-110">BufferLength : taille minimale de la mémoire tampon, en octets, nécessaire pour contenir les données d’animation d’image clé compressées.</span><span class="sxs-lookup"><span data-stu-id="3b501-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="3b501-111">La valeur est égale à ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="3b501-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="3b501-112">CompressedData \[ BufferLength \] : tableau de valeurs de données compressées.</span><span class="sxs-lookup"><span data-stu-id="3b501-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b501-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b501-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b501-114">Modèles</span><span class="sxs-lookup"><span data-stu-id="3b501-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="3b501-115">**XFILECOMPRESSEDANIMATIONSET**</span><span class="sxs-lookup"><span data-stu-id="3b501-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
