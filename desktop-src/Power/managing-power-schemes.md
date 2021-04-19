---
description: Gestion du mode de gestion de l’alimentation
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gestion du mode de gestion de l’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517705"
---
# <a name="power-scheme-management"></a><span data-ttu-id="94ba0-103">Gestion du mode de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="94ba0-103">Power Scheme Management</span></span>

<span data-ttu-id="94ba0-104">Chaque mode de gestion de l’alimentation est identifié de manière unique par un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="94ba0-104">Each power scheme is uniquely identified by a **GUID**.</span></span> <span data-ttu-id="94ba0-105">Pour énumérer tous les modes de gestion de l’alimentation disponibles, utilisez la fonction [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) .</span><span class="sxs-lookup"><span data-stu-id="94ba0-105">To enumerate all available power schemes, use the [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) function.</span></span> <span data-ttu-id="94ba0-106">**PowerEnumerate** peut également être utilisé pour récupérer tous les paramètres d’alimentation pour un schéma spécifié.</span><span class="sxs-lookup"><span data-stu-id="94ba0-106">**PowerEnumerate** can also be used to retrieve all of the power settings for a specified scheme.</span></span>

<span data-ttu-id="94ba0-107">Le mode de gestion de l’alimentation en cours d’utilisation sur le système est appelé mode de gestion de l’alimentation ou plan actif.</span><span class="sxs-lookup"><span data-stu-id="94ba0-107">The power scheme that is currently in use on the system is called the active power scheme or plan.</span></span> <span data-ttu-id="94ba0-108">Pour récupérer le **GUID** du plan actif, appelez la fonction [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="94ba0-108">To retrieve the **GUID** of the active plan, call the [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) function.</span></span> <span data-ttu-id="94ba0-109">Pour modifier le mode de gestion de l’alimentation actif, appelez la fonction [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .</span><span class="sxs-lookup"><span data-stu-id="94ba0-109">To change the active power plan, call the [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) function.</span></span>

<span data-ttu-id="94ba0-110">Pour créer un mode de gestion de l’alimentation, vous devez d’abord dupliquer un schéma existant à l’aide de la fonction [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , en spécifiant le **GUID** du schéma sur lequel vous souhaitez baser votre nouveau schéma.</span><span class="sxs-lookup"><span data-stu-id="94ba0-110">To create a power scheme, you need to first duplicate an existing scheme by using the [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) function, specifying the **GUID** of the scheme you wish to base your new scheme upon.</span></span> <span data-ttu-id="94ba0-111">Vous devez copier l’un des schémas intégrés et modifier les paramètres d’alimentation selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="94ba0-111">You should copy one of the built-in schemes and modify the power settings to your needs.</span></span> <span data-ttu-id="94ba0-112">Notez que la création d’un mode de gestion de l’alimentation ne met pas automatiquement à jour le mode de gestion de l’alimentation actif.</span><span class="sxs-lookup"><span data-stu-id="94ba0-112">Note that creating a power plan does not automatically update the active power plan.</span></span> <span data-ttu-id="94ba0-113">Vous devez toujours appeler [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) pour mettre à jour le mode de gestion de l’alimentation actif.</span><span class="sxs-lookup"><span data-stu-id="94ba0-113">You must always call [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) to update the active power plan.</span></span> <span data-ttu-id="94ba0-114">Les modes de gestion de l’alimentation existants peuvent être modifiés, puis appliqués de la même manière.</span><span class="sxs-lookup"><span data-stu-id="94ba0-114">Existing power plans can be modified and then applied in the same manner.</span></span>

<span data-ttu-id="94ba0-115">Pour supprimer un mode de gestion de l’alimentation, appelez la fonction [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .</span><span class="sxs-lookup"><span data-stu-id="94ba0-115">To remove a power plan, call the [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) function.</span></span>

> [!Note]  
> <span data-ttu-id="94ba0-116">Pour récupérer des informations supplémentaires sur l’état d’alimentation du système, appelez la fonction [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .</span><span class="sxs-lookup"><span data-stu-id="94ba0-116">To retrieve additional information about the system power state, call the [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94ba0-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94ba0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94ba0-118">Modes de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="94ba0-118">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 



