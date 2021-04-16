---
description: À l’aide de l’utilitaire Checkv4.exe pour modifier votre application IPv4 pour prendre en charge IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Utilisation de l’utilitaire Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553944"
---
# <a name="using-the-checkv4exe-utility"></a>Utilisation de l’utilitaire Checkv4.exe

> [!IMPORTANT]
> L’utilitaire *Checkv4.exe* n’est pas fourni avec le kit de développement logiciel (SDK) Windows pour Windows 8, ni dans les versions ultérieures du SDK Windows.

L’utilitaire *Checkv4.exe* est conçu pour vous fournir un partenaire de portage de code. un utilitaire qui parcourt votre base de code avec vous, identifie les problèmes potentiels ou met en évidence le code qui peut tirer parti des structures ou des fonctions compatibles IPv6, et formule des recommandations. Avec l’utilitaire Checkv4.exe, la tâche de modification d’une application IPv4 existante pour prendre en charge IPv6 devient beaucoup plus facile.

L’utilitaire *Checkv4.exe* est installé dans le cadre du kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et les SDK ultérieurs (jusqu’au kit de développement logiciel (SDK) Windows pour Windows 8).

Une version antérieure de l’utilitaire *Checkv4.exe* avec des fonctionnalités plus limitées a également été mise à disposition dans le cadre de la version préliminaire antérieure de la technologie IPv6 de Microsoft pour Windows 2000.

Les sections suivantes décrivent l’utilisation de l’utilitaire *Checkv4.exe* , puis expliquent l’approche recommandée pour la modification d’une application IPv4 existante afin de prendre en charge IPv6.

## <a name="recommendations-for-running-checkv4exe"></a>Recommandations pour l’exécution de Checkv4.exe

-   L’utilitaire *Checkv4.exe* est simple. Exécutez simplement *Checkv4.exe* sur la ligne de commande avec le nom du fichier que vous souhaitez vérifier comme paramètre. *Checkv4.exe* analyse le fichier et fournit des commentaires sur l’emplacement des problèmes de Portage IPv6 dans ce fichier. Le fait de placer le *Checkv4.exe* dans le chemin de votre ordinateur facilite grandement l’exécution de l’utilitaire *Checkv4.exe* à partir de n’importe quel endroit dans votre structure de répertoires de code source. Par exemple, le placement de *Checkv4.exe* dans% windir% vous permet de lancer des *Checkv4.exe* à partir de n’importe quel répertoire sur votre ordinateur sans inclure son chemin d’accès.

-   Exécutez la commande suivante à l’invite de commandes pour analyser le fichier Simplec. c :

    **Checkv4 simplec. c**

    Notez que certaines recommandations formulées par l’utilitaire *Checkv4.exe* requièrent des structures disponibles uniquement dans les versions récentes du fichier d’en-tête *Ws2tcpip. h* , telles que la structure **sockaddr \_ in6** . Ces fichiers d’en-tête sont inclus dans la SDK Windows publiée pour Windows Vista et versions ultérieures. Ces fichiers d’en-tête sont également inclus dans le kit de développement logiciel (SDK) de plateforme précédent publié pour Windows Server 2003. Ces fichiers d’en-tête sont également inclus dans le cadre d’un abonnement MSDN ou par téléchargement.

    La capture d’écran suivante affiche les résultats de l’utilisation de l’utilitaire *Checkv4.exe* sur le fichier Simplec. c inclus dans l’annexe A :

    ![checkv4.exe signale des incompatibilités IPv6 dans le fichier simplec. c](images/portingguide002.jpg)

    La capture d’écran suivante affiche les résultats de l’utilisation de l’utilitaire *Checkv4.exe* sur le fichier simple. c, qui est également inclus dans l’annexe A :

    ![checkv4.exe signale des incompatibilités IPv6 dans le fichier simple. c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>Processus de modification de l’application : où démarrer

Il existe une procédure recommandée associée à l’ajout de la fonctionnalité IPv6 aux applications. Le fait de suivre cette séquence est bénéfique, car il permet aux développeurs de s’assurer que toutes les étapes nécessaires à la modification d’une application IPv4 existante pour prendre en charge IPv6 sont prises. Certaines applications peuvent nécessiter une attention toute particulière à l’une de ces séquences. par exemple, un service système aura probablement moins de problèmes d’interface utilisateur qu’un programme de transfert de fichiers graphique (FTP).

**Pour modifier des applications IPv4 pour prendre en charge IPv6**

1.  Corrigez les structures et les déclarations pour activer la compatibilité IPv6 et IPv4.
2.  Modifiez les appels de fonction pour tirer parti des fonctions compatibles IPv6, telles que les fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .
3.  Examinez le code source pour l’utilisation d’adresses IPv4 codées en dur, telles que l’adresse de bouclage, ou l’utilisation d’autres chaînes littérales.
4.  Effectuer un examen approfondi de l’interface utilisateur, y compris les boîtes de dialogue d’informations. Indiquez s’il est approprié pour les applications compatibles IPv6 de spécifier ou de fournir des informations sur l’adresse IP.
5.  Déterminez si votre application s’appuie sur des protocoles sous-jacents, tels que RPC, et apportez des modifications de programmation appropriées pour gérer les adresses IPv6.
6.  Utilisez l’indicateur de compilation IPV6STRICT lors de la compilation d’applications sur Windows XP et versions ultérieures. Cet indicateur entraîne l’échec de la compilation du code incompatible, comme suit :

    Les applications Windows Sockets 1. x avec du code incompatible ne peuvent pas être compilées et retournent le message d’erreur « WINSOCK2 requis ».

    Les applications Windows Sockets 2. x avec du code incompatible provoquent une erreur au moment de la compilation pour chaque instance du code incompatible. Un message d’erreur est généré au format suivant :

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Par exemple :

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



