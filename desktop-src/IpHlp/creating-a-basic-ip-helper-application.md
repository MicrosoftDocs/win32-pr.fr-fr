---
description: Comment créer une application d’assistance IP de base.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Création d’une application d’assistance IP de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009793"
---
# <a name="creating-a-basic-ip-helper-application"></a>Création d’une application d’assistance IP de base

**Pour créer une application d’assistance IP de base**

1.  Créez un projet vide.
2.  Ajoutez un fichier source C++ vide au projet.
3.  Vérifiez que l’environnement de génération fait référence aux répertoires Include, lib et SRC du kit de développement logiciel (SDK) de la plateforme.
4.  Vérifiez que l’environnement de génération est lié au fichier iphlpapi. lib de la bibliothèque d’assistance IP et au fichier de bibliothèque Winsock WS2 \_ 32. lib.
    > [!Note]  
    > Certaines fonctions Winsock de base sont utilisées pour retourner des valeurs d’adresse IP et d’autres informations.

     

5.  Commencez à programmer l’application d’assistance IP. Utilisez l’API d’assistance IP en incluant le fichier d’en-tête d’assistance IP.

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Le fichier d’en-tête *iphlpapi. h* est requis pour les applications qui utilisent les fonctions d’assistance IP. Le fichier d’en-tête *iphlpapi. h* contient automatiquement d’autres fichiers d’en-tête avec des structures et des énumérations utilisées par les fonctions d’assistance IP.
    >
    > les nouvelles fonctions d’assistance IP introduites dans Windows Vista et versions ultérieures sont définies dans le fichier d’en-tête *Netioapi. h* qui est automatiquement inclus dans le fichier d’en-tête *Iphlpapi. h* . Le fichier d’en-tête *Netioapi. h* ne doit jamais être utilisé directement.
    >
    > La plupart des structures et énumérations utilisées par les fonctions d’assistance IP sont définies dans les fichiers d’en-tête *Iprtrmib. h*, *Ipexport. h* et *IPTypes. h* . Ces fichiers d’en-tête sont automatiquement inclus dans le fichier d’en-tête *iphlpapi. h* et ne doivent jamais être utilisés directement.
    >
    > dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’organisation des fichiers d’en-tête a changé. Certaines des structures sont maintenant définies dans les fichiers d’en-tête *Ipmib. h*, *tcpmib. h* et *Udpmib. h* , et non dans le fichier d’en-tête *Iprtrmib. h* . Le fichier d’en-tête *Ipmib. h* comprend automatiquement le fichier d’en-tête *ifmib. h* . Notez que ces fichiers d’en-tête sont automatiquement inclus dans *Iprtrmib. h*, qui est inclus automatiquement dans le fichier d’en-tête *iphlpapi. h* .
    >
    > le fichier d’en-tête *Winsock2. h* pour Windows sockets 2,0 est requis par la plupart des applications utilisant les api d’assistance IP. Lorsque le fichier d’en-tête *Winsock2. h* est requis, la \# ligne include de ce fichier doit être placée avant la \# ligne include pour le fichier d’en-tête *iphlpapi. h* .
    >
    > le fichier d’en-tête *Winsock2. h* inclut en interne les éléments principaux du fichier d’en-tête *Windows. h* . il n’y a donc pas de \# ligne include pour le fichier d’en-tête *Windows. h* dans les applications d’assistance IP. si une \# ligne include est nécessaire pour le fichier d’en-tête *Windows. h* , elle doit être précédée de la \# macro define WIN32 \_ maigre \_ AND \_ MEAN. pour des raisons historiques, l’en-tête *Windows. h* inclut par défaut le fichier d’en-tête *Winsock. h* pour Windows sockets 1,1. les déclarations du fichier d’en-tête *Winsock. h* pour Windows sockets 1,1 sont en conflit avec les déclarations dans le fichier d’en-tête *Winsock2. h* requis par Windows sockets 2,0. la \_ \_ \_ macro moyenne et moyenne WIN32 empêche le fichier d’en-tête *Winsock. h* d’être inclus dans le fichier d’en-tête *Windows. h* . Vous trouverez ci-dessous un exemple illustrant cette illustration.

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > cette application d’assistance ip de base utilise uniquement des structures de données d’adresse ip et des fonctions de conversion d’adresse ip à chaîne de Windows sockets 2,0. ces fonctions de Windows sockets peuvent être utilisées sans l’appel de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) pour initialiser les ressources de sockets Windows et [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) lorsqu’elles sont terminées à l’aide de ces ressources.
    >
    > dans les applications d’assistance ip qui utilisent d’autres fonctions Winsock autres que cette adresse ip pour les fonctions de chaîne, la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) doit être appelée pour initialiser Windows ressources sockets avant d’appeler des fonctions de sockets Windows et [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) doit être appelée lorsque l’application est exécutée à l’aide des ressources de sockets Windows.

     

    > [!Note]
    >
    > Le fichier d’en-tête *stdio. h* est requis pour l’utilisation de diverses fonctions C standard dans cette application d’assistance IP de base.

     

    Étape suivante : [récupération d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 
