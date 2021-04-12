---
description: La \_ structure MXDC S0PAGE \_ passthrough \_ Escape \_ t est une \_ structure d' \_ en-tête d’échappement MXDC \_ concaténée avec une \_ structure MXDC S0PAGE \_ Data \_ T.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Structure MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319570"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="a3604-103">\_Structure MXDC S0PAGE \_ passthrough- \_ Escape \_</span><span class="sxs-lookup"><span data-stu-id="a3604-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="a3604-104">La structure **MXDC \_ S0PAGE \_ passthrough \_ Escape \_ t** est une structure d' [**\_ \_ en-tête d’échappement MXDC \_**](mxdcescapeheader.md) concaténée avec une structure [**MXDC \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md) .</span><span class="sxs-lookup"><span data-stu-id="a3604-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3604-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3604-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="a3604-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a3604-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3604-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="a3604-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="a3604-108">Une [**structure \_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) avec son membre **opcode** défini sur **MXDCOP \_ Set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="a3604-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="a3604-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="a3604-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="a3604-110">Structure [**MxdcS0PageData**](mxdcs0pagedata.md) qui représente une page de document XPS.</span><span class="sxs-lookup"><span data-stu-id="a3604-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3604-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a3604-111">Remarks</span></span>

<span data-ttu-id="a3604-112">Cette structure est transmise dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quand elle est appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) et que le membre **opcode** de la structure T de l' [**\_ \_ en-tête \_ d’échappement MXDC**](mxdcescapeheader.md) est **MXDCOP \_ défini \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="a3604-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="a3604-113">En conséquence, Microsoft XML document Converter (MXDC) transmet la page à l’imprimante sans la traiter.</span><span class="sxs-lookup"><span data-stu-id="a3604-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="a3604-114">Allouez de la mémoire pour l’échappement comme indiqué ci-dessous, définissez les champs en fonction des besoins, puis appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="a3604-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="a3604-115">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="a3604-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="a3604-116">L’application appelante est chargée de valider le code XML de la page de document XPS.</span><span class="sxs-lookup"><span data-stu-id="a3604-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="a3604-117">La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ définir la \_ \_ ressource S0PAGE** comme **opcode** pour chaque ressource sur la page avant de l’appeler avec **MXDCOP \_ définir \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="a3604-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3604-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3604-118">Requirements</span></span>



| <span data-ttu-id="a3604-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3604-119">Requirement</span></span> | <span data-ttu-id="a3604-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3604-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a3604-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3604-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a3604-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3604-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3604-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3604-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a3604-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3604-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3604-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3604-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3604-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3604-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3604-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3604-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3604-128">Impression</span><span class="sxs-lookup"><span data-stu-id="a3604-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a3604-129">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="a3604-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="a3604-130">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3604-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a3604-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="a3604-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="a3604-132">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="a3604-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

