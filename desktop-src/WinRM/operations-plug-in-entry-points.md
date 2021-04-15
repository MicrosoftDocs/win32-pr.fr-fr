---
title: Points d’entrée du plug-in opérations
description: Points d’entrée du plug-in opérations
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0834363c7447bc50269da09d361e630d9bc0615a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463159"
---
# <a name="operations-plug-in-entry-points"></a>Points d’entrée du plug-in opérations

Un plug-in d’opérations doit implémenter certains points d’entrée en fonction des fonctionnalités qu’il souhaite prendre en charge.

Un plug-in doit s’inscrire auprès du service Windows Remote Management (WinRM), qui contient les noms des points d’entrée de la DLL du plug-in. Toutes les opérations ont des points d’entrée de DLL prédéfinis qui doivent être exposés si cette opération est prise en charge.

Le tableau suivant fournit une vue d’ensemble des points d’entrée de plug-in d’opérations dans l’API de plug-in WinRM.



| Fonction                                                                                 | Description                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_commande du plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Définit le rappel de commande pour un plug-in.<br/> Tous les plug-ins WinRM qui prennent en charge les fonctionnalités de l’interpréteur de commandes doivent implémenter ce rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command).<br/> |
| [**\_connexion au plug-in WSMan \_**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Définit le rappel de connexion pour un plug-in.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginConnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect).<br/>                                                                                                |
| [**\_réception du plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Définit le rappel de réception pour un plug-in.<br/> Tous les plug-ins WinRM qui prennent en charge les fonctionnalités de l’interpréteur de commandes doivent implémenter ce rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginReceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive).<br/> |
| [**contexte de commande de mise en version du \_ plug-in WSMan \_ \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Définit le rappel de commande Release pour le plug-in.<br/> Le nom du point d’entrée de la DLL doit être [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                        |
| [**contexte d’environnement de la \_ version du plug-in WSMan \_ \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Définit le rappel de l’interpréteur de commandes Release pour le plug-in.<br/> Le nom du point d’entrée de la DLL doit être [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                          |
| [**\_envoi du plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Définit le rappel d’envoi pour un plug-in.<br/> Tous les plug-ins WinRM qui prennent en charge les fonctionnalités de l’interpréteur de commandes doivent implémenter ce rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginSend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send).<br/>          |
| [**\_Shell du plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Définit le rappel de l’interpréteur de commandes pour un plug-in.<br/> Tous les plug-ins WinRM qui prennent en charge les fonctionnalités de l’interpréteur de commandes doivent implémenter ce rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell).<br/>       |
| [**\_arrêt du plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Définit le rappel d’arrêt pour le plug-in.<br/> Tous les plug-ins WinRM doivent implémenter cette fonction de rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown).<br/>                      |
| [**\_signal du plug-in WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Définit le rappel de signal pour un plug-in.<br/> Tous les plug-ins WinRM qui prennent en charge les fonctionnalités de l’interpréteur de commandes doivent implémenter ce rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginSignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal).<br/>    |
| [**\_démarrage du plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Définit le rappel de démarrage pour le plug-in.<br/> Tous les plug-ins WinRM doivent implémenter cette fonction de rappel.<br/> Le nom du point d’entrée de la DLL pour cette méthode doit être [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).<br/>                         |



 

 

