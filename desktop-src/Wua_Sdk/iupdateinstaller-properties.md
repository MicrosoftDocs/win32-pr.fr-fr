---
description: L’interface IUpdateInstaller définit les propriétés suivantes.
ms.assetid: 876a2150-40a1-42a3-bc9a-05dec94fccd3
title: Propriétés IUpdateInstaller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77df235c49e7b6f27b0f93ec3b0c4def12135065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862794"
---
# <a name="iupdateinstaller-properties"></a>Propriétés IUpdateInstaller

L’interface [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) définit les propriétés suivantes.



| Propriété                                                                                      | Description                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowSourcePrompts**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_allowsourceprompts)                             | Obtient et définit une valeur booléenne qui indique s’il faut afficher les invites de la source à l’utilisateur lors de l’installation des mises à jour.                  |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_clientapplicationid)                           | Obtient et définit l’application cliente actuelle.                                                                                         |
| [**IsBusy**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isbusy)                                                     | Obtient une valeur booléenne qui indique si une installation ou une désinstallation est en cours sur un ordinateur à un moment donné.        |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_isforced)                                                 | Obtient ou définit une valeur booléenne qui indique s’il faut ou non forcer l’installation ou la désinstallation d’une mise à jour.                                       |
| [**ParentHwnd**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parenthwnd)                                             | Obtient et définit un handle vers la fenêtre parente qui peut contenir une boîte de dialogue.                                                            |
| [**FenêtreParent**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_parentwindow)                                         | Obtient et définit l’interface qui représente la fenêtre parente qui peut contenir une boîte de dialogue.                                          |
| [**RebootRequiredBeforeInstallation**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_rebootrequiredbeforeinstallation) | Obtient une valeur booléenne qui indique si un redémarrage du système est nécessaire avant d’installer ou de désinstaller des mises à jour.                   |
| [**Mises à jour**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-get_updates)                                                   | Obtient et définit une interface qui contient une collection en lecture seule des mises à jour spécifiées pour l’installation ou la désinstallation. |



 

 

 



