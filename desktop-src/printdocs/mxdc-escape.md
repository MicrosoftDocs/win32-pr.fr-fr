---
description: La fonction d’échappement de l' \_ imprimante MXDC Escape permet aux applications d’écrire des documents dans un fichier ou sur une imprimante au format XPS (XML Paper Specification) au moyen de Microsoft XPS Document Converter (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE fonction (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541207"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="654a4-103">MXDC \_ fonction d’échappement)</span><span class="sxs-lookup"><span data-stu-id="654a4-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="654a4-104">La fonction d’échappement de l’imprimante **MXDC \_ Escape** permet aux applications d’écrire des documents dans un fichier ou sur une imprimante au format XPS (XML Paper Specification) au moyen de Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="654a4-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="654a4-105">Pour effectuer cette opération, appelez la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="654a4-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="654a4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="654a4-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="654a4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="654a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654a4-108">*HDC*</span><span class="sxs-lookup"><span data-stu-id="654a4-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="654a4-109">Handle vers le contexte de périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="654a4-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="654a4-110">*cbInput*</span><span class="sxs-lookup"><span data-stu-id="654a4-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="654a4-111">Taille, en octets, des données vers lesquelles pointe le paramètre *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="654a4-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="654a4-112">*lpszInData*</span><span class="sxs-lookup"><span data-stu-id="654a4-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="654a4-113">Pointeur vers une mémoire tampon contenant les données d’entrée, qui sont toujours stockées dans l’une des structures suivantes.</span><span class="sxs-lookup"><span data-stu-id="654a4-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="654a4-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span><span class="sxs-lookup"><span data-stu-id="654a4-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="654a4-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span><span class="sxs-lookup"><span data-stu-id="654a4-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="654a4-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="654a4-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="654a4-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="654a4-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="654a4-118">Chacune de ces structures a un membre opcode qui spécifie ce que le MXDC est supposé faire.</span><span class="sxs-lookup"><span data-stu-id="654a4-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="654a4-119">Pour obtenir des remarques détaillées sur ces codes, consultez MxdcEscapeHeader.</span><span class="sxs-lookup"><span data-stu-id="654a4-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="654a4-120">Code d’opération (OpCode)</span><span class="sxs-lookup"><span data-stu-id="654a4-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="654a4-121">Action</span><span class="sxs-lookup"><span data-stu-id="654a4-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="654a4-122"><dt>**MXDCOP \_ obtient le \_ nom du fichier**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="654a4-123">Définit le paramètre *lpszOutData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) sur, soit le chemin d’accès complet du fichier de sortie comme une chaîne se terminant par zéro, soit la taille de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="654a4-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="654a4-124"><dt>**\_ \_ \_ Seq document fixe MXDCOP \_ PRINTTICKET**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="654a4-125">Associe un ticket d’impression à une séquence de documents fixe XPS.</span><span class="sxs-lookup"><span data-stu-id="654a4-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="654a4-126"><dt>**\_ \_ document fixe MXDCOP \_ PRINTTICKET**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="654a4-127">Associe un ticket d’impression à un document XPS.</span><span class="sxs-lookup"><span data-stu-id="654a4-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="654a4-128"><dt>**\_ \_ page fixe MXDCOP \_ PRINTTICKET**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="654a4-129">Associe un ticket d’impression à une page XPS.</span><span class="sxs-lookup"><span data-stu-id="654a4-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="654a4-130"><dt>**MXDCOP \_ Set \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="654a4-131">Envoie le balisage XPS de la page actuelle à la sortie.</span><span class="sxs-lookup"><span data-stu-id="654a4-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="654a4-132"><dt>**MXDCOP \_ définir \_ la \_ ressource S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="654a4-133">Envoie une ressource sur la page, telle qu’une image ou une police, à la sortie.</span><span class="sxs-lookup"><span data-stu-id="654a4-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="654a4-134"><dt>**MXDCOP \_ définir \_ le \_ mode XPSPASSTHRU**</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="654a4-135">Place le MXDC dans un État pass-through, permettant à une application d’écrire XPS directement dans le fichier de sortie sans aucun traitement de la MXDC.</span><span class="sxs-lookup"><span data-stu-id="654a4-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="654a4-136">Un document entier ou même une séquence de documents peut être écrit de cette façon.</span><span class="sxs-lookup"><span data-stu-id="654a4-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="654a4-137">*cbOutput*</span><span class="sxs-lookup"><span data-stu-id="654a4-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="654a4-138">Taille, en octets, des données vers lesquelles pointe le paramètre *lpszOutData* .</span><span class="sxs-lookup"><span data-stu-id="654a4-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="654a4-139">*lpszOutData*</span><span class="sxs-lookup"><span data-stu-id="654a4-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="654a4-140">Pointeur vers une mémoire tampon contenant les données de sortie.</span><span class="sxs-lookup"><span data-stu-id="654a4-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654a4-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="654a4-141">Return value</span></span>

