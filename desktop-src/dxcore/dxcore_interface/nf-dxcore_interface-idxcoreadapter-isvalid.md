---
title: IDXCoreAdapter::IsValid
description: Détermine si cet objet adaptateur DXCore est toujours valide.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031618"
---
# <a name="idxcoreadapterisvalid-method"></a><span data-ttu-id="e9291-103">IDXCoreAdapter :: IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="e9291-103">IDXCoreAdapter::IsValid method</span></span>

<span data-ttu-id="e9291-104">Détermine si cet objet adaptateur DXCore est toujours valide.</span><span class="sxs-lookup"><span data-stu-id="e9291-104">Determines whether this DXCore adapter object is still valid.</span></span> <span data-ttu-id="e9291-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="e9291-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9291-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9291-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a><span data-ttu-id="e9291-107">Retours</span><span class="sxs-lookup"><span data-stu-id="e9291-107">Returns</span></span>

<span data-ttu-id="e9291-108">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="e9291-108">Type: **bool**</span></span>

<span data-ttu-id="e9291-109">Retourne  `true`   si cet objet adaptateur dxcore est toujours valide.</span><span class="sxs-lookup"><span data-stu-id="e9291-109">Returns `true` if this DXCore adapter object is still valid.</span></span> <span data-ttu-id="e9291-110">Sinon, retourne  `false` .</span><span class="sxs-lookup"><span data-stu-id="e9291-110">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9291-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9291-111">See also</span></span>

<span data-ttu-id="e9291-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e9291-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>