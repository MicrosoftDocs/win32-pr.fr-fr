---
description: La mise en réseau ATM (Asynchronous Transfer Mode) est émergente dans le monde de l’informatique, et la prise en charge de la technologie ATM a été ajoutée à de nombreuses parties du système d’exploitation.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Qualité de service (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867369"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="911f6-103">Qualité de service (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="911f6-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="911f6-104">La mise en réseau ATM (Asynchronous Transfer Mode) est émergente dans le monde de l’informatique, et la prise en charge de la technologie ATM a été ajoutée à de nombreuses parties du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="911f6-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="911f6-105">L’interface TAPI prend également en charge des attributs clés pour établir des appels sur des installations ATM.</span><span class="sxs-lookup"><span data-stu-id="911f6-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="911f6-106">Les plus importantes du point de vue d’une application sont la possibilité de demander, de négocier, de renégocier et de recevoir des indications de paramètres de qualité de service (QOS) sur les appels entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="911f6-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="911f6-107">Les informations de QOS dans TAPI sont échangées entre les applications et les fournisseurs de services dans les structures [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) définies dans Windows sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="911f6-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="911f6-108">Les applications demandent la qualité de service (QOS) aux appels sortants en définissant les valeurs d’informations de session avant de démarrer une session de communication.</span><span class="sxs-lookup"><span data-stu-id="911f6-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="911f6-109">Le fournisseur de services essaiera de fournir la qualité de service spécifiée et de faire échouer l’appel si ce n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="911f6-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="911f6-110">L’application peut ensuite ajuster ses paramètres et retenter l’appel.</span><span class="sxs-lookup"><span data-stu-id="911f6-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="911f6-111">Une fois qu’un appel est établi, une application peut demander une modification de la qualité de service (QOS).</span><span class="sxs-lookup"><span data-stu-id="911f6-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="911f6-112">L’interface TAPI fournit des notifications d’événements pour le propriétaire ou le contrôle des applications en cas de modification des niveaux de QOS.</span><span class="sxs-lookup"><span data-stu-id="911f6-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="911f6-113">La prise en charge de QOS n’est pas limitée aux transports ATM ; n’importe quel fournisseur de services peut implémenter des fonctionnalités QOS.</span><span class="sxs-lookup"><span data-stu-id="911f6-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="911f6-114">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="911f6-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="911f6-115">\* \* TAPI 2. x : \* \*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** et **dwReceivingFlowspecOffset** membres de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span><span class="sxs-lookup"><span data-stu-id="911f6-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="911f6-116">\* \* TAPI 3. x : \* \*[**ITBasicCallControl :: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="911f6-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
