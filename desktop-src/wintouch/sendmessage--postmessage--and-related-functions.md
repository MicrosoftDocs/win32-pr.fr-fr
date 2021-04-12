---
title: SendMessage, PostMessage et fonctions connexes
description: Cette section décrit les considérations relatives au transfert des messages à l’aide de SendMessage, PostMessage et des fonctions associées avec des messages tactiles.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382277"
---
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="3d4c4-103">SendMessage, PostMessage et fonctions connexes</span><span class="sxs-lookup"><span data-stu-id="3d4c4-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="3d4c4-104">Cette section décrit les considérations relatives au transfert des messages à l’aide de [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)et des fonctions associées avec des messages tactiles.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="3d4c4-105">Si un message tactile est transféré à l’aide de [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)ou une autre fonction associée, le handle d’entrée tactile est fermé.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="3d4c4-106">Si vous avez récupéré les informations contenues référencées par une poignée d’entrée tactile via un appel à [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), ces données restent valides jusqu’à ce que vous libériez la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="3d4c4-107">Une application qui reçoit des messages tactiles transmis via l’un de ces mécanismes est propriétaire du handle d’entrée tactile qu’elle reçoit dans le message *lParam* et est responsable de sa fermeture.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="3d4c4-108">Si vous ne fermez pas le descripteur avec un appel à [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), transmettez le message à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)ou transférez le message à l’aide de [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)ou d’une fonction associée, vous obtiendrez une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="3d4c4-109">Les messages tactiles sont soumis aux règles de l’isolation des privilèges de l’interface utilisateur (UIPI) normales lorsqu’ils sont transférés.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="3d4c4-110">Fonctions liées à SendMessage et PostMessage</span><span class="sxs-lookup"><span data-stu-id="3d4c4-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="3d4c4-111">Les fonctions suivantes peuvent affecter l’état du handle d’entrée tactile.</span><span class="sxs-lookup"><span data-stu-id="3d4c4-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="3d4c4-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="3d4c4-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="3d4c4-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="3d4c4-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="3d4c4-114">SendNotifyMessage</span><span class="sxs-lookup"><span data-stu-id="3d4c4-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="3d4c4-115">SendMessageCallback</span><span class="sxs-lookup"><span data-stu-id="3d4c4-115">SendMessageCallback</span></span>
-   <span data-ttu-id="3d4c4-116">SendMessageTimeout</span><span class="sxs-lookup"><span data-stu-id="3d4c4-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="3d4c4-117">PostThreadMessage</span><span class="sxs-lookup"><span data-stu-id="3d4c4-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d4c4-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d4c4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d4c4-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="3d4c4-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="3d4c4-120">DefWindowProc</span><span class="sxs-lookup"><span data-stu-id="3d4c4-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 