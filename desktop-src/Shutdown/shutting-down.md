---
description: 'Il existe trois façons pour une application d’arrêter des ordinateurs locaux ou distants : Arrêtez le systemshut sur le système et redémarrez itshut l’application, arrêtez et redémarrez le système, puis redémarrez toutes les applications qui ont été inscrites pour le redémarrage'
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: Arrêt en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436dd9e3b115112e63b0440b4d51de4c7f9f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519527"
---
# <a name="shutting-down"></a>Arrêt en cours

Il existe trois façons pour une application d’arrêter des ordinateurs locaux ou distants :

-   arrêter le système
-   Arrêtez le système et redémarrez-le.
-   Arrêtez l’application, arrêtez et redémarrez le système, puis redémarrez toutes les applications qui ont été inscrites pour le redémarrage

Pour arrêter le système, utilisez la fonction [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) avec l’indicateur d' \_ arrêt EWX. Pour obtenir un exemple, consultez [Comment arrêter le système](how-to-shut-down-the-system.md). Pour arrêter et redémarrer le système, utilisez l’indicateur de \_ redémarrage EWX. Pour redémarrer toutes les applications qui ont été inscrites pour le redémarrage à l’aide de la fonction [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) , utilisez l' \_ indicateur EXW RESTARTAPPS.

Les fonctions [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna), [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)et [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) démarrent un minuteur et affichent une boîte de dialogue qui invite l’utilisateur à se déconnecter. Lorsque cette boîte de dialogue est affichée, la fonction [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) peut arrêter le minuteur et empêcher l’ordinateur de s’arrêter. Toutefois, si le minuteur expire, l’ordinateur est arrêté. Ces fonctions peuvent également redémarrer l’ordinateur après une opération d’arrêt. Pour plus d’informations, consultez [affichage de la boîte de dialogue d’arrêt](displaying-the-shutdown-dialog-box.md).

## <a name="shutdown-notifications"></a>Notifications d’arrêt

Les applications avec une fenêtre et la file d’attente de messages reçoivent des notifications d’arrêt par le biais des messages [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) et [**WM \_ ENDSESSION**](wm-endsession.md) . Ces applications doivent retourner la **valeur true** pour indiquer qu’elles peuvent être arrêtées. Les applications ne doivent pas bloquer l’arrêt du système, sauf si cela est absolument nécessaire. Les applications doivent effectuer tout nettoyage requis lors du traitement de **WM \_ ENDSESSION**. Les applications qui contiennent des données non enregistrées peuvent enregistrer les données dans un emplacement temporaire et les restaurer lors du prochain démarrage de l’application. Il est recommandé que les applications enregistrent fréquemment leurs données et leur état ; par exemple, enregistrez automatiquement les données entre les opérations d’enregistrement initiées par l’utilisateur pour réduire la quantité de données à enregistrer lors de l’arrêt.

Les applications console reçoivent des notifications d’arrêt dans leurs routines de gestionnaire. Pour inscrire un gestionnaire de console, utilisez la fonction [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) .

Les applications de service reçoivent des notifications d’arrêt dans leurs routines de gestionnaire. Pour inscrire un gestionnaire de contrôle des services, utilisez la fonction [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .

## <a name="blocking-shutdown"></a>Blocage de l’arrêt

Si une application doit bloquer un éventuel arrêt du système, elle peut appeler la fonction [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . L’appelant fournit une chaîne de raison qui sera affichée à l’utilisateur. La chaîne de raison doit être abrégée et claire, fournissant à l’utilisateur les informations nécessaires pour décider s’il faut poursuivre l’arrêt du système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment arrêter le système](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
