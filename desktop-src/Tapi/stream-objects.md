---
description: Les objets de flux sont une abstraction du flux multimédia ou des flux associés à une session d’appel.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objets de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528197"
---
# <a name="stream-objects"></a><span data-ttu-id="1782f-103">Objets de flux</span><span class="sxs-lookup"><span data-stu-id="1782f-103">Stream Objects</span></span>

<span data-ttu-id="1782f-104">Les objets de flux sont une abstraction du flux multimédia ou des flux associés à une session d’appel.</span><span class="sxs-lookup"><span data-stu-id="1782f-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="1782f-105">Les interfaces et les méthodes exposées sur les objets de flux et sous-flux permettent à une application d’exercer des contrôles très détaillés, tels que la suspension d’un flux, l’ajout de nouveaux types de média à une session de communication ou l’ajustement du volume audio d’un participant à une conférence spécifique.</span><span class="sxs-lookup"><span data-stu-id="1782f-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="1782f-106">Les deux principaux types de flux sont le flux et le sous-flux.</span><span class="sxs-lookup"><span data-stu-id="1782f-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="1782f-107">Les interfaces et les méthodes d’une implémentation standard sont similaires pour les deux, mais le sous-flux autorise un niveau de contrôle inférieur.</span><span class="sxs-lookup"><span data-stu-id="1782f-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="1782f-108">Tous les fournisseurs de services multimédias (MSP) doivent implémenter les interfaces de contrôle de flux de base, mais la prise en charge des sous-flux est facultative.</span><span class="sxs-lookup"><span data-stu-id="1782f-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="1782f-109">En outre, certains fournisseurs de services implémentent des [interfaces spécifiques au fournisseur](provider-specific-interfaces.md) pour les flux.</span><span class="sxs-lookup"><span data-stu-id="1782f-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="1782f-110">Par exemple, le MSP IPConf fournit des contrôles de niveau participant.</span><span class="sxs-lookup"><span data-stu-id="1782f-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="1782f-111">Pour obtenir un résumé, consultez la page [interfaces MSP ipconf](ipconf-msp-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="1782f-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="1782f-112">Pour les autres interfaces qui peuvent être implémentées, consultez la documentation du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="1782f-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="1782f-113">Le MSP et l’interface TAPI créent des objets de flux pour un appel lors de la configuration initiale d’une session sortante ou entrante.</span><span class="sxs-lookup"><span data-stu-id="1782f-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="1782f-114">L’application est chargée d’identifier les terminaux appropriés pour ces flux et de sélectionner les terminaux sur les flux.</span><span class="sxs-lookup"><span data-stu-id="1782f-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="1782f-115">Notez que dans certains cas, un MSP peut exiger que l’application arrête ou interrompt les flux avant certaines opérations d’appel de session.</span><span class="sxs-lookup"><span data-stu-id="1782f-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="1782f-116">Les interfaces de flux sont documentées dans la [référence MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1782f-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="1782f-117">L’exemple de code de [sélection de terminal](select-a-terminal.md) montre un exemple d’énumération de flux et de sélection de terminaux.</span><span class="sxs-lookup"><span data-stu-id="1782f-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 



