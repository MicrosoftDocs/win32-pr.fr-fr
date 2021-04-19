---
description: Un fournisseur de consommateur d’événements est un composant de l’architecture de consommateur permanente qui détermine quel consommateur d’événements permanent gère un événement donné.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de consommateur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522058"
---
# <a name="writing-an-event-consumer-provider"></a><span data-ttu-id="ee8cd-103">Écriture d’un fournisseur de consommateur d’événements</span><span class="sxs-lookup"><span data-stu-id="ee8cd-103">Writing an Event Consumer Provider</span></span>

<span data-ttu-id="ee8cd-104">Un fournisseur de consommateur d’événements est un composant de l’architecture de consommateur permanente qui détermine quel consommateur d’événements permanent gère un événement donné.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-104">An event consumer provider is a component of the permanent consumer architecture that determines which permanent event consumer handles a given event.</span></span> <span data-ttu-id="ee8cd-105">Vous devez créer un fournisseur de consommateur d’événements et vos consommateurs d’événements permanents pour router correctement les événements à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-105">You should create an event consumer provider along with your permanent event consumers to route events properly from WMI.</span></span>

<span data-ttu-id="ee8cd-106">Un fournisseur de consommateur d’événements lie un fournisseur d’événements à une liste de classes de consommateur.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-106">An event consumer provider links an event provider with a list of consumer classes.</span></span> <span data-ttu-id="ee8cd-107">Les instances de ces classes de consommateur reçoivent alors des événements de ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-107">Instances of these consumer classes then receive events from that provider.</span></span> <span data-ttu-id="ee8cd-108">WMI identifie le fournisseur de consommateurs auquel les événements sont remis, en fonction de l’instance [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , qui associe l’instance [**\_ \_ Win32Provider**](--win32provider.md) du fournisseur de consommateurs à une classe de consommateur logique.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-108">WMI identifies which consumer provider the events are delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a logical consumer class.</span></span> <span data-ttu-id="ee8cd-109">Les utilisateurs créent des instances de la classe de consommateur dans le cadre d’un abonnement permanent.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-109">Users create instances of the consumer class as part of a permanent subscription.</span></span> <span data-ttu-id="ee8cd-110">Si le fournisseur d’événements n’est pas en cours d’exécution lorsqu’un événement se produit, WMI démarre le fournisseur lorsqu’il doit remettre des événements.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-110">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span>

<span data-ttu-id="ee8cd-111">La procédure suivante décrit comment implémenter un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-111">The following procedure describes how to implement an event consumer provider.</span></span>

<span data-ttu-id="ee8cd-112">**Pour implémenter un fournisseur de consommateur d’événements**</span><span class="sxs-lookup"><span data-stu-id="ee8cd-112">**To implement an event consumer provider**</span></span>

1.  <span data-ttu-id="ee8cd-113">Concevez des classes de consommateur en format MOF (MOF) et inscrivez-les avec WMI.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-113">Design consumer classes in Managed Object Format (MOF) and register them with WMI.</span></span> <span data-ttu-id="ee8cd-114">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ee8cd-114">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

    <span data-ttu-id="ee8cd-115">Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="ee8cd-115">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class.</span></span> <span data-ttu-id="ee8cd-116">Pour plus d’informations, consultez [inscription d’un fournisseur de consommateur d’événements](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee8cd-116">For more information, see [Registering an Event Consumer Provider](registering-an-event-consumer-provider.md).</span></span>

2.  <span data-ttu-id="ee8cd-117">Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-117">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="ee8cd-118">WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-118">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="ee8cd-119">Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ee8cd-119">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="ee8cd-120">Les fournisseurs de consommateur d’événements sont fortement encouragés à utiliser le modèle de multithreading « both ».</span><span class="sxs-lookup"><span data-stu-id="ee8cd-120">Event consumer providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="ee8cd-121">Implémentez l’interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-121">Implement the [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface for your provider.</span></span>

    <span data-ttu-id="ee8cd-122">L’interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) est l’interface principale d’un fournisseur de consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-122">The [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) interface is the primary interface for an event consumer provider.</span></span>

4.  <span data-ttu-id="ee8cd-123">Fournissez un ou plusieurs consommateurs physiques pour recevoir les messages d’événement de WMI.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-123">Supply one or more physical consumers to receive the event messages from WMI.</span></span>

    <span data-ttu-id="ee8cd-124">Un consommateur physique est un objet COM qui représente un consommateur d’événements permanent.</span><span class="sxs-lookup"><span data-stu-id="ee8cd-124">A physical consumer is a COM object that represents a permanent event consumer.</span></span> <span data-ttu-id="ee8cd-125">Tous les consommateurs physiques doivent implémenter l’interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="ee8cd-125">All physical consumers must implement the [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) interface.</span></span> <span data-ttu-id="ee8cd-126">Pour plus d’informations, consultez [implémentation d’un consommateur physique](implementing-a-physical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="ee8cd-126">For more information, see [Implementing a Physical Consumer](implementing-a-physical-consumer.md).</span></span>

 

 



