---
description: Le \_ \_ \_ \_ type d’énumération des valeurs d’état de couleur wpd corrigées décrit l’état de correction de couleur d’un fichier image ou vidéo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Énumération WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528921"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="7b23a-103">\_ \_ \_ Énumération des valeurs d’État corrigées de couleurs wpd \_</span><span class="sxs-lookup"><span data-stu-id="7b23a-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="7b23a-104">Le type d’énumération des **\_ valeurs d’état de couleur wpd \_ corrigées \_ \_** décrit l’état de correction de couleur d’un fichier image ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="7b23a-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b23a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b23a-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="7b23a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7b23a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7b23a-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_État corrigé de la couleur wpd \_ corrigé \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7b23a-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="7b23a-108">La couleur de l’image n’a pas été corrigée.</span><span class="sxs-lookup"><span data-stu-id="7b23a-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="7b23a-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**\_ \_ État corrigé de la couleur \_ \_ wpd corrigé**</span><span class="sxs-lookup"><span data-stu-id="7b23a-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="7b23a-110">La couleur de l’image a été corrigée.</span><span class="sxs-lookup"><span data-stu-id="7b23a-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="7b23a-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**l' \_ État de la couleur wpd \_ corrigé \_ \_ \_ ne doit pas \_ être \_ corrigé**</span><span class="sxs-lookup"><span data-stu-id="7b23a-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="7b23a-112">L’image n’a pas été et ne doit pas être corrigée.</span><span class="sxs-lookup"><span data-stu-id="7b23a-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b23a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7b23a-113">Remarks</span></span>

<span data-ttu-id="7b23a-114">Indique l’état de couleur corrigé d’une image.</span><span class="sxs-lookup"><span data-stu-id="7b23a-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="7b23a-115">Cette énumération est utilisée par la propriété de l' [ \_ \_ \_ \_ État couleur corrigée de l’image wpd](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="7b23a-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b23a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b23a-116">Requirements</span></span>



| <span data-ttu-id="7b23a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b23a-117">Requirement</span></span> | <span data-ttu-id="7b23a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b23a-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b23a-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b23a-119">Header</span></span><br/> | <dl> <span data-ttu-id="7b23a-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b23a-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b23a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b23a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b23a-122">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="7b23a-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




