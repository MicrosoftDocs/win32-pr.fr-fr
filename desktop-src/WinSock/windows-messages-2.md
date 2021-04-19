---
description: Windows Sockets 1,1 a introduit le mécanisme Async-SELECT pour fournir des indications d’événements réseau qui n’impliquaient pas l’interrogation ou le blocage.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Messages Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524938"
---
# <a name="windows-messages"></a><span data-ttu-id="9bfc8-103">Messages Windows</span><span class="sxs-lookup"><span data-stu-id="9bfc8-103">Windows Messages</span></span>

<span data-ttu-id="9bfc8-104">Windows Sockets 1,1 a introduit le mécanisme Async-SELECT pour fournir des indications d’événements réseau qui n’impliquaient pas l’interrogation ou le blocage.</span><span class="sxs-lookup"><span data-stu-id="9bfc8-104">Windows Sockets 1.1 introduced the async-select mechanism to provide network event indications that did not involve either polling or blocking.</span></span> <span data-ttu-id="9bfc8-105">La fonction [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) est utilisée pour enregistrer un intérêt dans un ou plusieurs événements réseau, comme indiqué dans le précédent, et fournir un handle de fenêtre à utiliser pour la notification.</span><span class="sxs-lookup"><span data-stu-id="9bfc8-105">The [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) function is used to register an interest in one or more network events as listed in the preceding, and supply a window handle to be used for notification.</span></span> <span data-ttu-id="9bfc8-106">Lorsqu’un événement réseau désigné se produit, un message Windows spécifié par le client est envoyé à la fenêtre indiquée.</span><span class="sxs-lookup"><span data-stu-id="9bfc8-106">When a nominated network event occurs, a client-specified Windows message is sent to the indicated window.</span></span> <span data-ttu-id="9bfc8-107">Pour ce faire, le fournisseur de services doit utiliser la fonction [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) .</span><span class="sxs-lookup"><span data-stu-id="9bfc8-107">The service provider must use the [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) function to accomplish this.</span></span>

<span data-ttu-id="9bfc8-108">Dans Windows, cela peut ne pas être le mécanisme de notification le plus efficace et il est peu commode pour les démons et les services qui ne souhaitent pas ouvrir de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="9bfc8-108">In Windows, this may not be the most efficient notification mechanism, and is inconvenient for daemons and services that do not want to open any windows.</span></span> <span data-ttu-id="9bfc8-109">Le mécanisme de signalisation de l’objet d’événement décrit dans les éléments suivants est introduit pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="9bfc8-109">The event object signaling mechanism described in the following is introduced to solve this problem.</span></span>

 

 
