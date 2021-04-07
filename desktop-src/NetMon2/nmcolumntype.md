---
description: Spécifie les membres de la structure NMCOLUMNVARIANT.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: NMCOLUMNTYPE, énumération (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760125"
---
# <a name="nmcolumntype-enumeration"></a><span data-ttu-id="fe241-103">Énumération NMCOLUMNTYPE</span><span class="sxs-lookup"><span data-stu-id="fe241-103">NMCOLUMNTYPE enumeration</span></span>

<span data-ttu-id="fe241-104">L’énumération **NMCOLUMNTYPE** spécifie les membres de la structure [**NMCOLUMNVARIANT**](nmcolumnvariant.md) .</span><span class="sxs-lookup"><span data-stu-id="fe241-104">The **NMCOLUMNTYPE** enumeration specifies the members of the [**NMCOLUMNVARIANT**](nmcolumnvariant.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe241-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe241-105">Syntax</span></span>


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a><span data-ttu-id="fe241-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fe241-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fe241-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE \_ UINT8**</span><span class="sxs-lookup"><span data-stu-id="fe241-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE\_UINT8**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-108">entier non signé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-108">8-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE \_ SINT8**</span><span class="sxs-lookup"><span data-stu-id="fe241-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE\_SINT8**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-110">entier signé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-110">8-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UINT16**</span><span class="sxs-lookup"><span data-stu-id="fe241-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE\_UINT16**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-112">entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-112">16-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE \_ SINT16**</span><span class="sxs-lookup"><span data-stu-id="fe241-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE\_SINT16**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-114">entier signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-114">16-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE \_ UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe241-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE\_UINT32**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-116">entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-116">32-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="fe241-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE\_SINT32**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-118">Entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-118">32-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE \_ FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="fe241-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE\_FLOAT64**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-120">virgule flottante 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fe241-120">64-bit float.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**\_Frame NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="fe241-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE\_FRAME**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-122">Numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="fe241-122">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE \_ YesNo**</span><span class="sxs-lookup"><span data-stu-id="fe241-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE\_YESNO**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-124">« Oui » ou « non ».</span><span class="sxs-lookup"><span data-stu-id="fe241-124">"Yes" or "No".</span></span>

</dd> <dt>

<span data-ttu-id="fe241-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE \_ microphone**</span><span class="sxs-lookup"><span data-stu-id="fe241-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE\_ONOFF**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-126">« On » ou « OFF »</span><span class="sxs-lookup"><span data-stu-id="fe241-126">"On" or "Off"</span></span>

</dd> <dt>

<span data-ttu-id="fe241-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE \_ truefalse**</span><span class="sxs-lookup"><span data-stu-id="fe241-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE\_TRUEFALSE**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-128">« True » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="fe241-128">"True" or "False".</span></span>

</dd> <dt>

<span data-ttu-id="fe241-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE \_ MACADDR**</span><span class="sxs-lookup"><span data-stu-id="fe241-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE\_MACADDR**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-130">Adresse MAC.</span><span class="sxs-lookup"><span data-stu-id="fe241-130">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE \_ IPXADDR**</span><span class="sxs-lookup"><span data-stu-id="fe241-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE\_IPXADDR**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-132">Adresse IPX.</span><span class="sxs-lookup"><span data-stu-id="fe241-132">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE \_ ipaddr**</span><span class="sxs-lookup"><span data-stu-id="fe241-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE\_IPADDR**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-134">Adresse IP.</span><span class="sxs-lookup"><span data-stu-id="fe241-134">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE \_ VARTIME**</span><span class="sxs-lookup"><span data-stu-id="fe241-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE\_VARTIME**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-136">Heure de la variante.</span><span class="sxs-lookup"><span data-stu-id="fe241-136">Variant time.</span></span>

</dd> <dt>

<span data-ttu-id="fe241-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_chaîne NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="fe241-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="fe241-138">Pointeur vers une chaîne.</span><span class="sxs-lookup"><span data-stu-id="fe241-138">Pointer to a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe241-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe241-139">Requirements</span></span>



| <span data-ttu-id="fe241-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe241-140">Requirement</span></span> | <span data-ttu-id="fe241-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe241-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe241-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe241-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fe241-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe241-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fe241-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe241-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fe241-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe241-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fe241-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe241-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe241-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe241-147"><dt>Netmon.h</dt></span></span> </dl> |



 

 




