---
description: Utilisation du \_ \_ Code de commande d’étendue de multidiffusion SIO pour spécifier l’étendue sur laquelle la multidiffusion doit se produire.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543731"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="d8c7b-103">IOCTL de l' \_ étendue de multidiffusion SIO \_</span><span class="sxs-lookup"><span data-stu-id="d8c7b-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="d8c7b-104">Lorsque la multidiffusion est utilisée, il est généralement nécessaire de spécifier l’étendue sur laquelle la multidiffusion doit se produire.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="d8c7b-105">Ici, l’étendue est définie comme étant le nombre de segments réseau routés à couvrir.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="d8c7b-106">Le \_ \_ Code de commande d’étendue de multidiffusion SIO pour [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) est utilisé pour contrôler cela.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="d8c7b-107">Une étendue égale à zéro indique que la transmission par multidiffusion n’est pas placée sur le câble, mais peut être diffusée sur les sockets au sein de l’hôte local.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="d8c7b-108">Une valeur d’étendue de 1 (valeur par défaut) indique que la transmission sera placée sur le câble, mais ne franchira pas de routeurs.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="d8c7b-109">Des valeurs de portée supérieures déterminent le nombre de routeurs qui peuvent être franchis.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="d8c7b-110">Notez que cela correspond au paramètre de durée de vie (TTL) dans la multidiffusion IP.</span><span class="sxs-lookup"><span data-stu-id="d8c7b-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
