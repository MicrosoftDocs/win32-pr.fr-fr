---
description: Comment créer une application Windows Sockets (Winsock) de base.
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Création d’une application Winsock de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113091"
---
# <a name="creating-a-basic-winsock-application"></a>Création d’une application Winsock de base

**Pour créer une application Winsock de base**

1.  Créez un projet vide.
2.  Ajoutez un fichier source C++ vide au projet.
3.  Veillez à ce que l’environnement de génération fasse référence aux répertoires Include, lib et SRC du kit de développement logiciel (SDK) Microsoft Windows ou du kit de développement logiciel (SDK) de plateforme précédent.
4.  Vérifiez que l’environnement de génération est lié au fichier de bibliothèque Winsock Ws2 \_ 32. lib. Les applications qui utilisent Winsock doivent être liées au \_ fichier de bibliothèque Ws2 32. lib. Le \# Commentaire pragma indique à l’éditeur de liens que le fichier *Ws2 \_ 32. lib* est nécessaire.
5.  Commencez à programmer l’application Winsock. Utilisez l’API Winsock en incluant les fichiers d’en-tête Winsock 2. Le fichier d’en-tête *Winsock2. h* contient la plupart des fonctions, structures et définitions Winsock. Le fichier d’en-tête *Ws2tcpip. h* contient les définitions présentées dans le document de l’annexe WinSock 2 Protocol-Specific pour TCP/IP, qui inclut des fonctions et structures plus récentes utilisées pour récupérer des adresses IP.
    > [!Note]  
    > Stdio. h est utilisé pour l’entrée et la sortie standard, en particulier la fonction **printf ()** .

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> Le fichier d’en-tête *iphlpapi. h* est requis si une application utilise les API d’assistance IP. Lorsque le fichier d’en-tête *iphlpapi. h* est requis, la \# ligne include pour le fichier d’en-tête *Winsock2. h* doit être placée avant la \# ligne include pour le fichier d’en-tête *iphlpapi. h* .
>
> Le fichier d’en-tête *Winsock2. h* inclut en interne les éléments principaux du fichier d’en-tête *Windows. h* . il n’y a donc pas \# de ligne include pour le fichier d’en-tête *Windows. h* dans les applications Winsock. Si une \# ligne include est nécessaire pour le fichier d’en-tête *Windows. h* , elle doit être précédée de la \# macro define Win32 \_ maigre \_ and \_ Mean. Pour des raisons historiques, l’en-tête *Windows. h* inclut par défaut le fichier d’en-tête *Winsock. h* pour Windows Sockets 1,1. Les déclarations du fichier d’en-tête *Winsock. h* sont en conflit avec les déclarations dans le fichier d’en-tête *Winsock2. h* requis par Windows Sockets 2,0. La \_ \_ \_ macro moyenne et moyenne Win32 empêche l’inclusion de *Winsock. h* par l’en-tête *Windows. h* . Vous trouverez ci-dessous un exemple illustrant cette illustration.

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



Étape suivante : [initialisation de Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec Winsock](getting-started-with-winsock.md)
</dt> <dt>

[À propos des serveurs et des clients](about-clients-and-servers.md)
</dt> </dl>

 

 



