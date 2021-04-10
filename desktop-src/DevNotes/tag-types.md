---
description: Décrit le type de données de la valeur associée à une BALIse.
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: Types de BALISes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200905"
---
# <a name="tag-types"></a><span data-ttu-id="7d7e9-103">Types de BALISes</span><span class="sxs-lookup"><span data-stu-id="7d7e9-103">TAG Types</span></span>

<span data-ttu-id="7d7e9-104">Décrit le type de données de la valeur associée à une BALIse.</span><span class="sxs-lookup"><span data-stu-id="7d7e9-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="7d7e9-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="7d7e9-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="7d7e9-106">Description</span><span class="sxs-lookup"><span data-stu-id="7d7e9-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="7d7e9-107"><dt>**Balise \_ TAPEZ \_ null**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="7d7e9-108">Aucune valeur n’est associée à la BALIse.</span><span class="sxs-lookup"><span data-stu-id="7d7e9-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="7d7e9-109"><dt>**Balise \_ \_Octet de type**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="7d7e9-110">Valeur d' **octet** .</span><span class="sxs-lookup"><span data-stu-id="7d7e9-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="7d7e9-111"><dt>**Balise \_ TAPEZ \_ Word**</dt> <dt>0x3000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="7d7e9-112">Valeur de **mot** .</span><span class="sxs-lookup"><span data-stu-id="7d7e9-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="7d7e9-113"><dt>**Balise \_ TAPEZ \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="7d7e9-114">Valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7d7e9-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="7d7e9-115"><dt>**Balise \_ TAPEZ \_ QWord**</dt> <dt>0x5000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="7d7e9-116">Valeur **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="7d7e9-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="7d7e9-117"><dt>**Balise \_ TAPEZ \_ STRINGREF**</dt> <dt>0x6000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="7d7e9-118">Valeur de chaîne avec jetons.</span><span class="sxs-lookup"><span data-stu-id="7d7e9-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="7d7e9-119"><dt>**Balise \_ 0x7000 \_ liste de types**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="7d7e9-120">Liste de valeurs de BALIse.</span><span class="sxs-lookup"><span data-stu-id="7d7e9-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="7d7e9-121"><dt>**Balise \_ \_Chaîne de type**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="7d7e9-122">Valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7d7e9-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="7d7e9-123"><dt>**Balise \_ TYPE \_ binaire**</dt> <dt>0x9000</dt></span><span class="sxs-lookup"><span data-stu-id="7d7e9-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="7d7e9-124">Valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="7d7e9-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="7d7e9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d7e9-125">Requirements</span></span>



| <span data-ttu-id="7d7e9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d7e9-126">Requirement</span></span> | <span data-ttu-id="7d7e9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d7e9-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7d7e9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d7e9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d7e9-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d7e9-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7d7e9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d7e9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d7e9-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d7e9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d7e9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d7e9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7e9-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7d7e9-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="7d7e9-134">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="7d7e9-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="7d7e9-135">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="7d7e9-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




