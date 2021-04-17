---
description: Tous les processus (applications ou dll) qui appellent des fonctions Winsock doivent initialiser l’utilisation de la DLL Windows Sockets avant d’effectuer d’autres appels de fonctions Winsock. Cela permet également de s’assurer que Winsock est pris en charge sur le système.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Initialisation de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526158"
---
# <a name="initializing-winsock"></a><span data-ttu-id="81cd1-104">Initialisation de Winsock</span><span class="sxs-lookup"><span data-stu-id="81cd1-104">Initializing Winsock</span></span>

<span data-ttu-id="81cd1-105">Tous les processus (applications ou dll) qui appellent des fonctions Winsock doivent initialiser l’utilisation de la DLL Windows Sockets avant d’effectuer d’autres appels de fonctions Winsock.</span><span class="sxs-lookup"><span data-stu-id="81cd1-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="81cd1-106">Cela permet également de s’assurer que Winsock est pris en charge sur le système.</span><span class="sxs-lookup"><span data-stu-id="81cd1-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="81cd1-107">**Pour initialiser Winsock**</span><span class="sxs-lookup"><span data-stu-id="81cd1-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="81cd1-108">Créez un objet [**wsadata,**](/windows/desktop/api/winsock/ns-winsock-wsadata) appelé wsadata,.</span><span class="sxs-lookup"><span data-stu-id="81cd1-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="81cd1-109">Appelez [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) et retournez sa valeur sous la forme d’un entier et recherchez les erreurs.</span><span class="sxs-lookup"><span data-stu-id="81cd1-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="81cd1-110">La fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) est appelée pour initier l’utilisation de WS2 \_32.dll.</span><span class="sxs-lookup"><span data-stu-id="81cd1-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="81cd1-111">La structure [**wsadata,**](/windows/desktop/api/winsock/ns-winsock-wsadata) contient des informations sur l’implémentation de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="81cd1-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="81cd1-112">Le paramètre MAKEWORD (2, 2) de [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) envoie une demande pour la version 2,2 de Winsock sur le système et définit la version passée comme la version la plus récente de prise en charge de Windows Sockets que l’appelant peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="81cd1-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="81cd1-113">Étape suivante pour un client : [création d’un socket pour le client](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="81cd1-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="81cd1-114">Étape suivante pour un serveur : [création d’un socket pour le serveur](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="81cd1-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="81cd1-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81cd1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81cd1-116">Prise en main avec Winsock</span><span class="sxs-lookup"><span data-stu-id="81cd1-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="81cd1-117">Création d’une application Winsock de base</span><span class="sxs-lookup"><span data-stu-id="81cd1-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



