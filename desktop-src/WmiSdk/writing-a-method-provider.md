---
description: Un fournisseur de méthode autorise l’accès WMI aux méthodes d’une classe. Par exemple, une classe qui représente une application peut avoir une méthode qui termine l’application.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Écriture d’un fournisseur de méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530853"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="09302-104">Écriture d’un fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="09302-104">Writing a Method Provider</span></span>

<span data-ttu-id="09302-105">Un fournisseur de méthode autorise l’accès WMI aux méthodes d’une classe.</span><span class="sxs-lookup"><span data-stu-id="09302-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="09302-106">Par exemple, une classe qui représente une application peut avoir une méthode qui termine l’application.</span><span class="sxs-lookup"><span data-stu-id="09302-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="09302-107">La modification de l’ordre des paramètres d’entrée et de sortie de la méthode lors de la mise à jour d’un fournisseur de méthodes existant peut provoquer un échec pour les applications qui appellent la méthode.</span><span class="sxs-lookup"><span data-stu-id="09302-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="09302-108">L’ordre des paramètres d’entrée ou de sortie est établi par la valeur du qualificateur d' [**ID**](standard-wmi-qualifiers.md) sur chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="09302-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="09302-109">Le premier paramètre a une valeur d' **ID** égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="09302-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="09302-110">Ajoutez de nouveaux paramètres d’entrée à la fin des paramètres existants au lieu de les insérer dans la séquence déjà établie.</span><span class="sxs-lookup"><span data-stu-id="09302-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="09302-111">La procédure suivante décrit comment implémenter un fournisseur de méthodes.</span><span class="sxs-lookup"><span data-stu-id="09302-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="09302-112">**Pour implémenter un fournisseur de méthode**</span><span class="sxs-lookup"><span data-stu-id="09302-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="09302-113">Concevez et inscrivez votre fournisseur de classes avec WMI.</span><span class="sxs-lookup"><span data-stu-id="09302-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="09302-114">Les fournisseurs de classes s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="09302-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="09302-115">Pour plus d’informations, consultez [inscription d’un fournisseur de méthodes](registering-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="09302-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="09302-116">Implémentez l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="09302-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="09302-117">Les fournisseurs de méthode sont fortement encouragés à utiliser le modèle de multithreading « both ».</span><span class="sxs-lookup"><span data-stu-id="09302-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="09302-118">Implémentez la méthode [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="09302-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="09302-119">L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) est l’interface principale d’un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="09302-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="09302-120">Pour plus d’informations, consultez [implémentation de l’interface principale pour un fournisseur de méthodes](implementing-the-primary-interface-for-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="09302-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="09302-121">Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="09302-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="09302-122">Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI.</span><span class="sxs-lookup"><span data-stu-id="09302-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="09302-123">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [maintenance des niveaux de sécurité dans un fournisseur](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="09302-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="09302-124">Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client.</span><span class="sxs-lookup"><span data-stu-id="09302-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="09302-125">Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="09302-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="09302-126">Remplacez le fournisseur préexistant par votre nouveau code.</span><span class="sxs-lookup"><span data-stu-id="09302-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="09302-127">Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier.</span><span class="sxs-lookup"><span data-stu-id="09302-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="09302-128">Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="09302-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



