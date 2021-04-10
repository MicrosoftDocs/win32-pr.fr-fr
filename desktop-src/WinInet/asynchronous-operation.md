---
title: Opération asynchrone
description: En mode asynchrone, une application peut exécuter n’importe quelle fonction qui comprend une valeur de contexte comme l’un de ses paramètres et peut continuer à exécuter d’autres commandes ou fonctions pendant que l’application attend que la fonction termine sa tâche.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7e1d0cf84aa92691e1d926d771ea809d31a171
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728932"
---
# <a name="asynchronous-operation"></a>Opération asynchrone

Le temps nécessaire à une application pour accéder à une ressource Internet dépend de plusieurs facteurs, tels que la connexion utilisée, le serveur sur lequel se trouve la ressource et le nombre d’utilisateurs qui essaient d’accéder à la ressource. Pour les applications qui téléchargent plusieurs ressources ou qui gèrent plusieurs tâches (y compris un ou plusieurs téléchargements), l’attente de la fin de chaque téléchargement avant de passer à la tâche suivante peut être extrêmement inefficace. Pour réduire la durée d’attente d’une application, la plupart des fonctions WinINet peuvent fonctionner de manière asynchrone.

En mode asynchrone, une application peut exécuter n’importe quelle fonction qui comprend une valeur de contexte comme l’un de ses paramètres et peut continuer à exécuter d’autres commandes ou fonctions pendant que l’application attend que la fonction termine sa tâche. Pendant l’exécution de la tâche, une fonction de rappel d’État fournie par l’application est notifiée de la progression de la tâche et de la fin de son exécution. À ce stade, la fonction de rappel d’État peut appeler d’autres fonctions ou exécuter toute autre tâche requise qui dépendait de la fin de la tâche.

Il n’y a pas de thread de rappel Afinity quand vous appelez WinINet de manière asynchrone : un appel peut démarrer à partir d’un thread, mais tout autre thread peut recevoir le rappel.

-   [Avantages](#benefits)
-   [Scénarios](#scenarios)
-   [Rubriques connexes](#related-topics)

## <a name="benefits"></a>Avantages

Il existe plusieurs avantages à fonctionner de manière asynchrone. Par exemple :

-   Téléchargement simultané de plusieurs ressources Internet.

    Vous pouvez vous connecter à plusieurs ressources Internet en même temps et les télécharger dès qu’elles sont disponibles.

-   Amélioration des performances de votre application.

    Une application utilisant les fonctions WinINet de manière asynchrone n’a pas besoin d’attendre que la demande soit terminée. l’application est donc libre d’effectuer d’autres tâches qui ne dépendent pas de la demande, améliorant ainsi les performances globales de l’application.

-   Surveiller la progression du téléchargement.

    La fonction de rappel d’État reçoit des notifications pendant le traitement d’une demande. Si nécessaire, votre application peut utiliser les informations fournies par cette fonction de rappel d’État pour que l’utilisateur soit informé de la progression de l’opération ou d’interruption des requêtes dont l’exécution est trop longue.

## <a name="scenarios"></a>Scénarios

Supposons que votre application doive télécharger des prix de café depuis le café Downfall & thé et les Fourth Coffee sites et comparer les prix. Le site Fourth Coffee a généralement un temps de réponse plus lent. votre application doit donc télécharger les informations de Downfall Coffee & Tea.

Deux versions de l’application sont développées. L’un fonctionne de façon synchrone, en téléchargeant d’abord les prix à partir du site Downfall Coffee & thé, puis les prix à partir du site Fourth Coffee. Le second fonctionne de façon asynchrone, en envoyant des demandes aux deux sites et en téléchargeant les prix lorsqu’ils sont disponibles.

Le tableau suivant illustre ce qui se passerait si le site Fourth Coffee était plus rapide à un jour donné.



| Événement                                                            | Version synchrone                        | Version asynchrone                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Démarrer                                                            | Envoyer une demande à Downfall Coffee & thé      | Envoyer des demandes à Downfall Coffee & thé et Fourth Coffee |
| Demande de la version asynchrone à Fourth Coffee terminée | En attente                                    | Télécharger les tarifs de Fourth Coffee                       |
| Demande de Downfall café & thé terminée                       | Télécharger les prix de Downfall Coffee & thé | Télécharger les prix de Downfall Coffee & thé               |
| Une fois Downfall café & les prix du thé sont téléchargés              | Envoyer une demande à Fourth Coffee              | Comparer les prix                                           |
| Comparaison de la version asynchrone terminée                      | En attente                                    | Opération terminée                                       |
| Demande de la version synchrone à Fourth Coffee terminée  | Télécharger les tarifs de Fourth Coffee         | n/a                                                      |
| Après le téléchargement des prix de Fourth Coffee                      | Comparer les prix                             | n/a                                                      |
| Comparaison de la version synchrone terminée                       | Opération terminée                         | n/a                                                      |



 

Un autre exemple est un navigateur Web tel que Microsoft Internet Explorer. Lorsque le navigateur télécharge une page, il doit souvent Télécharger d’autres ressources, telles que des images et des fichiers audio. En mode asynchrone, la page et les ressources qui lui sont associées peuvent être demandées simultanément et téléchargées dès qu’elles sont disponibles, au lieu de demander et de télécharger la page et chaque ressource une à la fois.

## <a name="related-topics"></a>Rubriques connexes

Vous trouverez ci-dessous des liens connexes.

Tutoriels

-   [Création de fonctions de rappel d’État](creating-status-callback-functions.md)

Fonctions nécessaires à la configuration d’une opération asynchrone

-   [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Fonctions qui peuvent être utilisées de façon asynchrone

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> Les fonctions [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)et [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) utilisent la valeur de contexte fournie dans l’appel à la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .

 

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 