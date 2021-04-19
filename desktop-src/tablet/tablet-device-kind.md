---
description: Indique le type de périphérique tablette, tel qu’un crayon, une souris ou un digitaliseur tactile.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Énumération TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531403"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="71b26-103">\_Énumération de type d’appareil tablette \_</span><span class="sxs-lookup"><span data-stu-id="71b26-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="71b26-104">Indique le type de périphérique tablette, tel qu’un crayon, une souris ou un digitaliseur tactile.</span><span class="sxs-lookup"><span data-stu-id="71b26-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71b26-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="71b26-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="71b26-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="71b26-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_souris du périphérique tablette \_**</span><span class="sxs-lookup"><span data-stu-id="71b26-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="71b26-108">La tablette est une souris.</span><span class="sxs-lookup"><span data-stu-id="71b26-108">The tablet is a mouse.</span></span> <span data-ttu-id="71b26-109">Cela comprend les pavés tactiles qui se trouvent sur de nombreux ordinateurs portables.</span><span class="sxs-lookup"><span data-stu-id="71b26-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="71b26-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_stylet du périphérique tablette \_**</span><span class="sxs-lookup"><span data-stu-id="71b26-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="71b26-111">La tablette utilise un crayon et un digitaliseur électromagnétiques.</span><span class="sxs-lookup"><span data-stu-id="71b26-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="71b26-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_toucher du périphérique tablette \_**</span><span class="sxs-lookup"><span data-stu-id="71b26-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="71b26-113">La tablette utilise un digitaliseur tactile.</span><span class="sxs-lookup"><span data-stu-id="71b26-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71b26-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71b26-114">Requirements</span></span>



| <span data-ttu-id="71b26-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71b26-115">Requirement</span></span> | <span data-ttu-id="71b26-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="71b26-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="71b26-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71b26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="71b26-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71b26-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="71b26-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71b26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="71b26-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="71b26-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="71b26-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71b26-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b26-122">**ITablet2 :: GetDeviceKind, méthode**</span><span class="sxs-lookup"><span data-stu-id="71b26-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




