---
description: Le \_ \_ type d’énumération types de messages SMS décrit le type de contenu d’un message SMS (Short Message Service).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Énumération SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530468"
---
# <a name="sms_message_types-enumeration"></a><span data-ttu-id="9268a-103">\_Énumération des types de messages SMS \_</span><span class="sxs-lookup"><span data-stu-id="9268a-103">SMS\_MESSAGE\_TYPES enumeration</span></span>

<span data-ttu-id="9268a-104">Le type d’énumération **\_ \_ types de messages SMS** décrit le type de contenu d’un message SMS (Short Message Service).</span><span class="sxs-lookup"><span data-stu-id="9268a-104">The **SMS\_MESSAGE\_TYPES** enumeration type describes the content type of a short message service (SMS) message.</span></span>

## <a name="syntax"></a><span data-ttu-id="9268a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9268a-105">Syntax</span></span>


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="9268a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9268a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9268a-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ SMS \_**</span><span class="sxs-lookup"><span data-stu-id="9268a-107"><span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS\_TEXT\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="9268a-108">Message texte.</span><span class="sxs-lookup"><span data-stu-id="9268a-108">A text message.</span></span>

</dd> <dt>

<span data-ttu-id="9268a-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS \_ - \_ message binaire**</span><span class="sxs-lookup"><span data-stu-id="9268a-109"><span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**SMS\_BINARY\_MESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="9268a-110">Message binaire.</span><span class="sxs-lookup"><span data-stu-id="9268a-110">A binary message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9268a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9268a-111">Remarks</span></span>

<span data-ttu-id="9268a-112">Cette énumération est utilisée par la commande [**wpd \_ \_ SMS \_ Send**](wpd-command-sms-send-command.md).</span><span class="sxs-lookup"><span data-stu-id="9268a-112">This enumeration is used by the [**WPD\_COMMAND\_SMS\_SEND Command**](wpd-command-sms-send-command.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9268a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9268a-113">Requirements</span></span>



| <span data-ttu-id="9268a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9268a-114">Requirement</span></span> | <span data-ttu-id="9268a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9268a-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9268a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="9268a-116">Header</span></span><br/> | <dl> <span data-ttu-id="9268a-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9268a-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9268a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9268a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9268a-119">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="9268a-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




