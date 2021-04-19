---
title: IDXCoreAdapter::IsPropertySupported
description: Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge la propriété de l’adaptateur spécifiée.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106538598"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="e4c42-103">IDXCoreAdapter :: IsPropertySupported, méthode</span><span class="sxs-lookup"><span data-stu-id="e4c42-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="e4c42-104">Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge la propriété de l’adaptateur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e4c42-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4c42-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="e4c42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4c42-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="e4c42-107">propriété</span><span class="sxs-lookup"><span data-stu-id="e4c42-107">property</span></span>

<span data-ttu-id="e4c42-108">Type : **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="e4c42-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="e4c42-109">Type de propriété pour lequel vous effectuez une requête sur la prise en charge de.</span><span class="sxs-lookup"><span data-stu-id="e4c42-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="e4c42-110">Consultez le tableau dans [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) pour plus d’informations sur chaque propriété de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="e4c42-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="e4c42-111">Retours</span><span class="sxs-lookup"><span data-stu-id="e4c42-111">Returns</span></span>

<span data-ttu-id="e4c42-112">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="e4c42-112">Type: **bool**</span></span>

<span data-ttu-id="e4c42-113">Retourne  `true`   si cet objet adaptateur dxcore et le système d’exploitation actuel prennent en charge la propriété de l’adaptateur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e4c42-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="e4c42-114">Sinon, retourne  `false` .</span><span class="sxs-lookup"><span data-stu-id="e4c42-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4c42-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4c42-115">See also</span></span>

<span data-ttu-id="e4c42-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e4c42-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>