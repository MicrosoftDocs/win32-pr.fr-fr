---
description: Winlogon met en œuvre deux opérations de délai d’attente, une pour les boîtes de dialogue sécurisées et l’autre pour l’activation et l’arrêt de l’écran de veille.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Opérations de Temps de service de boîte de dialogue prises en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751668"
---
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="02e58-103">Opérations de Temps de service de boîte de dialogue prises en charge</span><span class="sxs-lookup"><span data-stu-id="02e58-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="02e58-104">[*Winlogon*](../secgloss/w-gly.md) met en œuvre deux opérations de délai d’attente, une pour les boîtes de dialogue sécurisées et l’autre pour l’activation et l’arrêt de l’écran de veille.</span><span class="sxs-lookup"><span data-stu-id="02e58-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="02e58-105">Lorsque vous affichez une boîte de dialogue sécurisée, telle que l’ouverture ou le déverrouillage d’une station de travail, Winlogon peut expirer les boîtes de dialogue et retourner un code de résultat approprié à la procédure de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="02e58-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="02e58-106">Winlogon fournit un ensemble de fonctions de prise en charge de boîte de dialogue pour [*Gina*](../secgloss/g-gly.md).</span><span class="sxs-lookup"><span data-stu-id="02e58-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="02e58-107">La GINA doit utiliser ces fonctions au lieu de leurs équivalents Windows pour s’assurer que la GINA et Winlogon maintiennent le contrôle approprié sur les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="02e58-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="02e58-108">Si vous n’utilisez pas les versions Winlogon de ces fonctions, les utilisateurs non autorisés peuvent accéder au système.</span><span class="sxs-lookup"><span data-stu-id="02e58-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="02e58-109">Les services de boîte de dialogue Winlogon sont fournis par les fonctions de prise en charge suivantes.</span><span class="sxs-lookup"><span data-stu-id="02e58-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="02e58-110">Fonction de prise en charge</span><span class="sxs-lookup"><span data-stu-id="02e58-110">Support function</span></span>                                               | <span data-ttu-id="02e58-111">Description</span><span class="sxs-lookup"><span data-stu-id="02e58-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02e58-112">**WlxMessageBox**</span><span class="sxs-lookup"><span data-stu-id="02e58-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="02e58-113">Semblable à la fonction Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) .</span><span class="sxs-lookup"><span data-stu-id="02e58-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="02e58-114">**WlxDialogBox**</span><span class="sxs-lookup"><span data-stu-id="02e58-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="02e58-115">Semblable à la fonction Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="02e58-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="02e58-116">**WlxDialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="02e58-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="02e58-117">Semblable à la fonction [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) de Windows.</span><span class="sxs-lookup"><span data-stu-id="02e58-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="02e58-118">**WlxDialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="02e58-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="02e58-119">Semblable à la fonction [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) de Windows.</span><span class="sxs-lookup"><span data-stu-id="02e58-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="02e58-120">**WlxDialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="02e58-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="02e58-121">Semblable à la fonction [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) de Windows.</span><span class="sxs-lookup"><span data-stu-id="02e58-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="02e58-122">Les DLL GINA peuvent également recevoir \_ \_ des messages wlx WM SAS de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="02e58-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="02e58-123">Ces messages sont envoyés aux boîtes de dialogue actives si une [*séquence d’intervention sécurisée*](../secgloss/s-gly.md) (SAS) est reçue.</span><span class="sxs-lookup"><span data-stu-id="02e58-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="02e58-124">Cela est utile si la GINA est en train de demander le code PIN correspondant pour une [*carte à puce*](../secgloss/s-gly.md)et que la carte est supprimée du [*lecteur*](../secgloss/r-gly.md)de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="02e58-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="02e58-125">Winlogon utilise WLX \_ DLG \_ SAS comme code de résultat EndDialog lorsqu’un événement SAS se produit pendant une opération de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="02e58-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="02e58-126">Les délais d’attente sont également fournis de cette manière.</span><span class="sxs-lookup"><span data-stu-id="02e58-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="02e58-127">Un \_ message wlx WM \_ wlx est envoyé avec un \_ \_ \_ \_ délai d’expiration du type SAS SCRNSVR ou un délai \_ \_ d’expiration du type SAS wlx \_ .</span><span class="sxs-lookup"><span data-stu-id="02e58-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="02e58-128">La boîte de dialogue se termine par un code de sortie approprié pour permettre aux développeurs GINA de raccorder les notifications de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="02e58-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="02e58-129">Les boîtes de dialogue GINA peuvent être arrêtées par Winlogon à l’aide du code WLX \_ DLG \_ User \_ Logoff.</span><span class="sxs-lookup"><span data-stu-id="02e58-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="02e58-130">Cela indique que l’utilisateur s’est déconnecté lors de l’exécution de la boîte de dialogue (par exemple, en appelant la fonction [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) à partir d’un autre thread).</span><span class="sxs-lookup"><span data-stu-id="02e58-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02e58-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02e58-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e58-132">Initialisation de Winlogon</span><span class="sxs-lookup"><span data-stu-id="02e58-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="02e58-133">États Winlogon</span><span class="sxs-lookup"><span data-stu-id="02e58-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="02e58-134">Envoi de messages au GINA</span><span class="sxs-lookup"><span data-stu-id="02e58-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="02e58-135">Fonctions de prise en charge de Winlogon</span><span class="sxs-lookup"><span data-stu-id="02e58-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