<span data-ttu-id="654a4-142">Si la fonction est réussie, la valeur de retour est supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="654a4-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="654a4-143">Si la fonction échoue ou n’est pas prise en charge, la valeur de retour est inférieure ou égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="654a4-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="654a4-144">Notes</span><span class="sxs-lookup"><span data-stu-id="654a4-144">Remarks</span></span>

<span data-ttu-id="654a4-145">Cette séquence d’échappement est prise en charge par MXDC et XPSDrv, mais pas par GDI.</span><span class="sxs-lookup"><span data-stu-id="654a4-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="654a4-146">Pour déterminer si le pilote d’imprimante est le MXDC, appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec l’échappement [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="654a4-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="654a4-147">Si le pilote est le MXDC, **ExtEscape** retourne la chaîne se terminant par zéro « http://schemas.microsoft.com/xps/2005/06 ».</span><span class="sxs-lookup"><span data-stu-id="654a4-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="654a4-148">Assurez-vous que la mémoire tampon référencée par le paramètre *lpszOutData* est suffisamment grande pour contenir cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="654a4-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="654a4-149">Pour déterminer si le pilote d’imprimante est le pilote Microsoft XPS document Writer intégré de Windows, vérifiez que le pilote d’imprimante est le MXDC, puis déterminez si le nom du pilote d’imprimante est « Microsoft XPS document Writer ».</span><span class="sxs-lookup"><span data-stu-id="654a4-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="654a4-150">Pour connaître le nom du pilote d’imprimante, utilisez l’une des techniques suivantes.</span><span class="sxs-lookup"><span data-stu-id="654a4-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="654a4-151">Appelez [**GetPrinterDriver**](getprinterdriver.md) avec la valeur de paramètre *Level* définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="654a4-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="654a4-152">Le nom du pilote d’imprimante est retourné dans le membre **pname** de la structure [**\_ informations sur le pilote \_ 1**](driver-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="654a4-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="654a4-153">ou</span><span class="sxs-lookup"><span data-stu-id="654a4-153">or</span></span>  
<span data-ttu-id="654a4-154">Appelez [**GetPrinter**](getprinter.md) avec la valeur de paramètre *Level* définie sur 2.</span><span class="sxs-lookup"><span data-stu-id="654a4-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="654a4-155">Le nom du pilote d’imprimante est retourné dans le membre **pDriverName** de la structure [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="654a4-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="654a4-156">Le tableau suivant indique où trouver différents objets dans le fichier XPS. les différents types d’objets sont écrits.</span><span class="sxs-lookup"><span data-stu-id="654a4-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="654a4-157">Object</span><span class="sxs-lookup"><span data-stu-id="654a4-157">Object</span></span>       | <span data-ttu-id="654a4-158">Emplacement dans le fichier de sortie</span><span class="sxs-lookup"><span data-stu-id="654a4-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="654a4-159">Page fixe</span><span class="sxs-lookup"><span data-stu-id="654a4-159">Fixed Page</span></span>   | <span data-ttu-id="654a4-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="654a4-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="654a4-161">Thumbnail</span><span class="sxs-lookup"><span data-stu-id="654a4-161">Thumbnail</span></span>    | <span data-ttu-id="654a4-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="654a4-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="654a4-163">Imprimer le ticket</span><span class="sxs-lookup"><span data-stu-id="654a4-163">Print Ticket</span></span> | <span data-ttu-id="654a4-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="654a4-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="654a4-165">Police</span><span class="sxs-lookup"><span data-stu-id="654a4-165">Font</span></span>         | <span data-ttu-id="654a4-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="654a4-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="654a4-167">Image</span><span class="sxs-lookup"><span data-stu-id="654a4-167">Image</span></span>        | <span data-ttu-id="654a4-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="654a4-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="654a4-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="654a4-169">Requirements</span></span>



| <span data-ttu-id="654a4-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="654a4-170">Requirement</span></span> | <span data-ttu-id="654a4-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="654a4-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="654a4-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="654a4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="654a4-173">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="654a4-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="654a4-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="654a4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="654a4-175">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="654a4-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="654a4-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="654a4-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="654a4-177"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="654a4-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654a4-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="654a4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654a4-179">Impression</span><span class="sxs-lookup"><span data-stu-id="654a4-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="654a4-180">[Fonctions d’échappement d’imprimante](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="654a4-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="654a4-181">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="654a4-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

