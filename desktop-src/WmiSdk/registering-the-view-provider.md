---
description: WMI inscrit automatiquement la DLL du fournisseur d’affichage lors du processus d’installation de WMI. Toutefois, vous devez encore inscrire le fournisseur d’affichage auprès de WMI pour chaque espace de noms qui contiendra des classes d’affichage.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Inscription du fournisseur de vues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531748"
---
# <a name="registering-the-view-provider"></a><span data-ttu-id="d575c-104">Inscription du fournisseur de vues</span><span class="sxs-lookup"><span data-stu-id="d575c-104">Registering the View Provider</span></span>

<span data-ttu-id="d575c-105">WMI inscrit automatiquement la DLL du fournisseur d’affichage lors du processus d’installation de WMI.</span><span class="sxs-lookup"><span data-stu-id="d575c-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="d575c-106">Toutefois, vous devez encore inscrire le fournisseur d’affichage auprès de WMI pour chaque espace de noms qui contiendra des classes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d575c-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="d575c-107">La procédure suivante décrit comment inscrire le fournisseur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d575c-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="d575c-108">**Pour inscrire le fournisseur d’affichage**</span><span class="sxs-lookup"><span data-stu-id="d575c-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="d575c-109">Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) pour décrire l’implémentation du fournisseur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d575c-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="d575c-110">L’instance [**\_ \_ Win32Provider**](--win32provider.md) décrit le nom du fournisseur et son identificateur de classe (CLSID), ainsi que les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="d575c-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="d575c-111">L’exemple de code suivant décrit une implémentation de [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="d575c-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="d575c-112">Créez une instance de la classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="d575c-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="d575c-113">L’exemple de code suivant montre comment créer une instance de la classe **\_ \_ InstanceProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="d575c-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  <span data-ttu-id="d575c-114">Créez une instance de la classe [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) si vous souhaitez que votre classe d’affichage Union prenne en charge des méthodes.</span><span class="sxs-lookup"><span data-stu-id="d575c-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="d575c-115">L’exemple de code suivant montre comment créer une instance de la classe **\_ \_ MethodProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="d575c-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="d575c-116">Compilez votre code MOF à l’aide du compilateur MOF ([mofcomp](mofcomp.md)) ou de l’interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="d575c-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="d575c-117">Si vous enregistrez l’exemple de code MOF précédemment listé dans un fichier nommé Viewtest. mof, utilisez la commande mofcomp pour charger le code MOF dans l’espace de noms cible.</span><span class="sxs-lookup"><span data-stu-id="d575c-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="d575c-118">*NamespacePath* est l’espace de noms dans lequel vous souhaitez créer l’instance de la classe d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d575c-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="d575c-119">Tapez la commande suivante à l’invite de commandes pour charger le code MOF dans l’espace de noms cible.</span><span class="sxs-lookup"><span data-stu-id="d575c-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="d575c-120">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="d575c-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="d575c-121">Pour plus d’informations, consultez [inscription d’un fournisseur](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d575c-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



