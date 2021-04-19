---
description: Un fournisseur de classes gère une classe ou une série de classes pour WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517893"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="0adb6-103">Écriture d’un fournisseur de classe</span><span class="sxs-lookup"><span data-stu-id="0adb6-103">Writing a Class Provider</span></span>

<span data-ttu-id="0adb6-104">Un fournisseur de classes gère une classe ou une série de classes pour WMI.</span><span class="sxs-lookup"><span data-stu-id="0adb6-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="0adb6-105">Un fournisseur de classe peut être push ou pull ; autrement dit, il peut soit stocker ses propres données, soit autoriser WMI à stocker des données pour celui-ci dans le service de gestion Windows.</span><span class="sxs-lookup"><span data-stu-id="0adb6-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="0adb6-106">Bien qu’un fournisseur de classes soit installé sur un ordinateur spécifique, il peut modifier les définitions de classe dans toute l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0adb6-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="0adb6-107">Par conséquent, la plupart des développeurs ne créent pas souvent des fournisseurs de classes.</span><span class="sxs-lookup"><span data-stu-id="0adb6-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="0adb6-108">Avant de construire un fournisseur de classes, vérifiez que les classes prises en charge doivent réellement être générées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="0adb6-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="0adb6-109">Dans la plupart des cas, la liste des classes est à variation lente et finie.</span><span class="sxs-lookup"><span data-stu-id="0adb6-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="0adb6-110">Si c’est le cas, vous ne devez pas être obligé de créer un fournisseur de classe.</span><span class="sxs-lookup"><span data-stu-id="0adb6-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="0adb6-111">Au lieu de cela, vous pouvez placer vos définitions de classe dans le référentiel WMI à l’aide de l’API WMI ou d’un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="0adb6-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="0adb6-112">La procédure suivante décrit comment implémenter un fournisseur de classes.</span><span class="sxs-lookup"><span data-stu-id="0adb6-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="0adb6-113">**Pour implémenter un fournisseur de classes**</span><span class="sxs-lookup"><span data-stu-id="0adb6-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="0adb6-114">Déterminez si votre fournisseur est un fournisseur d’envoi ou d’extraction.</span><span class="sxs-lookup"><span data-stu-id="0adb6-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="0adb6-115">Un fournisseur d’extraction fournit des données de manière dynamique en réponse à une demande de l’application, tandis que les fournisseurs de notifications push stockent leurs données une seule fois dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="0adb6-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="0adb6-116">Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="0adb6-117">Concevez et inscrivez votre fournisseur de classes avec WMI.</span><span class="sxs-lookup"><span data-stu-id="0adb6-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="0adb6-118">Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une instance [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="0adb6-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="0adb6-119">Pour plus d’informations, consultez [inscription d’un fournisseur de classes](registering-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="0adb6-120">Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0adb6-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="0adb6-121">WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0adb6-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="0adb6-122">Si vous concevez un fournisseur push, **IWbemProviderInit** est la seule interface que vous allez implémenter.</span><span class="sxs-lookup"><span data-stu-id="0adb6-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="0adb6-123">Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="0adb6-124">Les fournisseurs de classes sont fortement encouragés à utiliser le modèle de multithreading « both ».</span><span class="sxs-lookup"><span data-stu-id="0adb6-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="0adb6-125">Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0adb6-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="0adb6-126">Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="0adb6-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="0adb6-127">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [maintenance des niveaux de sécurité dans un fournisseur](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="0adb6-128">Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client.</span><span class="sxs-lookup"><span data-stu-id="0adb6-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="0adb6-129">Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="0adb6-130">Implémentez l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0adb6-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="0adb6-131">L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) est l’interface principale d’un fournisseur de classe pull.</span><span class="sxs-lookup"><span data-stu-id="0adb6-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="0adb6-132">Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur de classes](implementing-the-primary-interface-for-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="0adb6-133">Remplacez le fournisseur préexistant par votre nouveau code.</span><span class="sxs-lookup"><span data-stu-id="0adb6-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="0adb6-134">Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier.</span><span class="sxs-lookup"><span data-stu-id="0adb6-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="0adb6-135">Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0adb6-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



