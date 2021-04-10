---
description: La \_ \_ structure T de l’en-tête d’échappement MXDC \_ contient le code d’opération d’un appel à ExtEscape avec MXDC \_ Escape comme paramètre nEscape. Il fournit également la taille des mémoires tampons d’entrée et de sortie.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Structure MXDC_ESCAPE_HEADER_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868529"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="7cfd1-104">MXDC \_ \_ structure T de l’en-tête d’échappement \_</span><span class="sxs-lookup"><span data-stu-id="7cfd1-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="7cfd1-105">La structure T de l' **\_ \_ \_ en-tête d’échappement MXDC** contient le code d’opération d’un appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec [**MXDC \_ Escape**](mxdc-escape.md) comme paramètre *nEscape* .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="7cfd1-106">Il fournit également la taille des mémoires tampons d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cfd1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cfd1-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="7cfd1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7cfd1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cfd1-109">**cbInput**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="7cfd1-110">Taille de la mémoire tampon d’entrée qui sera passée au paramètre *lpszOutData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="7cfd1-111">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="7cfd1-112">Taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-112">The size of the output buffer.</span></span> <span data-ttu-id="7cfd1-113">Il s’agit de la même valeur que le paramètre *cbOutput* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="7cfd1-114">**opCode**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="7cfd1-115">Constante de code qui indique à MXDC ce qu’il faut faire.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="7cfd1-116">Code des opérations</span><span class="sxs-lookup"><span data-stu-id="7cfd1-116">Operations code</span></span>                      | <span data-ttu-id="7cfd1-117">Description</span><span class="sxs-lookup"><span data-stu-id="7cfd1-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cfd1-118">MXDCOP \_ obtient le \_ nom du fichier</span><span class="sxs-lookup"><span data-stu-id="7cfd1-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="7cfd1-119">Retourne, dans le paramètre *lpszOutData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , le chemin d’accès complet du fichier de sortie comme une chaîne se terminant par zéro ou la taille de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="7cfd1-120">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-120">See Remarks.</span></span>                   |
| <span data-ttu-id="7cfd1-121">\_ \_ \_ Seq document fixe MXDCOP \_ PRINTTICKET</span><span class="sxs-lookup"><span data-stu-id="7cfd1-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="7cfd1-122">Associe un ticket d’impression à une séquence de documents fixe XPS.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="7cfd1-123">\_ \_ document fixe MXDCOP \_ PRINTTICKET</span><span class="sxs-lookup"><span data-stu-id="7cfd1-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="7cfd1-124">Associe un ticket d’impression à un document XPS.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="7cfd1-125">\_ \_ page fixe MXDCOP \_ PRINTTICKET</span><span class="sxs-lookup"><span data-stu-id="7cfd1-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="7cfd1-126">Associe un ticket d’impression à une page XPS.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="7cfd1-127">MXDCOP \_ Set \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="7cfd1-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="7cfd1-128">Envoie le balisage XPS de la page actuelle à la sortie.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="7cfd1-129">MXDCOP \_ définir \_ la \_ ressource S0PAGE</span><span class="sxs-lookup"><span data-stu-id="7cfd1-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="7cfd1-130">Envoie une ressource sur la page, telle qu’une image ou une police, à la sortie.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="7cfd1-131">MXDCOP \_ définir \_ le \_ mode XPSPASSTHRU</span><span class="sxs-lookup"><span data-stu-id="7cfd1-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="7cfd1-132">Place le MXDC dans un État direct, ce qui permet à une application d’écrire XPS directement dans le fichier de sortie sans aucun traitement de la MXDC.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="7cfd1-133">Un document entier ou même une séquence de documents peut être écrit de cette façon.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cfd1-134">Notes</span><span class="sxs-lookup"><span data-stu-id="7cfd1-134">Remarks</span></span>

