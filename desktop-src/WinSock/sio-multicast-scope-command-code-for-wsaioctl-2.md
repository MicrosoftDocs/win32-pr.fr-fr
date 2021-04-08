---
description: Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l’étendue sur laquelle la multidiffusion doit se produire.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE le code de commande pour WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034261"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a><span data-ttu-id="30f0b-103">\_ \_ Code de commande de l’étendue de multidiffusion SIO pour WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="30f0b-103">SIO\_MULTICAST\_SCOPE Command Code for WSAIoctl</span></span>

<span data-ttu-id="30f0b-104">Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l' *étendue* sur laquelle la multidiffusion doit se produire.</span><span class="sxs-lookup"><span data-stu-id="30f0b-104">When multicasting is employed, it is usually necessary to specify the *scope* over which the multicast should occur.</span></span> <span data-ttu-id="30f0b-105">L’étendue est définie comme le nombre de segments de réseau routé à couvrir.</span><span class="sxs-lookup"><span data-stu-id="30f0b-105">Scope is defined as the number of routed network segments to be covered.</span></span> <span data-ttu-id="30f0b-106">Une étendue égale à zéro indique que la transmission par multidiffusion n’est pas placée sur le câble, mais peut être diffusée sur les sockets au sein de l’hôte local.</span><span class="sxs-lookup"><span data-stu-id="30f0b-106">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="30f0b-107">Une valeur d’étendue de 1 (valeur par défaut) indique que la transmission sera placée sur le câble, mais ne franchira pas de routeurs.</span><span class="sxs-lookup"><span data-stu-id="30f0b-107">A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="30f0b-108">Des valeurs de portée supérieures déterminent le nombre de routeurs qui peuvent être franchis.</span><span class="sxs-lookup"><span data-stu-id="30f0b-108">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="30f0b-109">Notez que cela correspond au paramètre de durée de vie (TTL) dans la multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="30f0b-109">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

<span data-ttu-id="30f0b-110">La fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) est utilisée pour joindre un nœud terminal dans la session multipoint.</span><span class="sxs-lookup"><span data-stu-id="30f0b-110">The function [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) is used to join a leaf node into the multipoint session.</span></span> <span data-ttu-id="30f0b-111">Pour plus d’informations sur l’utilisation de cette fonction, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="30f0b-111">See the following for a discussion on how this function is utilized.</span></span>

 

 



