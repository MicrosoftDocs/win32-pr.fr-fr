---
description: L’une des premières tâches à coder pour un fournisseur est le processus d’initialisation, qui couvre toutes les tâches que votre fournisseur doit effectuer, qui lui permet d’envoyer et de recevoir des informations à partir de WMI, de contrôler un objet géré et d’effectuer d’autres tâches.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Initialisation d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868750"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="648c5-103">Initialisation d’un fournisseur</span><span class="sxs-lookup"><span data-stu-id="648c5-103">Initializing a Provider</span></span>

<span data-ttu-id="648c5-104">L’une des premières tâches à coder pour un fournisseur est le processus d’initialisation, qui couvre toutes les tâches que votre fournisseur doit effectuer, qui lui permet d’envoyer et de recevoir des informations à partir de WMI, de contrôler un objet géré et d’effectuer d’autres tâches.</span><span class="sxs-lookup"><span data-stu-id="648c5-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="648c5-105">Chaque type de fournisseur a un ensemble différent de tâches qu’il doit effectuer et un ensemble d’interfaces uniques.</span><span class="sxs-lookup"><span data-stu-id="648c5-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="648c5-106">Toutefois, tous les fournisseurs s’initialisent par le biais de l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et informent WMI de leur état d’initialisation par le biais de l’interface [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .</span><span class="sxs-lookup"><span data-stu-id="648c5-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="648c5-107">La procédure suivante décrit comment initialiser un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="648c5-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="648c5-108">**Pour initialiser un fournisseur**</span><span class="sxs-lookup"><span data-stu-id="648c5-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="648c5-109">Implémentez [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="648c5-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="648c5-110">Lorsque WMI détermine qu’un client requiert les services d’un fournisseur, WMI charge le fournisseur en appelant la méthode [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="648c5-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="648c5-111">Implémentez toutes les interfaces propres à votre type de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="648c5-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="648c5-112">Informez WMI que votre fournisseur a fini d’être initialisé en appelant [**IWbemProviderInitSink :: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="648c5-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="648c5-113">Toutes les implémentations de [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) doivent appeler [**IWbemProviderInitSink :: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) pour signaler l’état d’initialisation à WMI.</span><span class="sxs-lookup"><span data-stu-id="648c5-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="648c5-114">La méthode **SetStatus** permet à WMI de déterminer si un fournisseur est prêt à recevoir des demandes et le type de demandes que le fournisseur est prêt à recevoir.</span><span class="sxs-lookup"><span data-stu-id="648c5-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="648c5-115">La procédure suivante décrit comment signaler une initialisation réussie.</span><span class="sxs-lookup"><span data-stu-id="648c5-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="648c5-116">**Pour signaler une initialisation réussie**</span><span class="sxs-lookup"><span data-stu-id="648c5-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="648c5-117">Définissez le paramètre *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) sur **WBEM \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="648c5-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="648c5-118">En retournant **WBEM \_ S \_ initialisé**, un fournisseur indique une préparation pour gérer les demandes des applications, WMI et d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="648c5-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="648c5-119">Après la réception de WBEM \_ \_ , WMI effectue un appel à la méthode [**IWbemProviderInit :: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) sur le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="648c5-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="648c5-120">Cette requête récupère un pointeur vers l’interface principale du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="648c5-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="648c5-121">La procédure suivante décrit comment signaler une erreur pendant l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="648c5-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="648c5-122">**Pour signaler une erreur pendant l’initialisation**</span><span class="sxs-lookup"><span data-stu-id="648c5-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="648c5-123">**\_ \_ Échec** de la définition du paramètre *IStatus* de [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) à WBEM.</span><span class="sxs-lookup"><span data-stu-id="648c5-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="648c5-124">Les fournisseurs d’affichages WMI qui renvoient **WBEM \_ E \_ échouent** comme non fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="648c5-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="648c5-125">WMI libère le pointeur [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) une fois que WMI a obtenu un pointeur vers l’interface principale du fournisseur ou après l’échec de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="648c5-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="648c5-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="648c5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="648c5-127">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="648c5-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="648c5-128">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="648c5-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="648c5-129">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="648c5-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



