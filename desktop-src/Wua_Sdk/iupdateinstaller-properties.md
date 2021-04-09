---
description: L’interface IUpdateInstaller définit les propriétés suivantes.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propriétés IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862794"
---
# <a name="iupdateinstaller-properties"></a><span data-ttu-id="90dd4-103">Propriétés IUpdateInstaller</span><span class="sxs-lookup"><span data-stu-id="90dd4-103">IUpdateInstaller Properties</span></span>

<span data-ttu-id="90dd4-104">L’interface [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="90dd4-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following properties.</span></span>



| <span data-ttu-id="90dd4-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="90dd4-105">Property</span></span>                                                                                      | <span data-ttu-id="90dd4-106">Description</span><span class="sxs-lookup"><span data-stu-id="90dd4-106">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90dd4-107">**AllowSourcePrompts**</span><span class="sxs-lookup"><span data-stu-id="90dd4-107">**AllowSourcePrompts**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | <span data-ttu-id="90dd4-108">Obtient et définit une valeur booléenne qui indique s’il faut afficher les invites de la source à l’utilisateur lors de l’installation des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="90dd4-108">Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.</span></span>                  |
| [<span data-ttu-id="90dd4-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="90dd4-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | <span data-ttu-id="90dd4-110">Obtient et définit l’application cliente actuelle.</span><span class="sxs-lookup"><span data-stu-id="90dd4-110">Gets and sets the current client application.</span></span>                                                                                         |
| [<span data-ttu-id="90dd4-111">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="90dd4-111">**IsBusy**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | <span data-ttu-id="90dd4-112">Obtient une valeur booléenne qui indique si une installation ou une désinstallation est en cours sur un ordinateur à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="90dd4-112">Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.</span></span>        |
| [<span data-ttu-id="90dd4-113">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="90dd4-113">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | <span data-ttu-id="90dd4-114">Obtient ou définit une valeur booléenne qui indique s’il faut ou non forcer l’installation ou la désinstallation d’une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="90dd4-114">Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.</span></span>                                       |
| [<span data-ttu-id="90dd4-115">**ParentHwnd**</span><span class="sxs-lookup"><span data-stu-id="90dd4-115">**ParentHwnd**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | <span data-ttu-id="90dd4-116">Obtient et définit un handle vers la fenêtre parente qui peut contenir une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90dd4-116">Gets and sets a handle to the parent window that can contain a dialog box.</span></span>                                                            |
| [<span data-ttu-id="90dd4-117">**FenêtreParent**</span><span class="sxs-lookup"><span data-stu-id="90dd4-117">**ParentWindow**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | <span data-ttu-id="90dd4-118">Obtient et définit l’interface qui représente la fenêtre parente qui peut contenir une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90dd4-118">Gets and sets the interface that represents the parent window that can contain a dialog box.</span></span>                                          |
| [<span data-ttu-id="90dd4-119">**RebootRequiredBeforeInstallation**</span><span class="sxs-lookup"><span data-stu-id="90dd4-119">**RebootRequiredBeforeInstallation**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | <span data-ttu-id="90dd4-120">Obtient une valeur booléenne qui indique si un redémarrage du système est nécessaire avant d’installer ou de désinstaller des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="90dd4-120">Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.</span></span>                   |
| [<span data-ttu-id="90dd4-121">**Mises à jour**</span><span class="sxs-lookup"><span data-stu-id="90dd4-121">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | <span data-ttu-id="90dd4-122">Obtient et définit une interface qui contient une collection en lecture seule des mises à jour spécifiées pour l’installation ou la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="90dd4-122">Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.</span></span> |



 

 

 



