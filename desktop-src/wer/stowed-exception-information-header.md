---
title: Structure STOWED_EXCEPTION_INFORMATION_HEADER
description: Contient des informations qui identifient la structure parente.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER structure Rapport d’erreurs Windows
- Pointeur de structure PSTOWED_EXCEPTION_INFORMATION_HEADER Rapport d’erreurs Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033168"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="bd5e8-105">Structure d' \_ \_ \_ en-tête d’informations d’exception arrimé</span><span class="sxs-lookup"><span data-stu-id="bd5e8-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="bd5e8-106">Contient des informations qui identifient la structure parente.</span><span class="sxs-lookup"><span data-stu-id="bd5e8-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd5e8-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="bd5e8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bd5e8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd5e8-109">**Taille**</span><span class="sxs-lookup"><span data-stu-id="bd5e8-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="bd5e8-110">Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd5e8-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bd5e8-111">Taille, en octets, de la structure parente.</span><span class="sxs-lookup"><span data-stu-id="bd5e8-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="bd5e8-112">**Signature**</span><span class="sxs-lookup"><span data-stu-id="bd5e8-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="bd5e8-113">Type : **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd5e8-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="bd5e8-114">Valeur 32 bits qui spécifie la signature de la structure parente.</span><span class="sxs-lookup"><span data-stu-id="bd5e8-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="bd5e8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd5e8-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="bd5e8-116">Signification</span><span class="sxs-lookup"><span data-stu-id="bd5e8-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="bd5e8-117"><dt>**Rangé \_ \_Informations sur l’exception \_ v1 \_ signature**</dt> <dt>'SE01 '</dt></span><span class="sxs-lookup"><span data-stu-id="bd5e8-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="bd5e8-118">Cette valeur indique que le parent est une structure d’informations d’exception de l' **arrimage \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="bd5e8-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="bd5e8-119"><dt>**Rangé \_ \_Informations sur l’exception \_ v2 \_ signature**</dt> <dt>'SE02 '</dt></span><span class="sxs-lookup"><span data-stu-id="bd5e8-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="bd5e8-120">Cette valeur indique que le parent est une structure d' [**informations d’exception Alrangée \_ \_ \_ v2**](stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="bd5e8-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd5e8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bd5e8-121">Remarks</span></span>

<span data-ttu-id="bd5e8-122">[**Rangé \_ Les \_ informations \_ sur l’exception v2**](stowed-exception-information-v2.md) et l' **\_ \_ \_ en-tête d’informations d’exception arrimées** ne sont actuellement pas définis dans un en-tête disponible publiquement. vous devez donc les définir dans votre code source avant de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="bd5e8-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="bd5e8-123">La structure d’informations d’exception de la version **\_ \_ \_ v1** est identique à cette structure, sauf qu’elle ne contient pas les membres **NestedExceptionType** et **NestedException** .</span><span class="sxs-lookup"><span data-stu-id="bd5e8-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5e8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd5e8-124">Requirements</span></span>



| <span data-ttu-id="bd5e8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd5e8-125">Requirement</span></span> | <span data-ttu-id="bd5e8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd5e8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="bd5e8-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5e8-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd5e8-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bd5e8-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5e8-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd5e8-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bd5e8-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd5e8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd5e8-132"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="bd5e8-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5e8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd5e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5e8-134">**Informations sur les exceptions bacalées \_ \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="bd5e8-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

