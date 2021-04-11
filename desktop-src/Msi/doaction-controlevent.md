---
description: Le ControlEvent, de la transaction notifie le programme d’installation d’exécuter une action personnalisée. Cet événement peut être publié par un contrôle de bouton de commande, un contrôle de case à cocher ou un contrôle SelectionTree. Cet événement doit être créé dans la table ControlEvent,.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: Action ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112271"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="cb0ad-105">Action ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="cb0ad-105">DoAction ControlEvent</span></span>

<span data-ttu-id="cb0ad-106">Le ControlEvent, de la transaction notifie le programme d’installation d’exécuter une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cb0ad-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="cb0ad-107">Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md) de commande, un contrôle de [case à cocher](checkbox-control.md) ou un contrôle [SelectionTree](selectiontree-control.md) .</span><span class="sxs-lookup"><span data-stu-id="cb0ad-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="cb0ad-108">Cet événement doit être créé dans la table [ControlEvent,](controlevent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cb0ad-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="cb0ad-109">Notez que les actions personnalisées lancées par une action ControlEvent, peuvent envoyer un message avec la [**méthode de message**](session-message.md), mais ne peuvent pas envoyer de message avec [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="cb0ad-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="cb0ad-110">Sur les systèmes antérieurs à Windows Server 2003, les actions personnalisées lancées par une action ControlEvent, ne peuvent pas envoyer de messages avec **MsiProcessMessage** ou la **méthode de message**.</span><span class="sxs-lookup"><span data-stu-id="cb0ad-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="cb0ad-111">Pour plus d’informations, consultez [envoi de messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="cb0ad-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="cb0ad-112">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cb0ad-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="cb0ad-113">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cb0ad-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="cb0ad-114">Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cb0ad-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="cb0ad-115">Publié par</span><span class="sxs-lookup"><span data-stu-id="cb0ad-115">Published By</span></span>

<span data-ttu-id="cb0ad-116">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="cb0ad-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="cb0ad-117">Argument</span><span class="sxs-lookup"><span data-stu-id="cb0ad-117">Argument</span></span>

<span data-ttu-id="cb0ad-118">Chaîne, nom de l’action personnalisée à exécuter.</span><span class="sxs-lookup"><span data-stu-id="cb0ad-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="cb0ad-119">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="cb0ad-119">Action on Subscribers</span></span>

<span data-ttu-id="cb0ad-120">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="cb0ad-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="cb0ad-121">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="cb0ad-121">Typical Use</span></span>

<span data-ttu-id="cb0ad-122">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour appeler une action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="cb0ad-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



