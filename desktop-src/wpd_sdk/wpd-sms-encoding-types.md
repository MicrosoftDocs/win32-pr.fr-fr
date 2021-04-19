---
description: Le \_ \_ \_ type d’énumération des types d’encodage SMS wpd décrit le type d’encodage d’un message SMS (Short Message Service).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Énumération WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537629"
---
# <a name="wpd_sms_encoding_types-enumeration"></a><span data-ttu-id="b61ae-103">\_ \_ Énumération des types d’encodage SMS wpd \_</span><span class="sxs-lookup"><span data-stu-id="b61ae-103">WPD\_SMS\_ENCODING\_TYPES enumeration</span></span>

<span data-ttu-id="b61ae-104">Le type d’énumération des **\_ \_ \_ types d’encodage SMS wpd** décrit le type d’encodage d’un message SMS (Short Message Service).</span><span class="sxs-lookup"><span data-stu-id="b61ae-104">The **WPD\_SMS\_ENCODING\_TYPES** enumeration type describes the encoding type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="b61ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b61ae-105">Syntax</span></span>


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="b61ae-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b61ae-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b61ae-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**Encodage SMS \_ \_ 7 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="b61ae-107"><span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**SMS\_ENCODING\_7\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="b61ae-108">Encodage 7 bits.</span><span class="sxs-lookup"><span data-stu-id="b61ae-108">Seven-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="b61ae-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**Encodage SMS \_ \_ 8 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="b61ae-109"><span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**SMS\_ENCODING\_8\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="b61ae-110">Encodage 8 bits.</span><span class="sxs-lookup"><span data-stu-id="b61ae-110">Eight-bit encoding.</span></span>

</dd> <dt>

<span data-ttu-id="b61ae-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**Encodage SMS \_ \_ UTF \_ 16**</span><span class="sxs-lookup"><span data-stu-id="b61ae-111"><span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**SMS\_ENCODING\_UTF\_16**</span></span>
</dt> <dd>

<span data-ttu-id="b61ae-112">Encodage de 16 bits (UTF).</span><span class="sxs-lookup"><span data-stu-id="b61ae-112">Sixteen-bit encoding (UTF).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b61ae-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b61ae-113">Remarks</span></span>

<span data-ttu-id="b61ae-114">Cette énumération est utilisée par la propriété d' [ \_ \_ encodage SMS wpd](sms-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="b61ae-114">This enumeration is used by the [WPD\_SMS\_ENCODING](sms-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b61ae-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b61ae-115">Requirements</span></span>



| <span data-ttu-id="b61ae-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b61ae-116">Requirement</span></span> | <span data-ttu-id="b61ae-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b61ae-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b61ae-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b61ae-118">Header</span></span><br/> | <dl> <span data-ttu-id="b61ae-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b61ae-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b61ae-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b61ae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b61ae-121">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="b61ae-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




