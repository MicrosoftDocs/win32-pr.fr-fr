---
description: Montre comment utiliser les \_ API NotifyIcon Shell et Shell \_ NotifyIconGetRect pour afficher une icône de notification.
title: NotificationIcon, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973290"
---
# <a name="notificationicon-sample"></a>NotificationIcon, exemple

Montre comment utiliser les API [**\_ NotifyIcon Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) et [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) pour afficher une icône de notification.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="description"></a>Description

Outre l’utilisation de l' [**interface \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) et de l’interpréteur de commandes shell [**\_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) pour afficher une icône de notification, cet exemple montre également comment afficher une fenêtre complète, un menu contextuel et une notification de bulles.

> [!Note]  
> [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) est disponible uniquement sur Windows 7 et versions ultérieures.

 

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple NotificationIcon](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **NotificationIcon** .
2.  Entrez `msbuild NotificationIcon.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **NotificationIcon** .
2.  Double-cliquez sur l’icône du fichier NotificationIcon. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’Explorateur Windows.
2.  Sur la ligne de commande, entrez `NotificationIcon.exe` . Vous pouvez également, à partir de l’Explorateur Windows, double-cliquer sur l’icône de NotificationIcon.exe.

> [!Note]  
> Les icônes de notification spécifiées avec un GUID sont protégées contre l’usurpation en validant qu’une seule application les enregistre. Cette inscription est effectuée la première fois que vous appelez l’interface \_ NotifyIcon de l’interpréteur de commandes (NIM \_ Add,...) et le nom du chemin d’accès complet de l’application appelante est stocké. Si, par la suite, vous déplacez votre fichier binaire vers un emplacement différent, le système n’autorise pas l’ajout de l’icône. Pour plus d’informations, consultez [**\_ NotifyIcon de l’interpréteur**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) de commandes.

 

 

 



