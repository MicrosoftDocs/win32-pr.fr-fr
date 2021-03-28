---
description: Les comptes d’utilisateur Windows XP permettent à plusieurs utilisateurs de se connecter simultanément, chacun avec ses propres paramètres et chacun exécutant ses propres applications.
ms.assetid: bc404afc-f73e-404d-854d-faab5cf205a5
title: Comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc26471bcf56efce79fb5ccc91a78c24e43ae312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991608"
---
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a>Comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance

Les comptes d’utilisateur Windows XP permettent à plusieurs utilisateurs de se connecter simultanément, chacun avec ses propres paramètres et chacun exécutant ses propres applications. Étant donné qu’un utilisateur n’a pas à se déconnecter pour autoriser l’accès à un autre utilisateur, le Bureau de chaque utilisateur est facilement accessible à l’aide de la fonctionnalité changement rapide d’utilisateur. Les comptes d’utilisateur incluent également la fonctionnalité de Terminal Server personnelle, ou Bureau à distance, qui permet aux utilisateurs d’accéder à leur compte de bureau à partir de systèmes distants.

Les rubriques suivantes sont présentées.

-   [Conditions d’utilisation de l’infrastructure](#infrastructure-usage-requirements)
-   [Compatibilité avec les applications existantes](#compatibility-with-existing-applications)
-   [Inscription pour la notification de changement de session](#registering-for-session-switching-notification)
-   [Vérification qu’une seule instance de votre application est en cours d’exécution](#ensuring-only-one-instance-of-your-application-is-running)
-   [Arrêt de votre application dans toutes les sessions](#shutting-down-your-application-across-all-sessions)
-   [Interaction avec les services système](#interaction-with-system-services)
-   [Bureau à distance et bande passante](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a>Conditions d’utilisation de l’infrastructure

L’infrastructure sous-jacente héritée de Windows 2000 prend en charge la séparation d’état des données utilisateur, des paramètres utilisateur et des paramètres de l’ordinateur. En tirant parti de cette infrastructure, les éléments suivants sont nécessaires pour exécuter correctement votre application sous Windows XP.

-   Par défaut, le dossier **Mes documents** est utilisé pour le stockage des données créées par l’utilisateur.
-   Classifiez et stockez les données d’application correctement.
-   Se dégrader correctement sur les messages « accès refusé ».

Les fichiers temporaires, les fichiers mappés en mémoire et les documents doivent tous être stockés dans le sous-répertoire approprié du répertoire de profil de l’utilisateur. Utilisez [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) ou [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) pour déterminer l’emplacement de stockage approprié pour ces fichiers. Le passage de l’indicateur [**CSIDL \_ AppData**](csidl.md) à ces fonctions retourne le chemin d’accès d’un répertoire du système de fichiers qui sert de référentiel commun pour les données spécifiques à l’application. Utilisez l’indicateur [**CSIDL \_ local \_ AppData**](csidl.md) à la place de **CSIDL \_ AppData** pour les données qui doivent changer lorsque l’utilisateur change, par exemple des fichiers temporaires.

Les exigences répertoriées ci-dessus sont un sous-ensemble de celles du programme de certification Microsoft. Pour plus d’informations, consultez la page du **programme certifié pour Windows** à l’adresse https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx .

## <a name="compatibility-with-existing-applications"></a>Compatibilité avec les applications existantes

Le changement rapide d’utilisateur et le Terminal Server personnel utilisent la technologie des services Terminal Server et sont donc compatibles avec la plupart des applications Microsoft Win32 antérieures. Si une application est compatible avec le logo Windows 2000, implémentant des fonctionnalités de gestion de l’alimentation et de séparation de profil de base, cette application doit s’exécuter correctement sous des comptes d’utilisateur Windows XP individuels.

## <a name="registering-for-session-switching-notification"></a>Inscription pour la notification de changement de session

En règle générale, une application n’a pas besoin d’être averti lorsqu’un basculement de bureau se produit. Toutefois, les applications qui doivent être averties lorsque le compte sous lequel elles s’exécutent sont le Bureau actuel, par exemple les applications qui accèdent au port série ou à d’autres ressources partagées, peuvent s’inscrire pour la notification du commutateur de bureau. Pour vous inscrire à une notification, utilisez la fonction [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) .

Une fois que cette fonction a été appelée, la fenêtre avec handle *HWND* est inscrite pour recevoir un message de [**\_ \_ modification WM WTSSESSION**](../termserv/wm-wtssession-change.md) par le biais de sa fonction **WndProc** . L’ID de session est envoyé dans le paramètre **lParam** , et un code qui indique l’événement qui a généré le message est envoyé dans **wParam** comme l’un des indicateurs suivants.

-   connexion à la \_ console WTS \_
-   déconnexion de la \_ console WTS \_
-   \_connexion à distance WTS \_
-   \_déconnexion à distance WTS \_
-   \_fermeture de session WTS \_
-   connexion à la \_ session WTS \_

Les applications peuvent utiliser ce message pour suivre leur état, ainsi que pour libérer et acquérir des ressources spécifiques à la console. Les postes de travail des utilisateurs peuvent être basculés dynamiquement entre le contrôle à distance et la console. Les applications doivent utiliser le message de [**\_ \_ modification WM WTSSESSION**](../termserv/wm-wtssession-change.md) pour se synchroniser avec l’état de la connexion locale ou distante.

Lorsque votre processus n’a plus besoin de ces notifications ou s’arrête, il doit appeler [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) pour annuler l’inscription de sa notification.

> [!IMPORTANT]
> Les valeurs **HWND** transmises à [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) sont des références décomptées. vous devez donc effectuer un nombre d’appels égal à [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) pour garantir la libération de toutes les ressources allouées.

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a>Vérification qu’une seule instance de votre application est en cours d’exécution

De nombreuses applications doivent s’assurer qu’une seule instance est en cours d’exécution. Il existe plusieurs façons de procéder dans Windows XP. Parmi celles-ci, citons les suivantes :

-   Utilisez [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) ou [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) pour rechercher une fenêtre connue ouverte par votre application. Si cette fenêtre est déjà ouverte, vous pouvez l’utiliser pour indiquer que l’application est déjà en cours d’exécution.
-   Créez un objet mutex ou Semaphore lorsque votre application est ouverte, puis fermez cet objet lorsque l’application se termine. L’espace de noms de l’objet global est séparé pour chaque bureau, ce qui permet d’obtenir une liste unique d’objets mutex et Semaphore pour chacun.

## <a name="shutting-down-your-application-across-all-sessions"></a>Arrêt de votre application dans toutes les sessions

Une application peut être amenée à s’arrêter dans toutes les sessions. Par exemple, une application s’exécutant simultanément dans deux sessions ou plus peut télécharger un nouveau fichier à partir du Web. Ensuite, il peut s’avérer nécessaire de se fermer et de redémarrer avec les bits mis à jour. Cela doit bien sûr être fait dans toutes les sessions en cours d’exécution. Votre application doit être écrite pour s’arrêter correctement lorsqu’une notification est reçue.

## <a name="interaction-with-system-services"></a>Interaction avec les services système

Du point de vue de la programmation, les cas suivants doivent être traités.

-   Le processus serveur reçoit une demande directe d’un processus client.

    Dans ce cas, le message est probablement transmis à l’aide d’un appel de procédure locale (LPC) ou d’un appel de procédure distante (RPC). Il existe des API pour LPC ou RPC qui activent la récupération du jeton client. Une fois le jeton client obtenu, le serveur peut l’utiliser dans un appel à [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera). Cela fait apparaître le processus sur la station de fenêtre appropriée, en supposant que le jeton de l’utilisateur client possède une balise de session, ce qui devrait être le cas.

    > [!Note]  
    > [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ne prend pas en charge l’héritage de la gestion des sessions pour l’instant.

     

-   Le processus serveur reçoit une notification et doit afficher l’interface utilisateur, mais il n’est pas nécessaire que l’affichage se trouve dans le contexte de l’utilisateur actuel.

    Dans ce cas, le processus serveur peut dupliquer son jeton de processus principal et modifier l’identificateur de session en question pour qu’il corresponde à l’identificateur de session actuel. L’identificateur de session actuel peut être obtenu à l’aide de la fonction [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) .

    > [!Note]  
    > Pour définir l’ID de session de jeton, vous avez besoin du **\_ \_ privilège TCB de se**. Vous ne disposez que d’un service s’exécutant dans le système d’autorité NT \\ .

     

## <a name="remote-desktop-and-bandwidth"></a>Bureau à distance et bande passante

Avec l’ajout de la fonctionnalité de Bureau à distance à Windows XP, les applications doivent faire en sorte de ne pas utiliser plus de bande passante qu’il n’en faut, en évitant des dessins d’écran et des effets d’animation importants si le bureau est connecté à distance. Pour déterminer si la session active est distante, vous pouvez appeler [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec le **SM \_ REMOTESESSION**. Sachez toutefois que cet appel ne fait pas de distinction entre distant et déconnecté.

 

 
