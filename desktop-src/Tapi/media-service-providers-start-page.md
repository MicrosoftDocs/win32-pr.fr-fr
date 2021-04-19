---
description: Un fournisseur de services de média (MSP) permet à une application de contrôler le média pour un mécanisme de transport particulier.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Fournisseurs de services de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525793"
---
# <a name="media-service-providers"></a><span data-ttu-id="b0e4b-103">Fournisseurs de services de média</span><span class="sxs-lookup"><span data-stu-id="b0e4b-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="b0e4b-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="b0e4b-104">Purpose</span></span>

<span data-ttu-id="b0e4b-105">Un fournisseur de services de média (MSP) permet à une application de contrôler le média pour un mécanisme de transport particulier.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="b0e4b-106">Un MSP est toujours associé à un fournisseur de services de téléphonie (TSP).</span><span class="sxs-lookup"><span data-stu-id="b0e4b-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="b0e4b-107">L’interface MSPI (Media Service Provider Interface) est un ensemble d’interfaces et de méthodes implémentées par un MSP pour permettre à une application de contrôler le transport multimédia au cours d’une session de communication.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="b0e4b-108">Un MSP gère les mécanismes spécifiques à l’appareil et spécifiques au protocole requis pour mettre en œuvre ces contrôles, et communique avec son PVC couplé ou une application à l’aide des méthodes fournies dans le MSPI.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b0e4b-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="b0e4b-109">Developer audience</span></span>

<span data-ttu-id="b0e4b-110">Vous devez vous familiariser avec COM.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-110">Familiarity with COM is required.</span></span> <span data-ttu-id="b0e4b-111">L’expérience de développement avec les télécommunications ou d’autres applications de téléphonie est utile, mais pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b0e4b-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="b0e4b-112">Run-time requirements</span></span>

<span data-ttu-id="b0e4b-113">MSPI permet le développement de fournisseurs de services multimédias pour des protocoles ou des appareils spécifiques s’exécutant sur des systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0e4b-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b0e4b-114">In this section</span></span>



| <span data-ttu-id="b0e4b-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b0e4b-115">Topic</span></span>                                                                       | <span data-ttu-id="b0e4b-116">Description</span><span class="sxs-lookup"><span data-stu-id="b0e4b-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b0e4b-117">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="b0e4b-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="b0e4b-118">Informations générales sur l’architecture et les composants MSP.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="b0e4b-119">Référence</span><span class="sxs-lookup"><span data-stu-id="b0e4b-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="b0e4b-120">Documentation pour les interfaces MSPI.</span><span class="sxs-lookup"><span data-stu-id="b0e4b-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="b0e4b-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0e4b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e4b-122">Vue d’ensemble de la téléphonie Microsoft</span><span class="sxs-lookup"><span data-stu-id="b0e4b-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="b0e4b-123">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b0e4b-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="b0e4b-124">Fournisseurs de services de téléphonie</span><span class="sxs-lookup"><span data-stu-id="b0e4b-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

