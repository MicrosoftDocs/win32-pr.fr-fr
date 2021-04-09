---
description: La structure COMMCONFIG définit la configuration d’une ressource de communication, en série ou dans le cas contraire.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuration des ressources de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110702"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="15c34-103">Configuration des ressources de communication</span><span class="sxs-lookup"><span data-stu-id="15c34-103">Communications Resource Configuration</span></span>

<span data-ttu-id="15c34-104">La structure [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) définit la configuration d’une ressource de communication, en série ou dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="15c34-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="15c34-105">Le format de la structure varie selon le type de ressource de communication (le sous-type de fournisseur).</span><span class="sxs-lookup"><span data-stu-id="15c34-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="15c34-106">Les premiers membres de la structure sont communs à toutes les ressources de communication ; des membres supplémentaires sont définis pour des sous-types de fournisseur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="15c34-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="15c34-107">Les fournisseurs de services spécifiques peuvent également étendre la structure **COMMCONFIG** .</span><span class="sxs-lookup"><span data-stu-id="15c34-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="15c34-108">Une application peut obtenir et définir la configuration d’une ressource de communication à l’aide des fonctions [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) et [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) .</span><span class="sxs-lookup"><span data-stu-id="15c34-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="15c34-109">Une fois ouverte, une ressource de communication est initialisée à l’aide de la configuration par défaut pour son sous-type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="15c34-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="15c34-110">Pour obtenir et définir la configuration par défaut d’un sous-type de fournisseur, utilisez les fonctions [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) et [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .</span><span class="sxs-lookup"><span data-stu-id="15c34-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="15c34-111">Pour inviter l’utilisateur à fournir des informations de configuration, utilisez la fonction [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) .</span><span class="sxs-lookup"><span data-stu-id="15c34-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="15c34-112">Cette fonction affiche une boîte de dialogue définie par le fournisseur de services et remplit une structure [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) en fonction de l’entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15c34-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



