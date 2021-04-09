---
description: L’interface IInstallationJob définit les propriétés suivantes.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Propriétés IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752093"
---
# <a name="iinstallationjob-properties"></a><span data-ttu-id="7508b-103">Propriétés IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="7508b-103">IInstallationJob Properties</span></span>

<span data-ttu-id="7508b-104">L’interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7508b-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="7508b-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="7508b-105">Property</span></span>                                            | <span data-ttu-id="7508b-106">Description</span><span class="sxs-lookup"><span data-stu-id="7508b-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7508b-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="7508b-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="7508b-108">Obtient l’objet d’état spécifique à l’appelant qui est passé à la méthode [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="7508b-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="7508b-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="7508b-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="7508b-110">Obtient une valeur qui indique si un appel à la méthode [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) est entièrement traité.</span><span class="sxs-lookup"><span data-stu-id="7508b-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="7508b-111">**Mises à jour**</span><span class="sxs-lookup"><span data-stu-id="7508b-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="7508b-112">Obtient une interface qui contient une collection en lecture seule des mises à jour spécifiées lors de l’installation ou de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="7508b-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 



