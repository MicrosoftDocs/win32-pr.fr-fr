---
description: Le \_ \_ \_ type d’énumération des valeurs d’état de rognés wpd décrit l’état de rognage d’une image.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Énumération WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531795"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="c9ebd-103">\_ \_ Énumération des valeurs d’État rognées de l’API \_</span><span class="sxs-lookup"><span data-stu-id="c9ebd-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="c9ebd-104">Le type d’énumération des **\_ valeurs d' \_ état \_ de rognés wpd** décrit l’état de rognage d’une image.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ebd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9ebd-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="c9ebd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c9ebd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c9ebd-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_État du rognage wpd \_ \_ non \_ rogné**</span><span class="sxs-lookup"><span data-stu-id="c9ebd-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="c9ebd-108">L’image n’a pas été rognée.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="c9ebd-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**\_État du rognage wpd \_ \_ rogné**</span><span class="sxs-lookup"><span data-stu-id="c9ebd-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="c9ebd-110">L’image a été rognée.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="c9ebd-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**l' \_ État du rognage wpd ne \_ \_ doit \_ pas \_ être \_ rogné**</span><span class="sxs-lookup"><span data-stu-id="c9ebd-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="c9ebd-112">L’image n’a pas été découpée et ne doit pas être rognée.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9ebd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c9ebd-113">Remarks</span></span>

<span data-ttu-id="c9ebd-114">Indique l’État rogné d’une image.</span><span class="sxs-lookup"><span data-stu-id="c9ebd-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="c9ebd-115">Cette énumération est utilisée par la propriété de l' [ \_ \_ \_ État rogné de l’image wpd](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="c9ebd-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ebd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9ebd-116">Requirements</span></span>



| <span data-ttu-id="c9ebd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9ebd-117">Requirement</span></span> | <span data-ttu-id="c9ebd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9ebd-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ebd-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9ebd-119">Header</span></span><br/> | <dl> <span data-ttu-id="c9ebd-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9ebd-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ebd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9ebd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ebd-122">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="c9ebd-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




