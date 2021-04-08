---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Détermine si une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) spécifiée est comprise par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728037"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="b923a-103">IDXCoreAdapterList :: IsAdapterPreferenceSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="b923a-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="b923a-104">Description</span><span class="sxs-lookup"><span data-stu-id="b923a-104">Description</span></span>

<span data-ttu-id="b923a-105">Détermine si une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) spécifiée est comprise par le système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="b923a-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="b923a-106">Vous pouvez appeler **IsAdapterPreferenceSupported** avant d’appeler [IDXCoreAdapterList :: sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="b923a-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b923a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b923a-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="b923a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b923a-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="b923a-109">preference</span><span class="sxs-lookup"><span data-stu-id="b923a-109">preference</span></span>

<span data-ttu-id="b923a-110">Type : **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="b923a-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="b923a-111">Valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) qui sera vérifiée pour déterminer si elle est prise en charge par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b923a-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="b923a-112">Retours</span><span class="sxs-lookup"><span data-stu-id="b923a-112">Returns</span></span>

<span data-ttu-id="b923a-113">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="b923a-113">Type: **bool**</span></span>

<span data-ttu-id="b923a-114">Retourne `true` si le type de tri est interprété par le système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="b923a-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="b923a-115">Sinon, retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="b923a-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="b923a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b923a-116">See also</span></span>

<span data-ttu-id="b923a-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b923a-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>