---
description: Le \_ type d' \_ énumération des valeurs de type de stockage wpd \_ décrit les différents types de stockage d’appareils mobiles Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Énumération WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528757"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="b9ea8-103">\_ \_ Énumération des valeurs de type de stockage wpd \_</span><span class="sxs-lookup"><span data-stu-id="b9ea8-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="b9ea8-104">Le type d’énumération des **\_ valeurs de \_ type \_ de stockage wpd** décrit les différents types de stockage d’appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ea8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9ea8-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="b9ea8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b9ea8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b9ea8-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_type de stockage wpd \_ \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="b9ea8-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="b9ea8-108">Le stockage est d’un type non défini.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea8-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**mémoire \_ \_ fixe du type de stockage wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9ea8-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="b9ea8-110">Le stockage est non amovible et en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea8-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_type de stockage wpd \_ \_ \_ ROM amovible**</span><span class="sxs-lookup"><span data-stu-id="b9ea8-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="b9ea8-112">Le stockage est amovible et est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea8-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ RAM fixe de type de stockage wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9ea8-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="b9ea8-114">Le stockage est non amovible et prend en charge la lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="b9ea8-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ RAM amovible de type de stockage wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9ea8-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="b9ea8-116">Le stockage est amovible et prend en charge la lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9ea8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b9ea8-117">Remarks</span></span>

<span data-ttu-id="b9ea8-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b9ea8-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ea8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9ea8-119">Requirements</span></span>



| <span data-ttu-id="b9ea8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9ea8-120">Requirement</span></span> | <span data-ttu-id="b9ea8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9ea8-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ea8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9ea8-122">Header</span></span><br/> | <dl> <span data-ttu-id="b9ea8-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ea8-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ea8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9ea8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ea8-125">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="b9ea8-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




