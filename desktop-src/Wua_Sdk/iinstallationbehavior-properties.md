---
description: L’interface IInstallationBehavior définit les propriétés suivantes.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Propriétés IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951233"
---
# <a name="iinstallationbehavior-properties"></a><span data-ttu-id="5a463-103">Propriétés IInstallationBehavior</span><span class="sxs-lookup"><span data-stu-id="5a463-103">IInstallationBehavior Properties</span></span>

<span data-ttu-id="5a463-104">L’interface [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a463-104">The [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) interface defines the following properties.</span></span>



| <span data-ttu-id="5a463-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="5a463-105">Property</span></span>                                                                                 | <span data-ttu-id="5a463-106">Description</span><span class="sxs-lookup"><span data-stu-id="5a463-106">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a463-107">**CanRequestUserInput**</span><span class="sxs-lookup"><span data-stu-id="5a463-107">**CanRequestUserInput**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | <span data-ttu-id="5a463-108">Obtient une valeur booléenne thast indique si l’installation ou la désinstallation d’une mise à jour peut demander une entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a463-108">Gets a Boolean value thast indicates whether the installation or uninstallation of an update can prompt for user input.</span></span>                                                        |
| [<span data-ttu-id="5a463-109">**Impact**</span><span class="sxs-lookup"><span data-stu-id="5a463-109">**Impact**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | <span data-ttu-id="5a463-110">Obtient une énumération [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) qui indique comment l’installation ou la désinstallation de la mise à jour affecte l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5a463-110">Gets an [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) enumeration that indicates how the installation or uninstallation of the update affects the computer.</span></span>                 |
| [<span data-ttu-id="5a463-111">**RebootBehavior**</span><span class="sxs-lookup"><span data-stu-id="5a463-111">**RebootBehavior**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | <span data-ttu-id="5a463-112">Obtient une énumération [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) qui spécifie le comportement de redémarrage qui se produit lorsque vous installez ou désinstallez la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5a463-112">Gets an [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) enumeration that specifies the restart behavior that occurs when you install or uninstall the update.</span></span> |
| [<span data-ttu-id="5a463-113">**RequiresNetworkConnectivity**</span><span class="sxs-lookup"><span data-stu-id="5a463-113">**RequiresNetworkConnectivity**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | <span data-ttu-id="5a463-114">Obtient une valeur booléenne qui indique si l’installation ou la désinstallation d’une mise à jour requiert une connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="5a463-114">Gets a Boolean value that indicates whether the installation or uninstallation of an update requires network connectivity.</span></span>                                                     |



 

 

 



