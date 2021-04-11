---
description: Les classes d’appareils simplifient le développement en permettant aux programmeurs de traiter des appareils qui ont des propriétés similaires de la même manière.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Classe d’appareil (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951967"
---
# <a name="device-class"></a><span data-ttu-id="ffece-103">Classe d’appareil</span><span class="sxs-lookup"><span data-stu-id="ffece-103">Device Class</span></span>

<span data-ttu-id="ffece-104">Les classes d’appareils simplifient le développement en permettant aux programmeurs de traiter des appareils qui ont des propriétés similaires de la même manière.</span><span class="sxs-lookup"><span data-stu-id="ffece-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="ffece-105">Par exemple, un téléphone numérique dans un bureau a généralement plus de fonctionnalités qu’un téléphone de base standard, mais les deux répondent pratiquement de la même façon à un ensemble de fonctions de base, et tous deux appartiennent à une classe d’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="ffece-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="ffece-106">Les classes d’appareils permettent d’étendre l’interface TAPI en fournissant une infrastructure à partir de laquelle classifier et prendre en charge de nouveaux équipements.</span><span class="sxs-lookup"><span data-stu-id="ffece-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="ffece-107">Consultez [classes d’appareils TAPI](./tapi-device-classes.md) pour les classes définies par l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="ffece-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="ffece-108">Un fournisseur de services peut implémenter et définir des classes d’appareils supplémentaires pour l’équipement qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="ffece-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="ffece-109">Une application n’a jamais besoin de savoir quel est le fournisseur de services qui contrôle l’appareil, mais peut nécessiter des informations sur le contrôle des nouvelles classes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="ffece-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="ffece-110">Un fournisseur de services implémente une classe d’appareil en mappant les demandes dans les commandes d’appareil réelles.</span><span class="sxs-lookup"><span data-stu-id="ffece-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="ffece-111">Par exemple, lorsque le fournisseur de services pour un modem compatible Hayes reçoit une commande transmise via TAPISVR pour effectuer un appel, il envoie des commandes AT classiques au modem.</span><span class="sxs-lookup"><span data-stu-id="ffece-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="ffece-112">L’interface du fournisseur de services peut être mappée à un large éventail d’environnements, y compris ceux qui ne sont généralement pas considérés comme appartenant à la téléphonie.</span><span class="sxs-lookup"><span data-stu-id="ffece-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="ffece-113">Par exemple, la Conférence multimédia sur un réseau basé sur IP comme Internet.</span><span class="sxs-lookup"><span data-stu-id="ffece-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="ffece-114">Les développeurs d’applications doivent garder à l’esprit l’existence d’autres applications susceptibles de partager des services de téléphonie.</span><span class="sxs-lookup"><span data-stu-id="ffece-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 
