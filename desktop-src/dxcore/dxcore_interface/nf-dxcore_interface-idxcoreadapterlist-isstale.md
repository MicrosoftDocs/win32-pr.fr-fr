---
title: IDXCoreAdapterList::IsStale
description: Détermine si les modifications apportées à ce système ont entraîné la mise à jour de cet objet de liste d’adaptateurs DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512335"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="15939-103">IDXCoreAdapterList :: IsStale, méthode</span><span class="sxs-lookup"><span data-stu-id="15939-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="15939-104">Détermine si les modifications apportées à ce système ont entraîné la mise à jour de cet objet de liste d’adaptateurs DXCore.</span><span class="sxs-lookup"><span data-stu-id="15939-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="15939-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="15939-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15939-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15939-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="15939-107">Retours</span><span class="sxs-lookup"><span data-stu-id="15939-107">Returns</span></span>

<span data-ttu-id="15939-108">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="15939-108">Type: **bool**</span></span>

<span data-ttu-id="15939-109">Retourne  `true`   si, depuis la génération de la liste, des modifications ont été apportées aux conditions du système, ce qui entraînerait l’obsolescence de cette liste d’adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="15939-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="15939-110">Sinon, retourne  `false` .</span><span class="sxs-lookup"><span data-stu-id="15939-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="15939-111">Notes</span><span class="sxs-lookup"><span data-stu-id="15939-111">Remarks</span></span>

<span data-ttu-id="15939-112">Vous pouvez interroger **IsStale** pour déterminer si la modification des conditions système a entraîné la mise à jour de cette liste.</span><span class="sxs-lookup"><span data-stu-id="15939-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="15939-113">Si **IsStale** retourne `true` une seule fois, il retourne `true` pour la durée de vie restante de l’objet de liste d’adaptateurs dxcore.</span><span class="sxs-lookup"><span data-stu-id="15939-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="15939-114">Un objet de liste périmé est toujours considéré comme obsolète même si les conditions système retournent à un état correspondant à la liste (les mêmes conditions s’obtiennent maintenant que lors de la première génération de la liste).</span><span class="sxs-lookup"><span data-stu-id="15939-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="15939-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15939-115">See also</span></span>

<span data-ttu-id="15939-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="15939-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>