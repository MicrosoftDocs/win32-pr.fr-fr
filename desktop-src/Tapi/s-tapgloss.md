---
description: Les termes suivants sont utiles pour comprendre la technologie TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522745"
---
# <a name="s-telephony-api"></a><span data-ttu-id="3bb26-103">S (API de téléphonie)</span><span class="sxs-lookup"><span data-stu-id="3bb26-103">S (Telephony API)</span></span>

<span data-ttu-id="3bb26-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [e](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="3bb26-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="3bb26-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="3bb26-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="3bb26-106">Bibliothèque de liens dynamiques qui prend en charge les communications sur un réseau téléphonique via un ensemble de fonctions de service exportées.</span><span class="sxs-lookup"><span data-stu-id="3bb26-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="3bb26-107">Le fournisseur de services répond aux demandes de téléphonie, qui lui sont envoyées par la bibliothèque de liens dynamiques TAPI, en effectuant les tâches de bas niveau nécessaires pour communiquer sur le réseau téléphonique.</span><span class="sxs-lookup"><span data-stu-id="3bb26-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="3bb26-108">De cette façon, le fournisseur de services, en association avec l’interface TAPI, protège les applications des détails liés aux services et à la technologie de la communication du réseau téléphonique.</span><span class="sxs-lookup"><span data-stu-id="3bb26-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="3bb26-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**sous-adressage**</span><span class="sxs-lookup"><span data-stu-id="3bb26-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="3bb26-110">Fonctionnalité fournie sur les lignes RNIS, qui permet d’obtenir plus d’informations qu’un simple numéro de téléphone à utiliser lors de la numérotation.</span><span class="sxs-lookup"><span data-stu-id="3bb26-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="3bb26-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Téléphonie supplémentaire**</span><span class="sxs-lookup"><span data-stu-id="3bb26-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="3bb26-112">Niveau de service qui fournit des fonctionnalités de commutateur avancées, telles que le maintien, le transfert, etc.</span><span class="sxs-lookup"><span data-stu-id="3bb26-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="3bb26-113">Tous les services supplémentaires sont facultatifs. autrement dit, le fournisseur de services n’est pas tenu de les prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb26-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="3bb26-114">Consultez [*téléphonie assistée*](a-tapgloss.md), [*téléphonie de base*](b-tapgloss.md), [*téléphonie étendue*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span><span class="sxs-lookup"><span data-stu-id="3bb26-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="3bb26-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Commuté 56**</span><span class="sxs-lookup"><span data-stu-id="3bb26-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="3bb26-116">Service de données commuté qui permet à l’utilisateur de composer une autre personne et de transmettre en duplex intégral, Digital Synchronous 56 Kbps pour le prix d’un appel téléphonique.</span><span class="sxs-lookup"><span data-stu-id="3bb26-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="3bb26-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronise**</span><span class="sxs-lookup"><span data-stu-id="3bb26-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="3bb26-118">Méthode de transmission de données dans laquelle il existe un temps constant entre les bits, les caractères ou les événements successifs.</span><span class="sxs-lookup"><span data-stu-id="3bb26-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="3bb26-119">Le minutage est atteint par le partage d’une seule horloge.</span><span class="sxs-lookup"><span data-stu-id="3bb26-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="3bb26-120">Chaque fin de la transmission se synchronise avec l’utilisation des horloges et des informations envoyées avec les données transmises.</span><span class="sxs-lookup"><span data-stu-id="3bb26-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="3bb26-121">Les caractères sont espacés par heure, et non pas par les bits de démarrage et d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="3bb26-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="3bb26-122">Voir [*asynchrone*](a-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="3bb26-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



