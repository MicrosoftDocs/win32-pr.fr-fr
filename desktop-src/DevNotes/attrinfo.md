---
description: Contient les données d’attribut d’un fichier.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: ATTRINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847013"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="5cf24-103">ATTRINFO, structure</span><span class="sxs-lookup"><span data-stu-id="5cf24-103">ATTRINFO structure</span></span>

<span data-ttu-id="5cf24-104">Contient les données d’attribut d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="5cf24-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cf24-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="5cf24-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5cf24-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5cf24-107">**tAttrID**</span><span class="sxs-lookup"><span data-stu-id="5cf24-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="5cf24-108">Type d'attribut.</span><span class="sxs-lookup"><span data-stu-id="5cf24-108">The attribute type.</span></span> <span data-ttu-id="5cf24-109">Consultez [types de balises](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="5cf24-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cf24-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="5cf24-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5cf24-111">Indicateurs de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="5cf24-111">The flags for this attribute.</span></span>



| <span data-ttu-id="5cf24-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cf24-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="5cf24-113">Signification</span><span class="sxs-lookup"><span data-stu-id="5cf24-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="5cf24-114"><dt>**Attribut \_ DISPONIBLE**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5cf24-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5cf24-115">L’attribut est disponible.</span><span class="sxs-lookup"><span data-stu-id="5cf24-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="5cf24-116"><dt>**Attribut \_ ÉCHEC**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5cf24-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="5cf24-117">L’appel a échoué, car l’attribut n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="5cf24-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5cf24-118">**ullAttr**</span><span class="sxs-lookup"><span data-stu-id="5cf24-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="5cf24-119">Valeur **QWord** (si le type de balise **est \_ type \_ de balise QWord**).</span><span class="sxs-lookup"><span data-stu-id="5cf24-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="5cf24-120">**dwAttr**</span><span class="sxs-lookup"><span data-stu-id="5cf24-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="5cf24-121">Valeur **DWORD** (si le type de balise **est \_ \_ DWORD type de balise**).</span><span class="sxs-lookup"><span data-stu-id="5cf24-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="5cf24-122">**lpAttr**</span><span class="sxs-lookup"><span data-stu-id="5cf24-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="5cf24-123">Pointeur vers une chaîne (si le type de balise est le **type de balise \_ \_ STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="5cf24-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5cf24-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cf24-124">Requirements</span></span>



| <span data-ttu-id="5cf24-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cf24-125">Requirement</span></span> | <span data-ttu-id="5cf24-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cf24-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cf24-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cf24-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf24-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cf24-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cf24-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cf24-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf24-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cf24-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cf24-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf24-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf24-132">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="5cf24-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="5cf24-133">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="5cf24-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="5cf24-134">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="5cf24-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




