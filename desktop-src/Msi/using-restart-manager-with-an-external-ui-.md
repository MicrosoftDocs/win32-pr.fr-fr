---
description: Windows Installer les développeurs peuvent préparer leur package d’installation pour qu’ils fonctionnent avec le gestionnaire de redémarrage en suivant les instructions décrites dans utilisation de Windows Installer avec le gestionnaire de redémarrage.
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: Utilisation du gestionnaire de redémarrage avec une interface utilisateur externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f112884669b173b40f3806c48cf8e05308c5b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201466"
---
# <a name="using-restart-manager-with-an-external-ui"></a>Utilisation du gestionnaire de redémarrage avec une interface utilisateur externe

Windows Installer les développeurs peuvent préparer leur package d’installation pour qu’ils fonctionnent avec le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) en suivant les instructions décrites dans [utilisation de Windows Installer avec le gestionnaire de redémarrage](using-windows-installer-with-restart-manager.md).

Spécifiez le \_ type de message INSTALLLOGMODE RMFILESINUSE lors de l’appel de la fonction [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) ou [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) pour activer le gestionnaire d’interface utilisateur externe. Windows Installer envoie ensuite un \_ message INSTALLMESSAGE RMFILESINUSE pour une utilisation par des gestionnaires d’interface utilisateur externes qui prennent en charge le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md).

Votre gestionnaire d’interface utilisateur externe doit gérer les informations contenues dans les \_ messages INSTALLMESSAGE RMFILESINUSE. Si aucune interface utilisateur inscrite ou interne ne gère le \_ message INSTALLMESSAGE RMFILESINUSE, Windows Installer envoie un \_ message INSTALLMESSAGE FILESINUSE pour une utilisation par des gestionnaires externes existants qui prennent en charge \_ les messages INSTALLMESSAGE FILESINUSE et la boîte de dialogue [FILESINUSE](filesinuse-dialog.md) .

L’interface utilisateur externe peut retourner les valeurs indiquées dans le tableau suivant.



| Valeur de retour de l’interface utilisateur externe | Action entreprise par Windows Installer                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | L’utilisateur a cliqué sur le bouton **OK** . Le Windows Installer demande que le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) s’arrête et redémarre les applications qui contiennent les fichiers en cours d’utilisation.                                                                                                                                               |
| IDCANCEL                 | Le bouton **Annuler** a été enfoncé. Annulez l’installation.                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | L’utilisateur a cliqué sur le bouton **Ignorer** . Ignorer et continuer l’installation. Un redémarrage sera nécessaire à la fin de l’installation.                                                                                                                                                                                                            |
| IDNO                     | Le bouton **non** a été enfoncé. Si le package possède une boîte de dialogue [MsiRMFilesInUse](msirmfilesinuse-dialog.md) , envoyez un message 1610. Pour plus d’informations, consultez [Windows Installer des messages d’erreur](windows-installer-error-messages.md). Si le package n’a pas de boîte de dialogue MsiRMFilesInUse, envoyez un \_ message INSTALLMESSAGE FILESINUSE. |
| IDRETRY                  | Le bouton **Réessayer** a été enfoncé. Envoyez le \_ message INSTALLMESSAGE FILESINUSE.                                                                                                                                                                                                                                                                 |
| -1                       | Une erreur. Mettez fin à l’installation.                                                                                                                                                                                                                                                                                                                |



 

 

 
