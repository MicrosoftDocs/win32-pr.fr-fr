---
description: Les applications utilisant les fonctions d’API de jeu de caractères et Unicode utilisent généralement la même classe de fenêtre. Le système d’exploitation convertit en toute transparence les messages entre les fenêtres de différentes classes.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Traduction automatique des messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751165"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="d8a13-104">Traduction automatique des messages</span><span class="sxs-lookup"><span data-stu-id="d8a13-104">Automatic Message Translation</span></span>

<span data-ttu-id="d8a13-105">Les applications utilisant les fonctions d’API de jeu de caractères et Unicode utilisent généralement la même classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d8a13-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="d8a13-106">Le système d’exploitation convertit en toute transparence les messages entre les fenêtres de différentes classes.</span><span class="sxs-lookup"><span data-stu-id="d8a13-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="d8a13-107">Une fonction de fenêtre est implémentée pour recevoir des messages au format Unicode ou page de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="d8a13-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="d8a13-108">La fonction de fenêtre peut envoyer des messages ou appeler des fonctions de l’un ou l’autre type.</span><span class="sxs-lookup"><span data-stu-id="d8a13-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="d8a13-109">Les messages suivants comportent des arguments de texte et sont soumis à une traduction de texte automatique.</span><span class="sxs-lookup"><span data-stu-id="d8a13-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="d8a13-110">Pour plus d’informations sur la traduction automatique, consultez [sous-classes et traduction automatique des messages](subclassing-and-automatic-message-translation.md).</span><span class="sxs-lookup"><span data-stu-id="d8a13-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="d8a13-111">$ \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="d8a13-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="d8a13-112">\_Rép.</span><span class="sxs-lookup"><span data-stu-id="d8a13-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="d8a13-113">\_FindString CB</span><span class="sxs-lookup"><span data-stu-id="d8a13-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="d8a13-114">\_GETLBTEXT CB</span><span class="sxs-lookup"><span data-stu-id="d8a13-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="d8a13-115">\_INSERTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="d8a13-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="d8a13-116">\_SELECTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="d8a13-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="d8a13-117">\_GETLINE em</span><span class="sxs-lookup"><span data-stu-id="d8a13-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="d8a13-118">\_REPLACESEL em</span><span class="sxs-lookup"><span data-stu-id="d8a13-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="d8a13-119">\_SETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="d8a13-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="d8a13-120">\_ADDFILE lb</span><span class="sxs-lookup"><span data-stu-id="d8a13-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="d8a13-121">LB \_ ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="d8a13-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="d8a13-122">direction \_ lb</span><span class="sxs-lookup"><span data-stu-id="d8a13-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="d8a13-123">\_FindString lb</span><span class="sxs-lookup"><span data-stu-id="d8a13-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="d8a13-124">LB, \_ GETTEXT</span><span class="sxs-lookup"><span data-stu-id="d8a13-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="d8a13-125">\_INSERTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="d8a13-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="d8a13-126">\_SELECTSTRING lb</span><span class="sxs-lookup"><span data-stu-id="d8a13-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="d8a13-127">\_ASKCBFORMATNAME WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="d8a13-128">\_caractère WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="d8a13-129">\_CHARTOITEM WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="d8a13-130">création de WM \_</span><span class="sxs-lookup"><span data-stu-id="d8a13-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="d8a13-131">\_DEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="d8a13-132">\_DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="d8a13-133">WM \_ GETTEXT</span><span class="sxs-lookup"><span data-stu-id="d8a13-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="d8a13-134">\_MDICREATE WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="d8a13-135">\_MENUCHAR WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="d8a13-136">\_NCCREATE WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="d8a13-137">WM, \_ SETTEXT</span><span class="sxs-lookup"><span data-stu-id="d8a13-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="d8a13-138">\_SYSCHAR WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="d8a13-139">\_SYSDEADCHAR WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="d8a13-140">\_WININICHANGE WM</span><span class="sxs-lookup"><span data-stu-id="d8a13-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="d8a13-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8a13-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8a13-142">Unicode dans l'API Windows</span><span class="sxs-lookup"><span data-stu-id="d8a13-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
