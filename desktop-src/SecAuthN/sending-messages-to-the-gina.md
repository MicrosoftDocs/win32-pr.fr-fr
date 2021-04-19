---
description: Winlogon envoie des messages au GINA lorsque des boîtes de dialogue s’affichent. Ces messages sont tous encapsulés dans le \_ message wlx WM \_ SAS comme suit.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Envoi de messages au GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517824"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="79a4d-104">Envoi de messages au GINA</span><span class="sxs-lookup"><span data-stu-id="79a4d-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="79a4d-105">[*Winlogon*](../secgloss/w-gly.md) envoie des messages au [*Gina*](../secgloss/g-gly.md) lorsque des boîtes de dialogue s’affichent.</span><span class="sxs-lookup"><span data-stu-id="79a4d-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="79a4d-106">Ces messages sont tous encapsulés dans le \_ message wlx WM \_ SAS comme suit.</span><span class="sxs-lookup"><span data-stu-id="79a4d-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="79a4d-107">Type de séquence de vigilance sécurisée dans le paramètre wParam</span><span class="sxs-lookup"><span data-stu-id="79a4d-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="79a4d-108">Description</span><span class="sxs-lookup"><span data-stu-id="79a4d-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a4d-109">WLX \_ \_ type SAS \_ CTRL \_ Alt \_ Suppr</span><span class="sxs-lookup"><span data-stu-id="79a4d-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="79a4d-110">Indique qu’une séquence de touches CTRL + ALT + SUPPR a été reçue.</span><span class="sxs-lookup"><span data-stu-id="79a4d-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="79a4d-111">WLX \_ de \_ type SAS \_ SC \_ Insert</span><span class="sxs-lookup"><span data-stu-id="79a4d-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="79a4d-112">Indique qu’une [*carte à puce*](../secgloss/s-gly.md) a été insérée dans un appareil compatible.</span><span class="sxs-lookup"><span data-stu-id="79a4d-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="79a4d-113">\_type SAS \_ wlx \_ SC \_ Remove</span><span class="sxs-lookup"><span data-stu-id="79a4d-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="79a4d-114">Indique qu’une carte à puce a été supprimée d’un appareil compatible.</span><span class="sxs-lookup"><span data-stu-id="79a4d-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="79a4d-115">\_déconnexion \_ utilisateur du type SAS \_ wlx \_</span><span class="sxs-lookup"><span data-stu-id="79a4d-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="79a4d-116">Indique qu’un utilisateur a demandé la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="79a4d-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="79a4d-117">\_ \_ \_ \_ délai d’expiration du type SAS wlx SCRNSVR</span><span class="sxs-lookup"><span data-stu-id="79a4d-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="79a4d-118">Indique que l’économiseur d’écran doit être exécuté en raison de l’absence d’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79a4d-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="79a4d-119">\_ \_ \_ délai d’expiration du type SAS wlx</span><span class="sxs-lookup"><span data-stu-id="79a4d-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="79a4d-120">Indique qu’aucune entrée utilisateur n’a été reçue dans le délai d’attente spécifié.</span><span class="sxs-lookup"><span data-stu-id="79a4d-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="79a4d-121">Pour les délais d’attente et les dépassements, Winlogon ferme la boîte de dialogue une fois que le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="79a4d-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="79a4d-122">Ce message est envoyé de sorte que l’opération de la boîte de dialogue peut répondre de manière utile (par exemple, en se fermant à son tour si une déconnexion s’est produite).</span><span class="sxs-lookup"><span data-stu-id="79a4d-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="79a4d-123">Pour les délais d’attente d’entrée, la boîte de dialogue est fermée avec le code d' \_ \_ expiration d’entrée wlx DLG \_ .</span><span class="sxs-lookup"><span data-stu-id="79a4d-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="79a4d-124">Pour les délais d’expiration de l’économiseur d’écran, la boîte de dialogue est fermée avec le code WLX \_ DLG \_ \_ économiseur \_ d’écran Timeout.</span><span class="sxs-lookup"><span data-stu-id="79a4d-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="79a4d-125">Pour les fermetures de session, l’opération de la boîte de dialogue est fermée avec le code WLX \_ DLG \_ User \_ Logoff.</span><span class="sxs-lookup"><span data-stu-id="79a4d-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79a4d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79a4d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79a4d-127">Initialisation de Winlogon</span><span class="sxs-lookup"><span data-stu-id="79a4d-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="79a4d-128">États Winlogon</span><span class="sxs-lookup"><span data-stu-id="79a4d-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="79a4d-129">Opérations de Temps de service de boîte de dialogue prises en charge</span><span class="sxs-lookup"><span data-stu-id="79a4d-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="79a4d-130">Fonctions de prise en charge de Winlogon</span><span class="sxs-lookup"><span data-stu-id="79a4d-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
