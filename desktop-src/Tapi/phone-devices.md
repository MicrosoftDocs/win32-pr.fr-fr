---
description: La prise en charge des appareils téléphoniques est plus simple que de base, donc les fournisseurs de services ne sont pas tenus de prendre en charge les appareils téléphoniques.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Appareils téléphoniques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951350"
---
# <a name="phone-devices"></a><span data-ttu-id="f4d55-103">Appareils téléphoniques</span><span class="sxs-lookup"><span data-stu-id="f4d55-103">Phone Devices</span></span>

<span data-ttu-id="f4d55-104">La prise en charge des appareils téléphoniques est plus simple que de base, donc les fournisseurs de services ne sont pas tenus de prendre en charge les appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="f4d55-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="f4d55-105">Tout comme une classe de périphérique en ligne est une abstraction d’un périphérique de ligne physique, la classe de périphérique téléphonique représente une abstraction indépendante du périphérique d’un ensemble de téléphones.</span><span class="sxs-lookup"><span data-stu-id="f4d55-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="f4d55-106">L’interface TAPI traite les appareils téléphoniques et de ligne comme des appareils indépendants les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="f4d55-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="f4d55-107">En d’autres termes, vous pouvez utiliser un téléphone (appareil) sans utiliser de ligne associée, et vous pouvez utiliser une ligne (appareil) sans utiliser de téléphone.</span><span class="sxs-lookup"><span data-stu-id="f4d55-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="f4d55-108">Les fournisseurs de services qui implémentent pleinement cette indépendance peuvent offrir des utilisations pour ces appareils qui ne sont pas définis par les protocoles de téléphonie traditionnels.</span><span class="sxs-lookup"><span data-stu-id="f4d55-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="f4d55-109">Par exemple, une personne peut utiliser le combiné du téléphone du bureau comme un périphérique audio Wave pour l’enregistrement ou la lecture vocal, peut-être sans que le commutateur soit en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f4d55-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="f4d55-110">Dans une telle implémentation, le levage du téléphone local n’a pas besoin d’envoyer automatiquement un signal offhook au commutateur.</span><span class="sxs-lookup"><span data-stu-id="f4d55-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="f4d55-111">Cette indépendance permet également à une application d’appeler le téléphone local d’une manière indépendante des appels entrants.</span><span class="sxs-lookup"><span data-stu-id="f4d55-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="f4d55-112">Les fonctionnalités des fournisseurs de services sont limitées par les fonctionnalités du matériel et des logiciels utilisés pour interconnecter le commutateur, le téléphone et l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f4d55-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="f4d55-113">L’interface TAPI comprend des fonctions permettant de récupérer des fonctionnalités d’appareil qui permettent aux clients de déterminer si un tel modèle d’utilisation est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f4d55-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="f4d55-114">Cette section décrit les appareils téléphoniques et explique comment utiliser les fonctions de téléphonie TAPI pour accéder à ces appareils.</span><span class="sxs-lookup"><span data-stu-id="f4d55-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="f4d55-115">Appareil téléphonique</span><span class="sxs-lookup"><span data-stu-id="f4d55-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="f4d55-116">Initialisation et arrêt</span><span class="sxs-lookup"><span data-stu-id="f4d55-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 



