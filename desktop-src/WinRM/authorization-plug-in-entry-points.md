---
title: Points d’entrée du plug-in d’autorisation
description: Points d’entrée du plug-in d’autorisation
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee0db76457860106e51bd6c29cead3d0f8227d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510089"
---
# <a name="authorization-plug-in-entry-points"></a>Points d’entrée du plug-in d’autorisation

Les plug-ins d’autorisation sont configurés uniquement pour un processus hôte Internet Information Services (IIS). Un seul plug-in d’autorisation peut être configuré par répertoire virtuel.

Tous les plug-ins d’autorisation doivent prendre en charge les points d’entrée suivants :

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

Le point d’entrée suivant est facultatif :

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

Le tableau suivant fournit une vue d’ensemble des points d’entrée du plug-in d’autorisation dans l’API de plug-in Windows Remote Management (WinRM).



| Fonction                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**opération d’autorisation du plug- \_ in WSMan \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Appelé pour autoriser une opération spécifique. <br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).<br/>                                                                                                                                                                                                       |
| [**\_autorisation du plug-in wsman Autoriser le \_ \_ quota de requêtes \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Appelé après qu’une connexion a été autorisée à récupérer les informations de quota pour l’utilisateur. <br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).<br/>                                                                                                                                                    |
| [**\_contexte de \_ mise en \_ version autorisée du plug-in WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Appelé pour libérer le contexte qu’un plug-in signale à partir des méthodes [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) ou [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) . <br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginAuthzReleaseContext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).<br/> |
| [**\_ \_ utilisateur autorisé pour le plug-in WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Appelé pour déterminer si l’utilisateur est autorisé à effectuer une requête. <br/> Le nom du point d’entrée de la bibliothèque de liens dynamiques (DLL) de cette méthode doit être [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).<br/>                                                                                                                                                            |



 

 

