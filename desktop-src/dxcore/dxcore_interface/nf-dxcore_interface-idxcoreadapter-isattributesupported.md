---
title: IDXCoreAdapter::IsAttributeSupported
description: Détermine si cet objet adaptateur DXCore prend en charge l’attribut d’adaptateur spécifié.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382100"
---
# <a name="idxcoreadapterisattributesupported-method"></a><span data-ttu-id="a97ca-103">IDXCoreAdapter :: IsAttributeSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="a97ca-103">IDXCoreAdapter::IsAttributeSupported method</span></span>

<span data-ttu-id="a97ca-104">Détermine si cet objet adaptateur DXCore prend en charge l’attribut d’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a97ca-104">Determines whether this DXCore adapter object supports the specified adapter attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a97ca-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a><span data-ttu-id="a97ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a97ca-106">Parameters</span></span>

### <a name="attributeguid"></a><span data-ttu-id="a97ca-107">attributeGUID</span><span class="sxs-lookup"><span data-stu-id="a97ca-107">attributeGUID</span></span>

<span data-ttu-id="a97ca-108">Type : **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="a97ca-108">Type: **REFGUID**</span></span>

<span data-ttu-id="a97ca-109">Référence à un GUID d’attribut d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="a97ca-109">A reference to an adapter attribute GUID.</span></span> <span data-ttu-id="a97ca-110">Pour obtenir la liste des GUID d’attribut, consultez [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="a97ca-110">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span>

## <a name="returns"></a><span data-ttu-id="a97ca-111">Retours</span><span class="sxs-lookup"><span data-stu-id="a97ca-111">Returns</span></span>

<span data-ttu-id="a97ca-112">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="a97ca-112">Type: **bool**</span></span>

<span data-ttu-id="a97ca-113">Retourne  `true`   si cet objet adaptateur dxcore prend en charge l’attribut d’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a97ca-113">Returns `true` if this DXCore adapter object supports the specified adapter attribute.</span></span> <span data-ttu-id="a97ca-114">Sinon, retourne  `false` .</span><span class="sxs-lookup"><span data-stu-id="a97ca-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a97ca-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a97ca-115">See also</span></span>

<span data-ttu-id="a97ca-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a97ca-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>