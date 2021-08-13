---
title: Référence managée pour les classes de commandes Windows PowerShell WinRM
description: Windows la gestion à distance 2,0 (WinRM) peut utiliser des applets de commande Windows PowerShell pour la gestion du système. les applets de commande Windows PowerShell permettent à un administrateur de configurer WinRM et d’extraire des données ou de gérer des ressources.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- ConnectWSManCommand
- DisableWSManCredSSPCommand
- DisconnectWSManCommand
- EnableWSManCredSSPCommand
- GetWSManCredSSPCommand
- GetWSManInstanceCommand
- InvokeWSManActionCommand
- NewWSManInstanceCommand
- NewWSManSessionOptionCommand
- RemoveWSManInstanceCommand
- SetWSManInstanceCommand
- SetWSManQuickConfigCommand
- TestWSManCommand
- SessionOption
- AuthentificationMécanisme
- ProxyAccessType
- ProxyAuthentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d20a7615be5180350153596502386c9eac7c0c6820442284a717161ee1283e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412449"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Référence managée pour les classes de commandes Windows PowerShell WinRM

Windows la gestion à distance 2,0 (WinRM) peut utiliser des applets de commande Windows PowerShell pour la gestion du système. les applets de commande Windows PowerShell permettent à un administrateur de configurer WinRM et d’extraire des données ou de gérer des ressources.

les applets de commande Windows PowerShell pour winrm offrent les mêmes fonctionnalités que l’utilitaire de ligne de commande winrm. toutefois, Windows PowerShell effectue également les opérations suivantes :

-   Automatise les tâches WinRM dans un langage de script extensible et orienté gestion.
-   Fournit un outil unique pour toutes les tâches de gestion.

pour plus d’informations, consultez [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

## <a name="ws-management-windows-powershell-classes"></a>WS-Management les Classes Windows PowerShell

**Espace de noms**: Microsoft. WsMan. Management

**Assembly**: System. Management. Automation

Les classes de commande WinRM suivantes sont implémentées par Windows PowerShell. Ces classes sont incluses dans ce kit de développement logiciel (SDK) à des fins d’exhaustivité uniquement. Les membres de ces classes ne peuvent pas être utilisés directement et doivent être utilisés pour dériver d’autres classes.



| Classe                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConnectWSManCommand          | Se connecte au service WinRM sur un ordinateur distant. <br/> pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Connecter-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                              |
| DisableWSManCredSSPCommand   | Désactive l’authentification CredSSP sur un client.<br/> Pour plus d’informations sur les paramètres et pour obtenir des exemples, consultez l’applet de commande [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                           |
| DisconnectWSManCommand       | Se déconnecte du service WinRM sur un ordinateur distant. <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Disconnect-WSMan](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                      |
| EnableWSManCredSSPCommand    | Active l’authentification CredSSP sur le client.<br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                               |
| GetWSManCredSSPCommand       | Obtient la configuration liée à CredSSP pour le client.<br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                         |
| GetWSManInstanceCommand      | Affiche les informations de gestion d'une instance de ressource spécifiée par un URI de ressource.<br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                          |
| InvokeWSManActionCommand     | Appelle une action sur l’objet cible spécifié par l’URI de ressource et les sélecteurs. <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Invoke-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                         |
| NewWSManInstanceCommand      | Crée une instance d'une ressource de gestion. <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [New-WSManInstance](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                             |
| NewWSManSessionOptionCommand | crée une table de hachage de l’option de Session WinRM à utiliser comme paramètres d’entrée pour les applets de commande WSMan suivantes : [WSManInstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true), [Set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true), [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)et [Connecter-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true). <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) .<br/> |
| RemoveWSManInstanceCommand   | Supprime une instance de ressource de gestion. <br/> Consultez l’applet de commande [Remove-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true) pour obtenir des exemples et des informations détaillées sur les paramètres.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| SetWSManInstanceCommand      | Modifie les informations de gestion liées à une ressource. <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Set-WSManInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                       |
| SetWSManQuickConfigCommand   | Configure l'ordinateur local pour la gestion à distance. <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Set-WSManQuickConfig](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                      |
| TestWSManCommand             | Teste si le service WinRM est en cours d'exécution sur un ordinateur local ou distant. <br/> Pour obtenir des exemples et des informations détaillées sur les paramètres, consultez l’applet de commande [Test-WSMan]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | Définit un ensemble d'options étendues pour la session WS-Management.<br/> pour obtenir des exemples et des informations détaillées sur les valeurs possibles, consultez l’applet de commande [Connecter-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>énumérations de Windows PowerShell WS-Management

Les énumérations suivantes sont implémentées par Windows PowerShell. Ces énumérations sont incluses dans ce kit de développement logiciel (SDK) à des fins d’exhaustivité uniquement.



| Énumération             | Description                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AuthentificationMécanisme | Spécifie le mécanisme d’authentification à utiliser au niveau du serveur. <br/> pour obtenir des exemples et des informations détaillées sur les valeurs possibles, consultez l’applet de commande [Connecter-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) .<br/>      |
| ProxyAccessType         | Spécifie le mécanisme par lequel le serveur proxy est trouvé.<br/> Pour obtenir des exemples et des informations détaillées sur les valeurs possibles, consultez l’applet de commande [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) .<br/> |
| ProxyAuthentication     | Spécifie la méthode d'authentification à utiliser au niveau du proxy.<br/> Pour obtenir des exemples et des informations détaillées sur les valeurs possibles, consultez l’applet de commande [New-WSManSessionOption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) .<br/>      |



 

 

