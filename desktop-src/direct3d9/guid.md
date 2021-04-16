---
description: Définit un GUID qui peut être utilisé dans d’autres modèles.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: Guid (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521431"
---
# <a name="guid-directx-9"></a><span data-ttu-id="c6d8a-103">Guid (DirectX 9)</span><span class="sxs-lookup"><span data-stu-id="c6d8a-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="c6d8a-104">Définit un GUID qui peut être utilisé dans d’autres modèles.</span><span class="sxs-lookup"><span data-stu-id="c6d8a-104">Defines a GUID that can be used in other templates.</span></span>

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

<span data-ttu-id="c6d8a-105">Où les paramètres forment le format de stockage binaire pour un GUID :</span><span class="sxs-lookup"><span data-stu-id="c6d8a-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="c6d8a-106">données1-valeur de données de l’entier non signé 32 bits</span><span class="sxs-lookup"><span data-stu-id="c6d8a-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="c6d8a-107">data2-valeur de données de l’entier non signé 16 bits</span><span class="sxs-lookup"><span data-stu-id="c6d8a-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="c6d8a-108">data3-valeur de données de l’entier non signé 16 bits</span><span class="sxs-lookup"><span data-stu-id="c6d8a-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="c6d8a-109">data4-un tableau de caractères non signés</span><span class="sxs-lookup"><span data-stu-id="c6d8a-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="c6d8a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6d8a-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d8a-111">Modèles</span><span class="sxs-lookup"><span data-stu-id="c6d8a-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



