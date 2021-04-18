---
title: Structure BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: L’BITS_FILE_PROPERTY_VALUE Union fournit la valeur de la propriété du fichier DO en fonction d’une valeur de l’énumération BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Structure BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512546"
---
# <a name="bits_file_property_value-structure"></a><span data-ttu-id="fe2ad-104">Structure BITS_FILE_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="fe2ad-104">BITS_FILE_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="fe2ad-105">L' **BITS_FILE_PROPERTY_VALUE** Union fournit la valeur de la propriété du fichier do en fonction d’une valeur de l’énumération [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2ad-105">The **BITS_FILE_PROPERTY_VALUE** union provides the property value of the DO file based on a value from the [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2ad-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe2ad-106">Syntax</span></span>


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="fe2ad-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fe2ad-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe2ad-108">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="fe2ad-108">**String**</span></span>
</dt> <dd>

<span data-ttu-id="fe2ad-109">Cette valeur est utilisée lors de l’utilisation de la valeur enum de l’ID de propriété **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span><span class="sxs-lookup"><span data-stu-id="fe2ad-109">This value is used when using the property ID enum value **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe2ad-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe2ad-110">Requirements</span></span>



| <span data-ttu-id="fe2ad-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe2ad-111">Requirement</span></span> | <span data-ttu-id="fe2ad-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe2ad-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2ad-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe2ad-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fe2ad-114">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe2ad-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fe2ad-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe2ad-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fe2ad-116">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe2ad-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe2ad-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe2ad-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe2ad-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe2ad-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe2ad-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe2ad-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2ad-120">**BITS_FILE_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="fe2ad-120">**BITS_FILE_PROPERTY_ID**</span></span>](bits-file-property-id-.md)
</dt> <dt>

[<span data-ttu-id="fe2ad-121">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="fe2ad-121">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[<span data-ttu-id="fe2ad-122">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="fe2ad-122">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





