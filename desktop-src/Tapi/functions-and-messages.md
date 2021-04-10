---
description: La fonction phoneDevSpecific et son \_ message DEVSPECIFIC téléphone associé permettent à une application d’accéder à des fonctionnalités de téléphone spécifiques à l’appareil qui ne sont pas disponibles via les services de téléphonie courants pour les téléphones.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Fonctions et messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951963"
---
# <a name="functions-and-messages"></a><span data-ttu-id="0003c-103">Fonctions et messages</span><span class="sxs-lookup"><span data-stu-id="0003c-103">Functions and Messages</span></span>

<span data-ttu-id="0003c-104">La fonction [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) et son message [**\_ DEVSPECIFIC téléphone**](phone-devspecific.md) associé permettent à une application d’accéder à des fonctionnalités de téléphone spécifiques à l’appareil qui ne sont pas disponibles via les services de téléphonie courants pour les téléphones.</span><span class="sxs-lookup"><span data-stu-id="0003c-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="0003c-105">En d’autres termes, **phoneDevSpecific** est la fonction d’échappement propre au périphérique qui autorise les extensions dépendantes du fournisseur, et Phone \_ DEVSPECIFIC est le message spécifique à l’appareil qui est envoyé à l’application.</span><span class="sxs-lookup"><span data-stu-id="0003c-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="0003c-106">Le profil de paramètre de la fonction [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) est générique dans cette légère interprétation des paramètres effectuée par l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="0003c-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="0003c-107">Au lieu de cela, l’interprétation des paramètres est définie par le fournisseur de services et doit être comprise par une application qui les utilise.</span><span class="sxs-lookup"><span data-stu-id="0003c-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="0003c-108">Les paramètres sont simplement transmis par l’interface TAPI de l’application au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="0003c-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="0003c-109">Une application qui s’appuie sur des extensions spécifiques à l’appareil ne fonctionne généralement pas avec d’autres fournisseurs de services, mais les applications écrites dans les services téléphoniques courants fonctionnent avec le fournisseur de services étendu.</span><span class="sxs-lookup"><span data-stu-id="0003c-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



