---
description: Apprenez à utiliser l’API WSD (Web Services on Devices) de Microsoft pour implémenter des appareils et des services contrôlés par le client, ainsi que des hôtes d’appareil conformes à DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Développement d’applications WSD sur Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405782"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="86b16-103">Développement d’applications WSD sur Windows</span><span class="sxs-lookup"><span data-stu-id="86b16-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="86b16-104">L’API Microsoft Web Services on Devices (WSDAPI) prend en charge l’implémentation d’appareils et de services contrôlés par le client, ainsi que les hôtes d’appareils conformes au [profil des appareils pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="86b16-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="86b16-105">WSDAPI peut être utilisé pour le développement des implémentations du client et du serveur (périphérique).</span><span class="sxs-lookup"><span data-stu-id="86b16-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="86b16-106">Très souvent, le code WSDAPI pour ces applications est généré à l’aide de [WsdCodeGen](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="86b16-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="86b16-107">Certaines fonctions et méthodes WSDAPI sont destinées à être appelées uniquement par le code généré.</span><span class="sxs-lookup"><span data-stu-id="86b16-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="86b16-108">La documentation de référence sur les API indique quand une fonction ou une méthode doit être utilisée ou implémentée uniquement par le code généré.</span><span class="sxs-lookup"><span data-stu-id="86b16-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="86b16-109">Le SDK Windows comprend des exemples de fichiers WSDL, des fichiers de configuration WsdCodeGen et du code généré.</span><span class="sxs-lookup"><span data-stu-id="86b16-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="86b16-110">Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="86b16-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="86b16-111">Si vous souhaitez énumérer les appareils à l’aide du protocole WSD et interroger les métadonnées de l’appareil WSD, vous pouvez utiliser l’API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) à la place.</span><span class="sxs-lookup"><span data-stu-id="86b16-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="86b16-112">Si vous souhaitez implémenter un périphérique WSD qui n’exécute pas Windows, consultez la page [développement de périphérique WSD](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="86b16-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
