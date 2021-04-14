---
description: Comment créer une application d’assistance IP de base.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Création d’une application d’assistance IP de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321082"
---
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="54298-103">Création d’une application d’assistance IP de base</span><span class="sxs-lookup"><span data-stu-id="54298-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="54298-104">**Pour créer une application d’assistance IP de base**</span><span class="sxs-lookup"><span data-stu-id="54298-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="54298-105">Créez un projet vide.</span><span class="sxs-lookup"><span data-stu-id="54298-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="54298-106">Ajoutez un fichier source C++ vide au projet.</span><span class="sxs-lookup"><span data-stu-id="54298-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="54298-107">Vérifiez que l’environnement de génération fait référence aux répertoires Include, lib et SRC du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="54298-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="54298-108">Vérifiez que l’environnement de génération est lié au fichier iphlpapi. lib de la bibliothèque d’assistance IP et au fichier de bibliothèque Winsock WS2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="54298-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="54298-109">Certaines fonctions Winsock de base sont utilisées pour retourner des valeurs d’adresse IP et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="54298-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="54298-110">Commencez à programmer l’application d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="54298-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="54298-111">Utilisez l’API d’assistance IP en incluant le fichier d’en-tête d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="54298-111">Use the IP Helper API by including the IP Helper header file.</span></span>

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
    > <span data-ttu-id="54298-112">Le fichier d’en-tête *iphlpapi. h* est requis pour les applications qui utilisent les fonctions d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="54298-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="54298-113">Le fichier d’en-tête *iphlpapi. h* contient automatiquement d’autres fichiers d’en-tête avec des structures et des énumérations utilisées par les fonctions d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="54298-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="54298-114">Les nouvelles fonctions d’assistance IP introduites dans Windows Vista et les versions ultérieures sont définies dans le fichier d’en-tête *Netioapi. h* qui est automatiquement inclus dans le fichier d’en-tête *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="54298-115">Le fichier d’en-tête *Netioapi. h* ne doit jamais être utilisé directement.</span><span class="sxs-lookup"><span data-stu-id="54298-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="54298-116">La plupart des structures et énumérations utilisées par les fonctions d’assistance IP sont définies dans les fichiers d’en-tête *Iprtrmib. h*, *Ipexport. h* et *IPTypes. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="54298-117">Ces fichiers d’en-tête sont automatiquement inclus dans le fichier d’en-tête *iphlpapi. h* et ne doivent jamais être utilisés directement.</span><span class="sxs-lookup"><span data-stu-id="54298-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="54298-118">Dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’Organisation des fichiers d’en-tête a changé.</span><span class="sxs-lookup"><span data-stu-id="54298-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="54298-119">Certaines des structures sont maintenant définies dans les fichiers d’en-tête *Ipmib. h*, *tcpmib. h* et *Udpmib. h* , et non dans le fichier d’en-tête *Iprtrmib. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="54298-120">Le fichier d’en-tête *Ipmib. h* comprend automatiquement le fichier d’en-tête *ifmib. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="54298-121">Notez que ces fichiers d’en-tête sont automatiquement inclus dans *Iprtrmib. h*, qui est inclus automatiquement dans le fichier d’en-tête *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="54298-122">Le fichier d’en-tête *Winsock2. h* pour Windows sockets 2,0 est requis par la plupart des applications utilisant les API d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="54298-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="54298-123">Lorsque le fichier d’en-tête *Winsock2. h* est requis, la \# ligne include de ce fichier doit être placée avant la \# ligne include pour le fichier d’en-tête *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="54298-124">Le fichier d’en-tête *Winsock2. h* inclut en interne les éléments principaux du fichier d’en-tête *Windows. h* . il n’y a donc pas \# de ligne include pour le fichier d’en-tête *Windows. h* dans les applications d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="54298-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="54298-125">Si une \# ligne include est nécessaire pour le fichier d’en-tête *Windows. h* , elle doit être précédée de la \# macro define Win32 \_ maigre \_ and \_ Mean.</span><span class="sxs-lookup"><span data-stu-id="54298-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="54298-126">Pour des raisons historiques, l’en-tête *Windows. h* inclut par défaut le fichier d’en-tête *Winsock. h* pour Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="54298-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="54298-127">Les déclarations du fichier d’en-tête *Winsock. h* pour Windows sockets 1,1 seront en conflit avec les déclarations dans le fichier d’en-tête *Winsock2. h* requis par Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="54298-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="54298-128">La \_ \_ \_ macro moyenne et moyenne Win32 empêche le fichier d’en-tête *Winsock. h* d’être inclus dans le fichier d’en-tête *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="54298-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="54298-129">Vous trouverez ci-dessous un exemple illustrant cette illustration.</span><span class="sxs-lookup"><span data-stu-id="54298-129">An example illustrating this is shown below.</span></span>

     

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
    > <span data-ttu-id="54298-130">Cette application d’assistance IP de base utilise uniquement des structures de données d’adresse IP et des fonctions de conversion d’adresse IP à chaîne à partir de Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="54298-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="54298-131">Ces fonctions Windows Sockets peuvent être utilisées sans appeler [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) pour initialiser les ressources Windows Sockets et [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) lorsqu’elles sont terminées à l’aide de ces ressources.</span><span class="sxs-lookup"><span data-stu-id="54298-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="54298-132">Dans les applications d’assistance IP qui utilisent d’autres fonctions Winsock autres que cette adresse IP pour les fonctions de chaîne, la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) doit être appelée pour initialiser les ressources Windows Sockets avant d’appeler des fonctions Windows Sockets et [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) doit être appelé lorsque l’application est exécutée à l’aide des ressources Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="54298-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="54298-133">Le fichier d’en-tête *stdio. h* est requis pour l’utilisation de diverses fonctions C standard dans cette application d’assistance IP de base.</span><span class="sxs-lookup"><span data-stu-id="54298-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="54298-134">Étape suivante : [récupération d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="54298-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
