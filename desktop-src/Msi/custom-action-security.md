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
# <a name="custom-action-security"></a>Sécurité des actions personnalisées

Le programme d’installation exécute des actions personnalisées avec des privilèges d’utilisateur par défaut afin de limiter l’accès des actions personnalisées au système. Le programme d’installation peut exécuter des actions personnalisées avec des privilèges élevés si une application managée est en cours d’installation ou si la stratégie système a été spécifiée pour des privilèges élevés.

Vous devez utiliser la propriété [**MsiHiddenProperties**](msihiddenproperties.md) et **msidbCustomActionTypeHideTarget** pour empêcher la journalisation des informations sensibles utilisées par l’action personnalisée. Pour plus d’informations sur **msidbCustomActionTypeHideTarget** , consultez [option cible masquée des actions personnalisées](custom-action-hidden-target-option.md).

Désactivez la propriété CustomActionData après l’avoir définie pour s’assurer que les données sensibles ne sont plus disponibles. L’exemple de code ci-dessous est un extrait de code utilisé par une action personnalisée DLL immédiate qui configure des données pour une utilisation par une action personnalisée différée appelée « MyDeferredCA » :


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



Notez que seules les [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md) peuvent utiliser l’attribut **msidbCustomActionTypeNoImpersonate** . Pour plus d’informations, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

Si le bit **msidbCustomActionTypeNoImpersonate** n’est pas défini pour une action personnalisée, le programme d’installation exécute l’action personnalisée avec des privilèges au niveau de l’utilisateur. Pour plus d’informations, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).

Si le bit **msidbCustomActionTypeNoImpersonate** est défini et qu’une application managée est en cours d’installation avec l’autorisation administrateur, le programme d’installation peut exécuter l’action personnalisée avec des privilèges élevés. Toutefois, si un utilisateur tente d’installer l’application gérée sans autorisation d’administrateur, le programme d’installation exécute l’application avec des privilèges de niveau utilisateur, que **msidbCustomActionTypeNoImpersonate** soit défini ou non.

Notez qu’une action personnalisée peut s’exécuter avec des privilèges système même si le bit **msidbCustomActionTypeNoImpersonate** n’est pas défini. Cela se produit si un administrateur installe l’application pour tous les utilisateurs sur un serveur exécutant le service de rôle Terminal Server à l’aide de Windows 2000 et que l’action n’est pas marquée avec **msidbCustomActionTypeTSAware**. Une action personnalisée peut également s’exécuter avec des privilèges système si l’installation est appelée en l’absence de contexte utilisateur. Par exemple, s’il n’y a pas d’utilisateur actuellement connecté pendant une installation appelée par le déploiement d’applications Windows 2000.

Lorsque vous créez vos propres actions personnalisées, vous devez toujours créer l’action personnalisée à l’aide de méthodes sécurisées. Pour plus d’informations, consultez [instructions pour la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md).

 

 



