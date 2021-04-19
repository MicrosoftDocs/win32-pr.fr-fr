---
description: Avant de pouvoir utiliser un socket pour configurer une connexion ou recevoir une demande de connexion, il faut qu’il soit lié à une adresse locale.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Liaison à une adresse locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516005"
---
# <a name="binding-to-a-local-address"></a><span data-ttu-id="70678-103">Liaison à une adresse locale</span><span class="sxs-lookup"><span data-stu-id="70678-103">Binding to a Local Address</span></span>

<span data-ttu-id="70678-104">Avant de pouvoir utiliser un socket pour configurer une connexion ou recevoir une demande de connexion, il faut qu’il soit lié à une adresse locale.</span><span class="sxs-lookup"><span data-stu-id="70678-104">Before a socket can be used to set up a connection or receive a connection request, it needs to be bound to a local address.</span></span> <span data-ttu-id="70678-105">Cela peut être fait explicitement en appelant [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), ou implicitement par [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) si le socket est indépendant lorsque cette fonction est appelée.</span><span class="sxs-lookup"><span data-stu-id="70678-105">This could be done explicitly by calling [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), or implicitly by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) if the socket is unbound when this function is called.</span></span>

 

 
