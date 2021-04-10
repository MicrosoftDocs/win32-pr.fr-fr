---
title: Message EM_AUTOURLDETECT (RichEdit. h)
description: Active ou désactive la détection automatique des liens hypertexte par un contrôle RichEdit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942390"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="af590-104">\_Message AUTOURLDETECT em</span><span class="sxs-lookup"><span data-stu-id="af590-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="af590-105">Active ou désactive la détection automatique des liens hypertexte par un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="af590-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="af590-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af590-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af590-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af590-108">Spécifiez 0 pour désactiver la détection de liaison automatique, ou l’une des valeurs suivantes pour activer différents types de détection.</span><span class="sxs-lookup"><span data-stu-id="af590-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="af590-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="af590-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="af590-110">Signification</span><span class="sxs-lookup"><span data-stu-id="af590-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="af590-111"><dt>**AURL \_ DISABLEMIXEDLGC**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="af590-112">**Windows 8**: désactiver la reconnaissance des noms de domaine qui contiennent des étiquettes avec des caractères appartenant à plusieurs des scripts suivants : latin, grec et cyrillique.</span><span class="sxs-lookup"><span data-stu-id="af590-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="af590-113"><dt>**AURL \_ ENABLEDRIVELETTERS**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="af590-114">**Windows 8**: reconnaître les noms de fichiers qui ont une spécification de lecteur de début, par exemple c : \\ temp.</span><span class="sxs-lookup"><span data-stu-id="af590-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="af590-115"><dt>**AURL \_ ENABLEEA**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="af590-116">Cette valeur est déconseillée ; Utilisez **AURL \_ ENABLEEAURLS** à la place.</span><span class="sxs-lookup"><span data-stu-id="af590-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="af590-117"><dt>**AURL \_ ENABLEEAURLS**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="af590-118">Reconnaître les URL qui contiennent des caractères d’Extrême-Orient.</span><span class="sxs-lookup"><span data-stu-id="af590-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="af590-119"><dt>**AURL \_ ENABLEEMAILADDR**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="af590-120">**Windows 8**: reconnaître les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="af590-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="af590-121"><dt>**AURL \_ ENABLETELNO**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="af590-122">**Windows 8**: reconnaître les numéros de téléphone.</span><span class="sxs-lookup"><span data-stu-id="af590-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="af590-123"><dt>**AURL \_ ENABLEURL**</dt></span><span class="sxs-lookup"><span data-stu-id="af590-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="af590-124">**Windows 8**: reconnaître les URL qui incluent le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="af590-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="af590-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af590-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af590-126">Ce paramètre détermine les schémas d’URL reconnus si **AURL \_ ENABLEURL** est actif.</span><span class="sxs-lookup"><span data-stu-id="af590-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="af590-127">Si *lParam* a la valeur null, la liste de noms de schémas par défaut est utilisée (consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="af590-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="af590-128">*LParam* peut également pointer vers une chaîne se terminant par un caractère null, composée de noms de schéma se terminant par un point-virgule allant jusqu’à 50 qui remplacent la liste de noms de schéma par défaut.</span><span class="sxs-lookup"><span data-stu-id="af590-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="af590-129">Par exemple, la chaîne peut être « News : http : ftp : Telnet : ».</span><span class="sxs-lookup"><span data-stu-id="af590-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="af590-130">La syntaxe du nom du schéma est définie dans le document [URI (Uniform Resource Identifiers) : syntaxe générique]( https://www.ietf.org/rfc/rfc2396.txt) sur le site Web IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="af590-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="af590-131">Plus précisément, un nom de schéma peut contenir jusqu’à 13 caractères (y compris le signe deux-points), doit commencer par un caractère alphabétique ASCII et peut être suivi d’un mélange de alphabetics ASCII, de chiffres et de trois caractères de ponctuation : « . », « + » et « - ».</span><span class="sxs-lookup"><span data-stu-id="af590-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="af590-132">Le type de chaîne peut être **char \** _ ou _*WCHAR \*\*_; le contrôle Rich Edit détecte automatiquement le type.</span><span class="sxs-lookup"><span data-stu-id="af590-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af590-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af590-133">Return value</span></span>

<span data-ttu-id="af590-134">Si le message est correctement exécuté, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="af590-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="af590-135">Si le message échoue, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="af590-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="af590-136">Par exemple, le message peut échouer en raison d’une mémoire insuffisante, d’une option de détection non valide ou d’une chaîne de nom de schéma non valide.</span><span class="sxs-lookup"><span data-stu-id="af590-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="af590-137">Si _lParam \* contient plus de 50 noms de schéma, le message échoue avec la valeur de retour **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="af590-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="af590-138">Notes</span><span class="sxs-lookup"><span data-stu-id="af590-138">Remarks</span></span>

<span data-ttu-id="af590-139">Si la détection automatique d’URL est activée (autrement dit, *wParam* comprend **AURL \_ ENABLEURL**), le contrôle Rich Edit analyse tout texte modifié pour déterminer si le texte correspond au format d’une URL (ou plus généralement dans Windows 8 ou version ultérieure, un identificateur de ressource IRI international).</span><span class="sxs-lookup"><span data-stu-id="af590-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="af590-140">Si *lParam* a la valeur null, le contrôle détecte les URL qui commencent par les noms de schémas suivants :</span><span class="sxs-lookup"><span data-stu-id="af590-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="af590-141">callto</span><span class="sxs-lookup"><span data-stu-id="af590-141">callto</span></span>
-   <span data-ttu-id="af590-142">fichier</span><span class="sxs-lookup"><span data-stu-id="af590-142">file</span></span>
-   <span data-ttu-id="af590-143">ftp</span><span class="sxs-lookup"><span data-stu-id="af590-143">ftp</span></span>
-   <span data-ttu-id="af590-144">gopher</span><span class="sxs-lookup"><span data-stu-id="af590-144">gopher</span></span>
-   <span data-ttu-id="af590-145">http</span><span class="sxs-lookup"><span data-stu-id="af590-145">http</span></span>
-   <span data-ttu-id="af590-146">https</span><span class="sxs-lookup"><span data-stu-id="af590-146">https</span></span>
-   <span data-ttu-id="af590-147">mailto</span><span class="sxs-lookup"><span data-stu-id="af590-147">mailto</span></span>
-   <span data-ttu-id="af590-148">news</span><span class="sxs-lookup"><span data-stu-id="af590-148">news</span></span>
-   <span data-ttu-id="af590-149">HDInsight</span><span class="sxs-lookup"><span data-stu-id="af590-149">notes</span></span>
-   <span data-ttu-id="af590-150">NNTP</span><span class="sxs-lookup"><span data-stu-id="af590-150">nntp</span></span>
-   <span data-ttu-id="af590-151">onenote</span><span class="sxs-lookup"><span data-stu-id="af590-151">onenote</span></span>
-   <span data-ttu-id="af590-152">programme</span><span class="sxs-lookup"><span data-stu-id="af590-152">outlook</span></span>
-   <span data-ttu-id="af590-153">prospero</span><span class="sxs-lookup"><span data-stu-id="af590-153">prospero</span></span>
-   <span data-ttu-id="af590-154">tel</span><span class="sxs-lookup"><span data-stu-id="af590-154">tel</span></span>
-   <span data-ttu-id="af590-155">telnet</span><span class="sxs-lookup"><span data-stu-id="af590-155">telnet</span></span>
-   <span data-ttu-id="af590-156">wais</span><span class="sxs-lookup"><span data-stu-id="af590-156">wais</span></span>
-   <span data-ttu-id="af590-157">webcal</span><span class="sxs-lookup"><span data-stu-id="af590-157">webcal</span></span>

<span data-ttu-id="af590-158">Lorsque la détection automatique des liens est activée, le contrôle RichEdit supprime l’effet de **\_ lien CFE** d’un texte modifié qui n’a pas un format reconnu par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="af590-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="af590-159">Si votre application utilise l’effet de **\_ lien CFE** pour marquer d’autres types de texte, n’activez pas la détection automatique des liens.</span><span class="sxs-lookup"><span data-stu-id="af590-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="af590-160">Le contrôle RichEdit ne vérifie pas si un lien détecté existe ; Cette responsabilité appartient au client.</span><span class="sxs-lookup"><span data-stu-id="af590-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="af590-161">Un contrôle RichEdit envoie la notification [en \_ lien](en-link.md) lorsqu’il reçoit plusieurs messages lorsque le pointeur de la souris est sur du texte qui a l’effet de **\_ lien CFE** .</span><span class="sxs-lookup"><span data-stu-id="af590-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="af590-162">Pour plus d’informations, consultez [liens hypertexte RichEdit automatique](/archive/blogs/murrays/automatic-richedit-hyperlinks) et [liens hypertexte de nom convivial RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span><span class="sxs-lookup"><span data-stu-id="af590-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="af590-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af590-163">Requirements</span></span>



| <span data-ttu-id="af590-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af590-164">Requirement</span></span> | <span data-ttu-id="af590-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="af590-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af590-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af590-166">Minimum supported client</span></span><br/> | <span data-ttu-id="af590-167">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af590-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af590-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af590-168">Minimum supported server</span></span><br/> | <span data-ttu-id="af590-169">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af590-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af590-170">En-tête</span><span class="sxs-lookup"><span data-stu-id="af590-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="af590-171"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af590-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af590-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af590-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af590-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="af590-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="af590-174">en \_ lien</span><span class="sxs-lookup"><span data-stu-id="af590-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

