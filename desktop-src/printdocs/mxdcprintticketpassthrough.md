---
description: La \_ structure MXDC PRINTTICKET \_ Data \_ T contient un ticket d’impression de document XPS, qui contient les paramètres d’imprimante et de travail d’impression, à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Structure MXDC_PRINTTICKET_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864961"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="2650c-103">\_Structure de \_ données MXDC PRINTTICKET \_</span><span class="sxs-lookup"><span data-stu-id="2650c-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="2650c-104">La structure **MXDC \_ PRINTTICKET \_ Data \_ T** contient un ticket d’impression de document XPS, qui contient les paramètres d’imprimante et de travail d’impression, à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.</span><span class="sxs-lookup"><span data-stu-id="2650c-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2650c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2650c-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="2650c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2650c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2650c-107">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="2650c-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="2650c-108">Taille du ticket d’impression en octets.</span><span class="sxs-lookup"><span data-stu-id="2650c-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2650c-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="2650c-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="2650c-110">Ticket d’impression du document XPS.</span><span class="sxs-lookup"><span data-stu-id="2650c-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2650c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2650c-111">Remarks</span></span>

<span data-ttu-id="2650c-112">Cette structure est ajoutée à une structure [**\_ T d' \_ en \_ -tête d’échappement MXDC**](mxdcescapeheader.md) dont le membre **opcode** est défini sur la **\_ \_ \_ page fixe MXDCOP PrintTicket**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq** pour créer une structure [**MXDC \_ PrintTicket \_ Escape \_ T**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="2650c-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="2650c-113">La **structure \_ MXDC \_ PRINTTICKET \_ Escape T** est ensuite transmise au paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quand elle est appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="2650c-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="2650c-114">L’effet est d’écrire le ticket d’impression dans le fichier de document XPS.</span><span class="sxs-lookup"><span data-stu-id="2650c-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="2650c-115">Si l' **opcode** est défini sur **la \_ \_ \_ page fixe MXDCOP PRINTTICKET**, l’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="2650c-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="2650c-116">Si le **opcode** défini sur **MXDCOP \_ PrintTicket \_ fixed \_ doc** ou **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, l’appel à **ExtEscape** doit se produire entre un appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et un appel à [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="2650c-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="2650c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2650c-117">Requirements</span></span>



| <span data-ttu-id="2650c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2650c-118">Requirement</span></span> | <span data-ttu-id="2650c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2650c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2650c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2650c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2650c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2650c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2650c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2650c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2650c-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2650c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2650c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2650c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2650c-125"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="2650c-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2650c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2650c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2650c-127">Impression</span><span class="sxs-lookup"><span data-stu-id="2650c-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2650c-128">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2650c-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="2650c-129">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2650c-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2650c-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="2650c-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="2650c-131">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="2650c-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

