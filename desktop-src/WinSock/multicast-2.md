---
description: Les fonctions Winsock multipoint génériques prennent en charge la multidiffusion IP.
ms.assetid: 32fffca8-4f13-495b-afb6-bb57a9cce553
title: Multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c6b4ece06119d01e2661028f452985bb20b068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113043"
---
# <a name="multicast"></a><span data-ttu-id="b7031-103">Multidiffusion</span><span class="sxs-lookup"><span data-stu-id="b7031-103">Multicast</span></span>

<span data-ttu-id="b7031-104">Les fonctions Winsock multipoint génériques prennent en charge la multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="b7031-104">Generic Winsock multipoint functions support IP multicast.</span></span> <span data-ttu-id="b7031-105">Toutefois, les fournisseurs de transport TCP/IP qui prennent en charge la multidiffusion doivent également fournir une prise en charge de la multidiffusion du style BSD (Berkeley Software Distribution), en prenant en charge les options de multidiffusion correspondantes.</span><span class="sxs-lookup"><span data-stu-id="b7031-105">However, the TCP/IP transport providers that support multicast must also provide Berkeley Software Distribution (BSD) style–multicast support by supporting the corresponding multicast options.</span></span> <span data-ttu-id="b7031-106">Cela simplifie le portage d’applications de multidiffusion existantes vers Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="b7031-106">This simplifies the porting of existing multicast applications to Windows Sockets 2.</span></span>

 

 



