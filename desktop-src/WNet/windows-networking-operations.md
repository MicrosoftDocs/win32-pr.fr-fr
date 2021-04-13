---
title: Opérations de réseau Windows
description: Une application peut utiliser les fonctions WNet pour parcourir, ajouter ou annuler des connexions réseau n’importe où dans la hiérarchie du réseau.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315468"
---
# <a name="windows-networking-operations"></a><span data-ttu-id="f7be7-103">Opérations de réseau Windows</span><span class="sxs-lookup"><span data-stu-id="f7be7-103">Windows Networking Operations</span></span>

<span data-ttu-id="f7be7-104">Une application peut utiliser les fonctions WNet pour parcourir, ajouter ou annuler des connexions réseau n’importe où dans la hiérarchie du réseau.</span><span class="sxs-lookup"><span data-stu-id="f7be7-104">An application can use the WNet functions to browse, add, or cancel network connections anywhere in the network hierarchy.</span></span>

<span data-ttu-id="f7be7-105">Une *connexion permanente* est une connexion réseau que le système restaure automatiquement lorsque l’utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="f7be7-105">A *persistent connection* is a network connection that the system automatically restores when the user logs on.</span></span> <span data-ttu-id="f7be7-106">Vous pouvez appeler les fonctions [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (ou [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) et [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) pour contrôler si une connexion réseau est persistante d’une session à la suivante.</span><span class="sxs-lookup"><span data-stu-id="f7be7-106">You can call the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (or [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) and [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) functions to control whether a network connection is persistent from one session to the next.</span></span>

<span data-ttu-id="f7be7-107">Pour rechercher le nom d’utilisateur par défaut ou le nom d’utilisateur utilisé pour établir une connexion réseau, appelez la fonction [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .</span><span class="sxs-lookup"><span data-stu-id="f7be7-107">To find the default user name or the user name used to establish a network connection, call the [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) function.</span></span>

<span data-ttu-id="f7be7-108">En plus d’appeler les fonctions WNet, un processus peut également utiliser des mailslots et des canaux nommés pour communiquer avec un autre processus.</span><span class="sxs-lookup"><span data-stu-id="f7be7-108">In addition to calling the WNet functions, a process can also use mailslots and named pipes to communicate with another process.</span></span> <span data-ttu-id="f7be7-109">Pour plus d’informations, consultez les [mailslots](/windows/desktop/ipc/mailslots) et les [canaux](/windows/desktop/ipc/pipes).</span><span class="sxs-lookup"><span data-stu-id="f7be7-109">For more information, see [Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).</span></span>

 

 