<span data-ttu-id="7cfd1-135">Avant d’appeler [**MXDC \_ Escape**](mxdc-escape.md), \_ les applications doivent d’abord vérifier que le pilote est MXDC en appelant [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec l’échappement [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="7cfd1-136">Si le pilote est le MXDC, la fonction retourne la chaîne se terminant par zéro « http://schemas.microsoft.com/xps/2005/06 ».</span><span class="sxs-lookup"><span data-stu-id="7cfd1-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="7cfd1-137">Cette structure est toujours au début des données passées à la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) dans son paramètre *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="7cfd1-138">Lorsque l' **opcode** est MXDCOP, \_ récupérez le nom de \_ fichier :</span><span class="sxs-lookup"><span data-stu-id="7cfd1-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="7cfd1-139">Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose uniquement de la structure T de l' **\_ \_ en-tête \_ d’échappement MXDC** .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="7cfd1-140">Obtenez le nom du fichier de sortie en appelant [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deux fois.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="7cfd1-141">La première fois, Pass 4 au paramètre *cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="7cfd1-142">Définissez le paramètre *lpszOutData* pour qu’il pointe vers tous les 4 octets alloués de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="7cfd1-143">La taille du chemin d’accès complet du fichier est retournée dans le paramètre *lpszOutData* de **ExtEscape**.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="7cfd1-144">Ensuite, appelez à nouveau la fonction.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-144">Then call the function again.</span></span> <span data-ttu-id="7cfd1-145">Cette fois, définissez *cbOutput* et *cbInput* sur 4 + *DataSize*.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="7cfd1-146">Le chemin d’accès complet au fichier est retourné dans une structure [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="7cfd1-147">Lorsque l' **opcode** est MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq ou MXDCOP \_ PrintTicket \_ fixed \_ doc :</span><span class="sxs-lookup"><span data-stu-id="7cfd1-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="7cfd1-148">Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concaténée dans une structure [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="7cfd1-149">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) et un appel à [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="7cfd1-150">Lorsque l' **opcode** est \_ la \_ page fixe MXDCOP PRINTTICKET \_ :</span><span class="sxs-lookup"><span data-stu-id="7cfd1-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="7cfd1-151">Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concaténée dans une structure [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="7cfd1-152">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="7cfd1-153">Lorsque l' **opcode** est MXDCOP, \_ définissez \_ S0PAGE :</span><span class="sxs-lookup"><span data-stu-id="7cfd1-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="7cfd1-154">Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcS0PageData**](mxdcs0pagedata.md) concaténée dans une structure [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="7cfd1-155">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="7cfd1-156">L’application appelante est chargée de valider le XML.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="7cfd1-157">La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec MXDCOP \_ définir \_ \_ la ressource S0PAGE comme **opcode** pour chaque ressource sur la page avant de l’appeler avec MXDCOP \_ définir \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="7cfd1-158">Lorsque l' **opcode** est MXDCOP, \_ définissez la \_ \_ ressource S0PAGE :</span><span class="sxs-lookup"><span data-stu-id="7cfd1-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="7cfd1-159">Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose de la structure **\_ \_ \_ T d’en-tête d’échappement MXDC** et d’une structure [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concaténée dans une structure [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="7cfd1-160">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit se produire entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), mais il peut y avoir plusieurs appels de ce type entre les appels **StartPage** et **EndPage** .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="7cfd1-161">La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec MXDCOP \_ définir \_ \_ la ressource S0PAGE comme **opcode** pour chaque ressource sur la page avant de l’appeler avec MXDCOP \_ définir \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="7cfd1-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="7cfd1-162">Lorsque l' **opcode** est MXDCOP, \_ Définissez le \_ \_ mode XPSPASSTHRU :</span><span class="sxs-lookup"><span data-stu-id="7cfd1-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="7cfd1-163">Le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) se compose uniquement de la structure T de l' **\_ \_ en-tête \_ d’échappement MXDC** .</span><span class="sxs-lookup"><span data-stu-id="7cfd1-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="7cfd1-164">Cet appel doit se produire avant l’appel à [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span><span class="sxs-lookup"><span data-stu-id="7cfd1-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cfd1-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cfd1-165">Requirements</span></span>



| <span data-ttu-id="7cfd1-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cfd1-166">Requirement</span></span> | <span data-ttu-id="7cfd1-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cfd1-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7cfd1-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cfd1-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7cfd1-169">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cfd1-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cfd1-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cfd1-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7cfd1-171">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cfd1-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7cfd1-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cfd1-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cfd1-173"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cfd1-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cfd1-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cfd1-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cfd1-175">Impression</span><span class="sxs-lookup"><span data-stu-id="7cfd1-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7cfd1-176">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7cfd1-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="7cfd1-177">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cfd1-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7cfd1-178">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="7cfd1-179">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="7cfd1-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

