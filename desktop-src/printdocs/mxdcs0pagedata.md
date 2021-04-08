---
description: La \_ structure MXDC S0PAGE \_ Data \_ T contient une page de document XPS à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Structure MXDC_S0PAGE_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757743"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="c2b1c-103">\_Structure MXDC S0PAGE \_ Data \_ T</span><span class="sxs-lookup"><span data-stu-id="c2b1c-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="c2b1c-104">La structure **MXDC \_ S0PAGE \_ Data \_ T** contient une page de document XPS à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b1c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2b1c-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="c2b1c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c2b1c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2b1c-107">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="c2b1c-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2b1c-108">Taille de la mémoire tampon de sortie, **bData**.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2b1c-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="c2b1c-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="c2b1c-110">Page de document XPS.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2b1c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c2b1c-111">Remarks</span></span>

<span data-ttu-id="c2b1c-112">Cette structure est ajoutée à une structure [**\_ t d' \_ en \_ -tête d’échappement MXDC**](mxdcescapeheader.md) (dont le **opcode** a la valeur MXDCOP \_ Set \_ S0PAGE) pour créer une structure [**MXDC \_ S0PAGE passthrough d' \_ \_ échappement \_**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="c2b1c-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="c2b1c-113">Cette structure est ensuite transmise au paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quand elle est appelée avec [**MXDC \_ Escape**](mxdc-escape.md) comme caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="c2b1c-114">Le résultat est que le MXDC transmet la page à la sortie sans la traiter.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="c2b1c-115">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="c2b1c-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="c2b1c-116">L’application appelante est chargée de valider le code XML de la page de document XPS.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="c2b1c-117">La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ définir la \_ \_ ressource S0PAGE** comme **opcode** pour chaque ressource sur la page avant de l’appeler avec **MXDCOP \_ définir \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="c2b1c-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b1c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2b1c-118">Requirements</span></span>



| <span data-ttu-id="c2b1c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2b1c-119">Requirement</span></span> | <span data-ttu-id="c2b1c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2b1c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c2b1c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2b1c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b1c-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2b1c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2b1c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2b1c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b1c-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2b1c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2b1c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2b1c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2b1c-126"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2b1c-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b1c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2b1c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b1c-128">Impression</span><span class="sxs-lookup"><span data-stu-id="c2b1c-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c2b1c-129">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c2b1c-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="c2b1c-130">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c2b1c-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c2b1c-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="c2b1c-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="c2b1c-132">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="c2b1c-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

