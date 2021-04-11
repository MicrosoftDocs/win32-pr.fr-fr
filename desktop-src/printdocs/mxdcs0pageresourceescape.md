---
description: La \_ \_ structure d’échappement de la ressource MXDC S0PAGE \_ \_ est \_ une \_ structure d’en-tête d’échappement MXDC \_ concaténée avec une \_ \_ structure de ressource t MXDC XPS S0PAGE \_ \_ .
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Structure MXDC_S0PAGE_RESOURCE_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202808"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="c3956-103">Structure de l’échappement de la \_ ressource MXDC S0PAGE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c3956-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="c3956-104">La structure d’échappement de la **\_ ressource MXDC S0PAGE \_ \_ \_** est une structure d' [**\_ \_ en-tête d’échappement \_ MXDC**](mxdcescapeheader.md) concaténée avec une structure de [**\_ \_ \_ ressource \_ t MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="c3956-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3956-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3956-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="c3956-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c3956-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3956-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="c3956-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="c3956-108">Une [**structure \_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) avec son membre **opcode** défini sur MXDCOP \_ définir \_ S0PAGE \_ ressource.</span><span class="sxs-lookup"><span data-stu-id="c3956-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="c3956-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="c3956-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="c3956-110">Structure [**de \_ ressource MXDC XPS \_ S0PAGE \_ \_**](mxdcxpss0pageresource.md) représentant une ressource, telle qu’une police ou un fichier image, sur une page de document XPS.</span><span class="sxs-lookup"><span data-stu-id="c3956-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3956-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c3956-111">Remarks</span></span>

<span data-ttu-id="c3956-112">Cette structure est transmise dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) lorsque cette fonction est appelée avec l’échappement [**MXDC \_**](mxdc-escape.md) Escape et que le membre **opcode** de la structure T de l' [**\_ \_ en-tête \_ d’échappement MXDC**](mxdcescapeheader.md) est **MXDCOP définir la \_ \_ \_ ressource S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="c3956-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="c3956-113">Le résultat est une ressource de page à envoyer à MXDC.</span><span class="sxs-lookup"><span data-stu-id="c3956-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="c3956-114">Allouez de la mémoire pour l’échappement comme indiqué ci-dessous, définissez les champs en fonction des besoins, puis appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="c3956-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="c3956-115">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Toutefois, il peut y avoir plus d’un de ces appels entre les appels à **StartPage** et **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="c3956-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="c3956-116">La consommation de la diffusion en continu est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ défini \_ S0PAGE \_** **opcode** de ressource pour chaque ressource sur la page avant d’appeler **ExtEscape** avec l'**opcode** **MXDCOP \_ Set \_ S0PAGE**.  </span><span class="sxs-lookup"><span data-stu-id="c3956-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3956-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3956-117">Requirements</span></span>



| <span data-ttu-id="c3956-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3956-118">Requirement</span></span> | <span data-ttu-id="c3956-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3956-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3956-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3956-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c3956-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3956-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c3956-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3956-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c3956-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3956-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c3956-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3956-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3956-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3956-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3956-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3956-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3956-127">Impression</span><span class="sxs-lookup"><span data-stu-id="c3956-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c3956-128">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c3956-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="c3956-129">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3956-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c3956-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="c3956-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="c3956-131">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="c3956-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

