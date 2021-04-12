---
title: Message WM_DDE_EXECUTE (DDE. h)
description: Une application cliente échange dynamique de données (DDE) publie un \_ \_ message WM Execute DDE dans une application de serveur DDE pour envoyer une chaîne au serveur à traiter en tant que série de commandes.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- WM_DDE_EXECUTE l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384784"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="5f0fd-104">\_Message d’exécution DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="5f0fd-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="5f0fd-105">Une application cliente échange dynamique de données (DDE) publie un message **WM \_ \_ Execute DDE** dans une application de serveur DDE pour envoyer une chaîne au serveur à traiter en tant que série de commandes.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="5f0fd-106">L’application serveur doit poster un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE en réponse.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="5f0fd-107">Pour poster ce message, appelez la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="5f0fd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f0fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0fd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f0fd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0fd-110">Handle de la fenêtre client qui publie le message.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="5f0fd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f0fd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f0fd-112">Contient un objet mémoire global qui fait référence à une chaîne de commande ANSI ou Unicode, en fonction des types de fenêtres impliquées dans la conversation.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f0fd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5f0fd-113">Remarks</span></span>

<span data-ttu-id="5f0fd-114">La chaîne de commande est une chaîne se terminant par un caractère null qui se compose d’une ou de plusieurs chaînes opcode placées entre crochets ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="5f0fd-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="5f0fd-115">Chaque chaîne opcode a la syntaxe suivante, où la liste de *paramètres* est facultative :</span><span class="sxs-lookup"><span data-stu-id="5f0fd-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="5f0fd-116">*paramètres opcode*</span><span class="sxs-lookup"><span data-stu-id="5f0fd-116">*opcode parameters*</span></span>

<span data-ttu-id="5f0fd-117">L' *opcode* est tout jeton unique défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="5f0fd-118">Il ne peut pas contenir des espaces, des virgules, des parenthèses, des crochets ou des guillemets.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="5f0fd-119">La liste de *paramètres* peut contenir n’importe quelle valeur ou valeur définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="5f0fd-120">Plusieurs paramètres sont séparés par des virgules, et l’ensemble de la liste de paramètres est placé entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="5f0fd-121">Les paramètres ne peuvent pas inclure de virgules ou de parenthèses à l’intérieur d’une chaîne entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="5f0fd-122">Si un crochet ou un caractère de parenthèse doit apparaître dans une chaîne entre guillemets, il n’est pas nécessaire qu’il soit doublé, comme c’était le cas dans les anciennes règles.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="5f0fd-123">Les chaînes de commande valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f0fd-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="5f0fd-124">Notez que, dans les anciennes règles, les parenthèses et les crochets devaient être doublés, comme suit :</span><span class="sxs-lookup"><span data-stu-id="5f0fd-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="5f0fd-125">Les serveurs doivent être en mesure d’analyser les commandes sous l’une ou l’autre forme.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="5f0fd-126">Les chaînes d’exécution Unicode ne doivent être utilisées que lorsque les handles de fenêtre du client et du serveur forcent la fonction [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) à retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="5f0fd-127">Publication</span><span class="sxs-lookup"><span data-stu-id="5f0fd-127">Posting</span></span>

<span data-ttu-id="5f0fd-128">L’application cliente alloue l’objet de mémoire globale en appelant la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="5f0fd-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="5f0fd-129">Lors du traitement du message d’accusé de réception [**\_ \_ DDE DDE**](wm-dde-ack.md) que le serveur publie en réponse à un message **WM d' \_ \_ exécution DDE** , l’application cliente doit supprimer l’objet retourné par le message d' **\_ \_ accusé** de réception DDE.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="5f0fd-130">Réception</span><span class="sxs-lookup"><span data-stu-id="5f0fd-130">Receiving</span></span>

<span data-ttu-id="5f0fd-131">L’application serveur publie le message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) pour répondre positivement ou négativement.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="5f0fd-132">Le serveur doit réutiliser l’objet mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="5f0fd-133">Sauf indication contraire d’un sous-protocole, le serveur ne doit pas envoyer le message d’accusé de réception DDE de l’échange de messages ( [**\_ \_ ACK**](wm-dde-ack.md) ) pour que toutes les actions spécifiées par la chaîne de commande d’exécution soient terminées.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="5f0fd-134">La seule exception à cette règle est lorsque la chaîne oblige le serveur à mettre fin à la conversation.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0fd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f0fd-135">Requirements</span></span>



| <span data-ttu-id="5f0fd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f0fd-136">Requirement</span></span> | <span data-ttu-id="5f0fd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f0fd-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0fd-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f0fd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0fd-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5f0fd-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f0fd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0fd-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f0fd-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f0fd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f0fd-143"><dt>DDE. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0fd-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0fd-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f0fd-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f0fd-145">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f0fd-146">**IsWindowUnicode**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="5f0fd-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="5f0fd-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="5f0fd-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="5f0fd-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="5f0fd-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="5f0fd-152">**\_ACK DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="5f0fd-153">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f0fd-154">À propos de échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="5f0fd-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

