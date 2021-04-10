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
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="0be24-103">Création d’une application Winsock de base</span><span class="sxs-lookup"><span data-stu-id="0be24-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="0be24-104">**Pour créer une application Winsock de base**</span><span class="sxs-lookup"><span data-stu-id="0be24-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="0be24-105">Créez un projet vide.</span><span class="sxs-lookup"><span data-stu-id="0be24-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="0be24-106">Ajoutez un fichier source C++ vide au projet.</span><span class="sxs-lookup"><span data-stu-id="0be24-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="0be24-107">Veillez à ce que l’environnement de génération fasse référence aux répertoires Include, lib et SRC du kit de développement logiciel (SDK) Microsoft Windows ou du kit de développement logiciel (SDK) de plateforme précédent.</span><span class="sxs-lookup"><span data-stu-id="0be24-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="0be24-108">Vérifiez que l’environnement de génération est lié au fichier de bibliothèque Winsock Ws2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="0be24-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="0be24-109">Les applications qui utilisent Winsock doivent être liées au \_ fichier de bibliothèque Ws2 32. lib.</span><span class="sxs-lookup"><span data-stu-id="0be24-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="0be24-110">Le \# Commentaire pragma indique à l’éditeur de liens que le fichier *Ws2 \_ 32. lib* est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0be24-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="0be24-111">Commencez à programmer l’application Winsock.</span><span class="sxs-lookup"><span data-stu-id="0be24-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="0be24-112">Utilisez l’API Winsock en incluant les fichiers d’en-tête Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="0be24-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="0be24-113">Le fichier d’en-tête *Winsock2. h* contient la plupart des fonctions, structures et définitions Winsock.</span><span class="sxs-lookup"><span data-stu-id="0be24-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="0be24-114">Le fichier d’en-tête *Ws2tcpip. h* contient les définitions présentées dans le document de l’annexe WinSock 2 Protocol-Specific pour TCP/IP, qui inclut des fonctions et structures plus récentes utilisées pour récupérer des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="0be24-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="0be24-115">Stdio. h est utilisé pour l’entrée et la sortie standard, en particulier la fonction **printf ()** .</span><span class="sxs-lookup"><span data-stu-id="0be24-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


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
> <span data-ttu-id="0be24-116">Le fichier d’en-tête *iphlpapi. h* est requis si une application utilise les API d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="0be24-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="0be24-117">Lorsque le fichier d’en-tête *iphlpapi. h* est requis, la \# ligne include pour le fichier d’en-tête *Winsock2. h* doit être placée avant la \# ligne include pour le fichier d’en-tête *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="0be24-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="0be24-118">Le fichier d’en-tête *Winsock2. h* inclut en interne les éléments principaux du fichier d’en-tête *Windows. h* . il n’y a donc pas \# de ligne include pour le fichier d’en-tête *Windows. h* dans les applications Winsock.</span><span class="sxs-lookup"><span data-stu-id="0be24-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="0be24-119">Si une \# ligne include est nécessaire pour le fichier d’en-tête *Windows. h* , elle doit être précédée de la \# macro define Win32 \_ maigre \_ and \_ Mean.</span><span class="sxs-lookup"><span data-stu-id="0be24-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="0be24-120">Pour des raisons historiques, l’en-tête *Windows. h* inclut par défaut le fichier d’en-tête *Winsock. h* pour Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="0be24-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="0be24-121">Les déclarations du fichier d’en-tête *Winsock. h* sont en conflit avec les déclarations dans le fichier d’en-tête *Winsock2. h* requis par Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="0be24-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="0be24-122">La \_ \_ \_ macro moyenne et moyenne Win32 empêche l’inclusion de *Winsock. h* par l’en-tête *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="0be24-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="0be24-123">Vous trouverez ci-dessous un exemple illustrant cette illustration.</span><span class="sxs-lookup"><span data-stu-id="0be24-123">An example illustrating this is shown below.</span></span>

 


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



<span data-ttu-id="0be24-124">Étape suivante : [initialisation de Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="0be24-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0be24-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0be24-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0be24-126">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="0be24-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="0be24-127">À propos des serveurs et des clients</span><span class="sxs-lookup"><span data-stu-id="0be24-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



