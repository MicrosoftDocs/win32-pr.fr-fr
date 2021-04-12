---
title: Constantes TS_CHAR_ (Textstor. h)
description: Les \_ \_ constantes char \ de TS décrivent le type de caractère.
ms.assetid: b40ca931-d45c-4101-9380-bb2b3ad25fba
topic_type:
- apiref
api_name:
- TS_CHAR_EMBEDDED
- TS_CHAR_REGION
- TS_CHAR_REPLACEMENT
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25f66006dcb37e2504785b2b28ca1f328edfcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384371"
---
# <a name="ts_char_-constants"></a><span data-ttu-id="2d25f-103">\_ \_ \* CONSTANTEs char TS</span><span class="sxs-lookup"><span data-stu-id="2d25f-103">TS\_CHAR\_\* Constants</span></span>

<span data-ttu-id="2d25f-104">Les \_ \_ \* constantes char de TS décrivent le type de caractère.</span><span class="sxs-lookup"><span data-stu-id="2d25f-104">The TS\_CHAR\_\* constants describe the type of character.</span></span>



| <span data-ttu-id="2d25f-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="2d25f-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="2d25f-106">Description</span><span class="sxs-lookup"><span data-stu-id="2d25f-106">Description</span></span>                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span id="TS_CHAR_EMBEDDED"></span><span id="ts_char_embedded"></span><dl> <span data-ttu-id="2d25f-107"><dt>**TS \_ CHAR \_ Embedded**</dt> <dt>(0xfffc)</dt></span><span class="sxs-lookup"><span data-stu-id="2d25f-107"><dt>**TS\_CHAR\_EMBEDDED**</dt> <dt>( 0xfffc )</dt></span></span> </dl>          | <span data-ttu-id="2d25f-108">Le caractère est un caractère de remplacement d’objet Unicode 2,1.</span><span class="sxs-lookup"><span data-stu-id="2d25f-108">The character is a Unicode 2.1 object-replacement character.</span></span><br/>                             |
| <span id="TS_CHAR_REGION"></span><span id="ts_char_region"></span><dl> <span data-ttu-id="2d25f-109"><dt>**TS \_ \_Zone de caractères**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="2d25f-109"><dt>**TS\_CHAR\_REGION**</dt> <dt>( 0 )</dt></span></span> </dl>                     | <span data-ttu-id="2d25f-110">Le caractère est une limite de région.</span><span class="sxs-lookup"><span data-stu-id="2d25f-110">The character is a region boundary.</span></span><br/>                                                      |
| <span id="TS_CHAR_REPLACEMENT"></span><span id="ts_char_replacement"></span><dl> <span data-ttu-id="2d25f-111"><dt>**TS \_ \_Remplacement de char**</dt> <dt>(0xFFFD)</dt></span><span class="sxs-lookup"><span data-stu-id="2d25f-111"><dt>**TS\_CHAR\_REPLACEMENT**</dt> <dt>( 0xfffd )</dt></span></span> </dl> | <span data-ttu-id="2d25f-112">Le caractère est un caractère d’espace réservé de texte masqué ou un caractère de remplacement Unicode.</span><span class="sxs-lookup"><span data-stu-id="2d25f-112">The character is a hidden-text placeholder character or a Unicode replacement character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2d25f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d25f-113">Requirements</span></span>



| <span data-ttu-id="2d25f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d25f-114">Requirement</span></span> | <span data-ttu-id="2d25f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d25f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d25f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d25f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d25f-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d25f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2d25f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d25f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d25f-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d25f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2d25f-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2d25f-120">Redistributable</span></span><br/>          | <span data-ttu-id="2d25f-121">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="2d25f-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="2d25f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d25f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d25f-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d25f-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d25f-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="2d25f-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d25f-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d25f-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d25f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d25f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d25f-127">Objets incorporés</span><span class="sxs-lookup"><span data-stu-id="2d25f-127">Embedded Objects</span></span>](embedded-objects.md)
</dt> </dl>

 

 





