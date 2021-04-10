---
title: DXCoreHardwareID
description: Représente les éléments d’ID de matériel PnP pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101772"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="792cd-103">DXCoreHardwareID, structure</span><span class="sxs-lookup"><span data-stu-id="792cd-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="792cd-104">Représente les éléments d’ID de matériel PnP pour un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="792cd-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="792cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="792cd-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="792cd-106">Membres</span><span class="sxs-lookup"><span data-stu-id="792cd-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="792cd-107">vendorId</span><span class="sxs-lookup"><span data-stu-id="792cd-107">vendorId</span></span>

<span data-ttu-id="792cd-108">Type : **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="792cd-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="792cd-109">ID PCI du fournisseur de matériel de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="792cd-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="792cd-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="792cd-110">deviceId</span></span>

<span data-ttu-id="792cd-111">Type : **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="792cd-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="792cd-112">ID PCI du périphérique matériel de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="792cd-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="792cd-113">subSysId</span><span class="sxs-lookup"><span data-stu-id="792cd-113">subSysId</span></span>

<span data-ttu-id="792cd-114">Type : **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="792cd-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="792cd-115">ID PCI du sous-système matériel de la carte.</span><span class="sxs-lookup"><span data-stu-id="792cd-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="792cd-116">revision</span><span class="sxs-lookup"><span data-stu-id="792cd-116">revision</span></span>

<span data-ttu-id="792cd-117">Type : **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="792cd-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="792cd-118">ID PCI du numéro de révision de la carte.</span><span class="sxs-lookup"><span data-stu-id="792cd-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="792cd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792cd-119">See also</span></span>

<span data-ttu-id="792cd-120">[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="792cd-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>