---
title: Messages d’erreur et notifications
description: Messages d’erreur et notifications
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031136"
---
# <a name="error-messages-and-notifications"></a><span data-ttu-id="16054-104">Messages d’erreur et notifications</span><span class="sxs-lookup"><span data-stu-id="16054-104">Error Messages and Notifications</span></span>

<span data-ttu-id="16054-105">MCIWnd utilise MCI pour contrôler les appareils qui lisent et enregistrent les données multimédias.</span><span class="sxs-lookup"><span data-stu-id="16054-105">MCIWnd uses MCI to control the devices that play and record multimedia data.</span></span> <span data-ttu-id="16054-106">En général, MCIWnd affiche les erreurs MCI dans une boîte de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="16054-106">In general, MCIWnd displays MCI errors in an error dialog box.</span></span> <span data-ttu-id="16054-107">Une erreur MCI est générée chaque fois qu’une commande MCI échoue.</span><span class="sxs-lookup"><span data-stu-id="16054-107">An MCI error is generated whenever an MCI command fails.</span></span> <span data-ttu-id="16054-108">Par exemple, si votre application tente de reprendre la lecture suspendue à l’aide de la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) et que l’appareil actuel ne prend pas en charge la reprise, une erreur est signalée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16054-108">For example, if your application tries to resume paused playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro and the current device does not support resume, an error is reported to the user.</span></span>

<span data-ttu-id="16054-109">MCIWnd vous permet de gérer les messages d’erreur de deux manières :</span><span class="sxs-lookup"><span data-stu-id="16054-109">MCIWnd allows you two choices for handling error messages:</span></span>

-   <span data-ttu-id="16054-110">Vous pouvez empêcher les messages d’erreur d’atteindre l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16054-110">You can prevent error messages from reaching the user.</span></span> <span data-ttu-id="16054-111">Pour empêcher l’affichage des messages d’erreur MCI, spécifiez le \_ style de fenêtre MCIWNDF NOERRORDLG lorsque vous créez une instance d’une fenêtre MCIWnd à l’aide de la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="16054-111">To prevent the display of MCI error messages, specify the MCIWNDF\_NOERRORDLG window style when you create an instance of an MCIWnd window by using the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) or [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span>
-   <span data-ttu-id="16054-112">Vous pouvez les rediriger vers votre application pour les afficher.</span><span class="sxs-lookup"><span data-stu-id="16054-112">You can redirect them to your application for display.</span></span> <span data-ttu-id="16054-113">Pour rediriger les messages d’erreur MCI vers votre application, spécifiez le \_ style de fenêtre MCIWNDF NOTIFYERROR lorsque vous créez une instance d’une fenêtre MCIWnd à l’aide de **MCIWndCreate** ou de **CreateWindowEx**.</span><span class="sxs-lookup"><span data-stu-id="16054-113">To redirect MCI error messages to your application, specify the MCIWNDF\_NOTIFYERROR window style when you create an instance of an MCIWnd window by using **MCIWndCreate** or **CreateWindowEx**.</span></span>

<span data-ttu-id="16054-114">Lorsque la notification d’erreur est activée, MCIWnd envoie chaque message de notification ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) au gestionnaire de messages principal du parent de la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="16054-114">When error notification is enabled, MCIWnd sends each notification message ([**MCIWNDM\_NOTIFYERROR**](mciwndm-notifyerror.md)) to the main message handler of the parent of the MCIWnd window.</span></span> <span data-ttu-id="16054-115">Votre application doit avoir un gestionnaire de messages pour traiter les messages de notification qu’elle reçoit.</span><span class="sxs-lookup"><span data-stu-id="16054-115">Your application must have a message handler to process the notification messages it receives.</span></span>

<span data-ttu-id="16054-116">Vous pouvez obtenir une description textuelle du message d’erreur MCI le plus récent à l’aide de la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) .</span><span class="sxs-lookup"><span data-stu-id="16054-116">You can obtain a textual description of the most recent MCI error message by using the [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) macro.</span></span> <span data-ttu-id="16054-117">Cette macro retourne le texte dans une mémoire tampon définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="16054-117">This macro returns the text in an application-defined buffer.</span></span> <span data-ttu-id="16054-118">Si la chaîne d’erreur est plus longue que la mémoire tampon, MCIWnd tronque la chaîne.</span><span class="sxs-lookup"><span data-stu-id="16054-118">If the error string is longer than the buffer, MCIWnd truncates the string.</span></span>

<span data-ttu-id="16054-119">Vous pouvez acheminer toutes les notifications vers une autre fenêtre à l’aide de la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="16054-119">You can route all notifications to another window by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>

 

 