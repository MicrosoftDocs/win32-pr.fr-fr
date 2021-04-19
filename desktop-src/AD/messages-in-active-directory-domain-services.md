---
title: Messages dans Active Directory Domain Services
description: Les messages dans Active Directory Domain Services sont fonctionnels dans Windows 2000 et Windows NT 4,0 avec Service Pack 6A (SP6a) et versions ultérieures avec DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Messages d’Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510188"
---
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="adb67-104">Messages dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="adb67-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="adb67-105">Les messages dans Active Directory Domain Services sont fonctionnels dans Windows 2000 et Windows NT 4,0 avec Service Pack 6A (SP6a) et versions ultérieures avec DSClient.</span><span class="sxs-lookup"><span data-stu-id="adb67-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="adb67-106">Ils sont également fonctionnels dans les stations de travail Windows 98/95 avec IE 4.01 et versions ultérieures et DSClient.</span><span class="sxs-lookup"><span data-stu-id="adb67-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="adb67-107">Toutefois, si les pages de propriétés multisélections sont lancées à partir de l’interpréteur de commandes, le message d' [**erreur de \_ \_ notification \_ WM ADSPROP**](wm-adsprop-notify-error.md) et les fonctions d’assistance correspondantes, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) et [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) ne sont pas fonctionnels et ne s’affichent pas.</span><span class="sxs-lookup"><span data-stu-id="adb67-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="adb67-108">Si les pages de propriétés multisélections sont lancées au sein d’un outil d’administration, par exemple, utilisateurs et ordinateurs Active Directory, tous les messages sont fonctionnels et disponibles pour être affichés dans les pages de propriétés multisélections.</span><span class="sxs-lookup"><span data-stu-id="adb67-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="adb67-109">Active Directory Domain Services utiliser les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="adb67-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="adb67-110">**\_demande de \_ notification WM ADSPROP \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="adb67-111">**notification de modification de la \_ notification WM ADSPROP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="adb67-112">**\_erreur de \_ notification WM ADSPROP \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="adb67-113">**notification de la sortie de \_ ADSPROP WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="adb67-114">**WM \_ ADSPROP \_ Notify \_ premier plan**</span><span class="sxs-lookup"><span data-stu-id="adb67-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="adb67-115">**WM \_ ADSPROP \_ Notify \_ PAGEHWND**</span><span class="sxs-lookup"><span data-stu-id="adb67-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="adb67-116">**WM \_ ADSPROP \_ Notify \_ PAGEINIT**</span><span class="sxs-lookup"><span data-stu-id="adb67-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="adb67-117">**WM \_ ADSPROP \_ Notify \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="adb67-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="adb67-118">**création de la \_ feuille ADSPROP WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="adb67-119">**notification de fermeture de la \_ feuille du DSA WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="adb67-120">**créer une notification de la \_ feuille DSA DSA \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="adb67-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




