---
description: Récupère le type d’appareil matériel WIA (Windows Image Acquisition).
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo. type, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520383"
---
# <a name="deviceinfotype-property"></a><span data-ttu-id="d8114-103">DeviceInfo. type, propriété</span><span class="sxs-lookup"><span data-stu-id="d8114-103">DeviceInfo.Type property</span></span>

<span data-ttu-id="d8114-104">Récupère le type d’appareil matériel WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="d8114-104">Retrieves the type of Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="d8114-105">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8114-105">Possible values are:</span></span>

-   <span data-ttu-id="d8114-106">DigitalCamera</span><span class="sxs-lookup"><span data-stu-id="d8114-106">DigitalCamera</span></span>
-   <span data-ttu-id="d8114-107">Scanneur</span><span class="sxs-lookup"><span data-stu-id="d8114-107">Scanner</span></span>
-   <span data-ttu-id="d8114-108">StreamingVideo</span><span class="sxs-lookup"><span data-stu-id="d8114-108">StreamingVideo</span></span>
-   <span data-ttu-id="d8114-109">Default</span><span class="sxs-lookup"><span data-stu-id="d8114-109">Default</span></span>

<span data-ttu-id="d8114-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d8114-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8114-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8114-111">Syntax</span></span>


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a><span data-ttu-id="d8114-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d8114-112">Property value</span></span>

<span data-ttu-id="d8114-113">Chaîne qui reçoit l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d8114-113">String that receives the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8114-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8114-114">Requirements</span></span>



| <span data-ttu-id="d8114-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8114-115">Requirement</span></span> | <span data-ttu-id="d8114-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8114-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8114-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8114-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d8114-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8114-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8114-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8114-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d8114-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8114-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d8114-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d8114-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8114-122"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d8114-122"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




