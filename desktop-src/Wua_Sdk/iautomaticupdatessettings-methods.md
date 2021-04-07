---
description: L’interface IAutomaticUpdatesSettings définit les méthodes suivantes.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Méthodes IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863746"
---
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="697c9-103">Méthodes IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="697c9-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="697c9-104">L’interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) définit les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="697c9-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="697c9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="697c9-105">Method</span></span>                                               | <span data-ttu-id="697c9-106">Description</span><span class="sxs-lookup"><span data-stu-id="697c9-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="697c9-107">**Actualiser**</span><span class="sxs-lookup"><span data-stu-id="697c9-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="697c9-108">Récupère les derniers paramètres de Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="697c9-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="697c9-109">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="697c9-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="697c9-110">Applique les paramètres de Mises à jour automatiques actuels.</span><span class="sxs-lookup"><span data-stu-id="697c9-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="697c9-111">Sur Windows RT, vous ne pouvez plus utiliser la méthode [**IAutomaticUpdatesSettings :: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) pour configurer des paramètres de Windows Update par programmation.</span><span class="sxs-lookup"><span data-stu-id="697c9-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="697c9-112">L’opération de configuration échoue si vous utilisez **Save** pour définir une valeur autre que 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span><span class="sxs-lookup"><span data-stu-id="697c9-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



