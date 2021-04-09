---
title: IDXCoreAdapter::IsQueryStateSupported
description: Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge l’interrogation de la valeur de l’état de l’adaptateur spécifié.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102041"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a><span data-ttu-id="d9584-103">IDXCoreAdapter :: IsQueryStateSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="d9584-103">IDXCoreAdapter::IsQueryStateSupported method</span></span>

<span data-ttu-id="d9584-104">Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge l’interrogation de la valeur de l’état de l’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="d9584-104">Determines whether this DXCore adapter object and the current operating system (OS) support querying the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9584-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9584-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="d9584-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9584-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="d9584-107">state</span><span class="sxs-lookup"><span data-stu-id="d9584-107">state</span></span>

<span data-ttu-id="d9584-108">Type : **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="d9584-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="d9584-109">Type d’élément d’État sur lequel vous effectuez une requête sur la prise en charge de.</span><span class="sxs-lookup"><span data-stu-id="d9584-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="d9584-110">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur chaque type d’état de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="d9584-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="d9584-111">Retours</span><span class="sxs-lookup"><span data-stu-id="d9584-111">Returns</span></span>

<span data-ttu-id="d9584-112">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="d9584-112">Type: **bool**</span></span>

<span data-ttu-id="d9584-113">Retourne  `true`   si cet objet adaptateur dxcore et le système d’exploitation actuel prennent en charge l’interrogation de l’état d’adaptateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="d9584-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support querying the specified adapter state.</span></span> <span data-ttu-id="d9584-114">Sinon, retourne  `false` .</span><span class="sxs-lookup"><span data-stu-id="d9584-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9584-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9584-115">See also</span></span>

<span data-ttu-id="d9584-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="d9584-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>