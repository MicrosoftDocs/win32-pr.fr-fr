---
description: La \_ structure MXDC PrintTicket \_ Escape \_ t est une \_ structure d' \_ en-tête d’échappement MXDC \_ concaténée avec une \_ structure de données MXDC PrintTicket \_ \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Structure MXDC_PRINTTICKET_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535600"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="eaf05-103">\_Structure MXDC PRINTTICKET \_ Escape \_ T</span><span class="sxs-lookup"><span data-stu-id="eaf05-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="eaf05-104">La structure **MXDC \_ PrintTicket \_ Escape \_ t** est une structure d' [**\_ \_ en-tête d’échappement MXDC \_**](mxdcescapeheader.md) concaténée avec une structure de [**\_ \_ données \_ MXDC PrintTicket**](mxdcprintticketpassthrough.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf05-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaf05-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="eaf05-106">Membres</span><span class="sxs-lookup"><span data-stu-id="eaf05-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eaf05-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="eaf05-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="eaf05-108">Une [**structure \_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) avec son membre **OPCODE** défini sur la \_ page fixe MXDCOP PrintTicket \_ \_ , MXDCOP \_ PRINTTICKET \_ fixed \_ doc ou MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq.</span><span class="sxs-lookup"><span data-stu-id="eaf05-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="eaf05-109">**printTicketData**</span><span class="sxs-lookup"><span data-stu-id="eaf05-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="eaf05-110">Structure [**de \_ \_ données MXDC \_ PRINTTICKET**](mxdcprintticketpassthrough.md) contenant le ticket d’impression.</span><span class="sxs-lookup"><span data-stu-id="eaf05-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaf05-111">Notes</span><span class="sxs-lookup"><span data-stu-id="eaf05-111">Remarks</span></span>

<span data-ttu-id="eaf05-112">Cette structure est passée dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) lorsque cette fonction est appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) et le membre **opcode** de la structure T de l' [**\_ \_ en-tête \_ d’échappement MXDC**](mxdcescapeheader.md) est **MXDCOP \_ \_ \_ page fixe PrintTicket**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**.</span><span class="sxs-lookup"><span data-stu-id="eaf05-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="eaf05-113">Le résultat est d’écrire le ticket d’impression dans le fichier de document XPS.</span><span class="sxs-lookup"><span data-stu-id="eaf05-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="eaf05-114">Allouez de la mémoire pour l’échappement comme indiqué ci-dessous, définissez les champs en fonction des besoins, puis appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="eaf05-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="eaf05-115">Si l' **opcode** est défini sur **la \_ \_ \_ page fixe MXDCOP PRINTTICKET**, l’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="eaf05-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="eaf05-116">Si le **opcode** défini sur **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, l’appel à **ExtEscape** doit se produire entre un appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et un appel à [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="eaf05-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf05-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaf05-117">Requirements</span></span>



| <span data-ttu-id="eaf05-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaf05-118">Requirement</span></span> | <span data-ttu-id="eaf05-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf05-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="eaf05-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf05-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf05-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf05-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eaf05-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf05-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf05-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf05-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eaf05-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="eaf05-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaf05-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf05-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf05-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf05-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf05-127">Impression</span><span class="sxs-lookup"><span data-stu-id="eaf05-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="eaf05-128">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="eaf05-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="eaf05-129">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eaf05-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eaf05-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="eaf05-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="eaf05-131">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="eaf05-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

