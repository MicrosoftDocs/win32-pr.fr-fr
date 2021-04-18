---
description: Un fournisseur de propriétés récupère et modifie des valeurs de propriété individuelles pour les instances d’une classe donnée qui est stockée dans le référentiel WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519936"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="90401-103">Écriture d’un fournisseur de propriétés</span><span class="sxs-lookup"><span data-stu-id="90401-103">Writing a Property Provider</span></span>

<span data-ttu-id="90401-104">Un fournisseur de propriétés récupère et modifie des valeurs de propriété individuelles pour les instances d’une classe donnée qui est stockée dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="90401-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="90401-105">La procédure suivante décrit comment créer un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="90401-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="90401-106">**Pour créer un fournisseur de propriétés**</span><span class="sxs-lookup"><span data-stu-id="90401-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="90401-107">Concevez et inscrivez votre fournisseur avec WMI.</span><span class="sxs-lookup"><span data-stu-id="90401-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="90401-108">Les fournisseurs d’instances s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="90401-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="90401-109">Pour plus d’informations, consultez [inscription d’un fournisseur de propriétés](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90401-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="90401-110">Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="90401-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="90401-111">WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="90401-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="90401-112">Il s’agit d’une tâche commune à tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="90401-112">This is a task common to all providers.</span></span> <span data-ttu-id="90401-113">Pour plus d’informations, consultez [initialisation d’un fournisseur](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90401-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="90401-114">Les fournisseurs de propriétés sont fortement encouragés à utiliser le modèle de multithreading « both ».</span><span class="sxs-lookup"><span data-stu-id="90401-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="90401-115">Implémentez l’interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="90401-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="90401-116">L’interface [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) est l’interface principale d’un fournisseur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="90401-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="90401-117">Les deux méthodes principales sont [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) et [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span><span class="sxs-lookup"><span data-stu-id="90401-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="90401-118">Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur de propriétés](implementing-the-primary-interface-for-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90401-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="90401-119">Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="90401-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="90401-120">Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="90401-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="90401-121">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [maintenance des niveaux de sécurité dans un fournisseur](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="90401-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="90401-122">Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client.</span><span class="sxs-lookup"><span data-stu-id="90401-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="90401-123">Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="90401-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="90401-124">Remplacez le fournisseur préexistant par votre nouveau code.</span><span class="sxs-lookup"><span data-stu-id="90401-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="90401-125">Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier.</span><span class="sxs-lookup"><span data-stu-id="90401-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="90401-126">Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90401-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



