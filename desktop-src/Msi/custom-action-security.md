---
description: Le programme d’installation exécute des actions personnalisées avec des privilèges d’utilisateur par défaut afin de limiter l’accès des actions personnalisées au système.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Sécurité des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320881"
---
# <a name="custom-action-security"></a><span data-ttu-id="4e632-103">Sécurité des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="4e632-103">Custom Action Security</span></span>

<span data-ttu-id="4e632-104">Le programme d’installation exécute des actions personnalisées avec des privilèges d’utilisateur par défaut afin de limiter l’accès des actions personnalisées au système.</span><span class="sxs-lookup"><span data-stu-id="4e632-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="4e632-105">Le programme d’installation peut exécuter des actions personnalisées avec des privilèges élevés si une application managée est en cours d’installation ou si la stratégie système a été spécifiée pour des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="4e632-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="4e632-106">Vous devez utiliser la propriété [**MsiHiddenProperties**](msihiddenproperties.md) et **msidbCustomActionTypeHideTarget** pour empêcher la journalisation des informations sensibles utilisées par l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4e632-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="4e632-107">Pour plus d’informations sur **msidbCustomActionTypeHideTarget** , consultez [option cible masquée des actions personnalisées](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="4e632-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="4e632-108">Désactivez la propriété CustomActionData après l’avoir définie pour s’assurer que les données sensibles ne sont plus disponibles.</span><span class="sxs-lookup"><span data-stu-id="4e632-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="4e632-109">L’exemple de code ci-dessous est un extrait de code utilisé par une action personnalisée DLL immédiate qui configure des données pour une utilisation par une action personnalisée différée appelée « MyDeferredCA » :</span><span class="sxs-lookup"><span data-stu-id="4e632-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



<span data-ttu-id="4e632-110">Notez que seules les [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md) peuvent utiliser l’attribut **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="4e632-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="4e632-111">Pour plus d’informations, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="4e632-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="4e632-112">Si le bit **msidbCustomActionTypeNoImpersonate** n’est pas défini pour une action personnalisée, le programme d’installation exécute l’action personnalisée avec des privilèges au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e632-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="4e632-113">Pour plus d’informations, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="4e632-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="4e632-114">Si le bit **msidbCustomActionTypeNoImpersonate** est défini et qu’une application managée est en cours d’installation avec l’autorisation administrateur, le programme d’installation peut exécuter l’action personnalisée avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="4e632-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="4e632-115">Toutefois, si un utilisateur tente d’installer l’application gérée sans autorisation d’administrateur, le programme d’installation exécute l’application avec des privilèges de niveau utilisateur, que **msidbCustomActionTypeNoImpersonate** soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="4e632-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="4e632-116">Notez qu’une action personnalisée peut s’exécuter avec des privilèges système même si le bit **msidbCustomActionTypeNoImpersonate** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="4e632-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="4e632-117">Cela se produit si un administrateur installe l’application pour tous les utilisateurs sur un serveur exécutant le service de rôle Terminal Server à l’aide de Windows 2000 et que l’action n’est pas marquée avec **msidbCustomActionTypeTSAware**.</span><span class="sxs-lookup"><span data-stu-id="4e632-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="4e632-118">Une action personnalisée peut également s’exécuter avec des privilèges système si l’installation est appelée en l’absence de contexte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e632-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="4e632-119">Par exemple, s’il n’y a pas d’utilisateur actuellement connecté pendant une installation appelée par le déploiement d’applications Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4e632-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="4e632-120">Lorsque vous créez vos propres actions personnalisées, vous devez toujours créer l’action personnalisée à l’aide de méthodes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="4e632-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="4e632-121">Pour plus d’informations, consultez [instructions pour la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4e632-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



