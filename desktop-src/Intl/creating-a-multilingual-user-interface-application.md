---
description: Ce didacticiel montre comment prendre une application monolingue et la rendre prête pour le monde. Cette application se présente sous la forme d’une solution complète générée dans Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Ajout de la prise en charge de l’interface utilisateur multilingue à une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867945"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="37e52-104">Ajout de la prise en charge de l’interface utilisateur multilingue à une application</span><span class="sxs-lookup"><span data-stu-id="37e52-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="37e52-105">Ce didacticiel montre comment prendre une application monolingue et la rendre prête pour le monde.</span><span class="sxs-lookup"><span data-stu-id="37e52-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="37e52-106">Cette application se présente sous la forme d’une solution complète générée dans Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37e52-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="37e52-107">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="37e52-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="37e52-108">L’idée derrière le MUI Hello</span><span class="sxs-lookup"><span data-stu-id="37e52-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="37e52-109">Configuration de la solution Hello MUI</span><span class="sxs-lookup"><span data-stu-id="37e52-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="37e52-110">Configuration requise pour la plateforme</span><span class="sxs-lookup"><span data-stu-id="37e52-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="37e52-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="37e52-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="37e52-112">Étape 0 : création de l’interface MUI Hello codée en dur</span><span class="sxs-lookup"><span data-stu-id="37e52-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="37e52-113">Étape 1 : implémentation du module de ressources de base</span><span class="sxs-lookup"><span data-stu-id="37e52-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="37e52-114">Étape 2 : génération du module de ressources de base</span><span class="sxs-lookup"><span data-stu-id="37e52-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="37e52-115">Fractionnement des différents modules de ressources linguistiques : vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="37e52-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="37e52-116">Fractionnement des différents modules de ressources linguistiques : création des fichiers</span><span class="sxs-lookup"><span data-stu-id="37e52-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="37e52-117">Étape 3 : création d’un Resource-Savvy « Hello MUI »</span><span class="sxs-lookup"><span data-stu-id="37e52-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="37e52-118">Étape 4 : globalisation de « Hello MUI »</span><span class="sxs-lookup"><span data-stu-id="37e52-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="37e52-119">Étape 5 : personnalisation de « Hello MUI »</span><span class="sxs-lookup"><span data-stu-id="37e52-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="37e52-120">Considérations supplémentaires pour MUI</span><span class="sxs-lookup"><span data-stu-id="37e52-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="37e52-121">Prise en charge des applications console</span><span class="sxs-lookup"><span data-stu-id="37e52-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="37e52-122">Détermination des langues à prendre en charge au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="37e52-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="37e52-123">Prise en charge des scripts complexes dans les versions antérieures à Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37e52-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="37e52-124">Résumé</span><span class="sxs-lookup"><span data-stu-id="37e52-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="37e52-125">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="37e52-125">Overview</span></span>

<span data-ttu-id="37e52-126">À partir de Windows Vista, le système d’exploitation Windows lui-même a été créé dès le départ pour être une plateforme multilingue, avec une prise en charge supplémentaire qui vous permet de créer des applications multilingues qui utilisent le modèle de ressource MUI Windows.</span><span class="sxs-lookup"><span data-stu-id="37e52-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="37e52-127">Ce didacticiel illustre cette nouvelle prise en charge des applications multilingues en couvrant les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="37e52-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="37e52-128">Utilise la prise en charge améliorée de la plateforme MUI pour activer facilement les applications multilingues.</span><span class="sxs-lookup"><span data-stu-id="37e52-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="37e52-129">Étend les applications multilingues pour qu’elles s’exécutent sur des versions de Windows antérieures à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37e52-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="37e52-130">Aborde les considérations supplémentaires impliquées dans le développement d’applications multilingues spécialisées, telles que les applications de console.</span><span class="sxs-lookup"><span data-stu-id="37e52-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="37e52-131">Ces liens permettent d’actualiser rapidement les concepts relatifs à l’internationalisation et à l’interface MUI :</span><span class="sxs-lookup"><span data-stu-id="37e52-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="37e52-132">[Aperçu rapide de l’internationalisation](understanding-internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="37e52-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="37e52-133">[Concepts MUI](understanding-mui.md).</span><span class="sxs-lookup"><span data-stu-id="37e52-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="37e52-134">[Utilisation de l’interface MUI pour développer des applications Win32](using-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="37e52-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="37e52-135">L’idée derrière le MUI Hello</span><span class="sxs-lookup"><span data-stu-id="37e52-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="37e52-136">Vous êtes probablement familiarisé avec l’application Hello World classique, qui illustre les concepts de programmation de base.</span><span class="sxs-lookup"><span data-stu-id="37e52-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="37e52-137">Ce didacticiel adopte une approche similaire pour illustrer l’utilisation du modèle de ressources MUI pour mettre à jour une application monolingue afin de créer une version multilingue appelée Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="37e52-138">Les tâches de ce didacticiel sont décrites dans les étapes détaillées en raison de la précision avec laquelle ces activités doivent être exécutées et de la nécessité d’expliquer les détails aux développeurs qui ont peu d’expérience avec ces tâches.</span><span class="sxs-lookup"><span data-stu-id="37e52-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="37e52-139">Configuration de la solution Hello MUI</span><span class="sxs-lookup"><span data-stu-id="37e52-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="37e52-140">Ces étapes décrivent comment préparer la création de la solution de l’interface MUI Hello.</span><span class="sxs-lookup"><span data-stu-id="37e52-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="37e52-141">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="37e52-141">Platform Requirements</span></span>

<span data-ttu-id="37e52-142">Vous devez compiler les exemples de code de ce didacticiel à l’aide du kit de développement logiciel (SDK) Windows pour Windows 7 et Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="37e52-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="37e52-143">Le kit de développement logiciel (SDK) Windows 7 s’installe sur Windows XP, Windows Vista et Windows 7, et l’exemple de solution peut être basé sur n’importe laquelle de ces versions de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="37e52-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="37e52-144">Tous les exemples de code de ce didacticiel sont conçus pour être exécutés sur des versions x86 et x64 de Windows XP, Windows Vista et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37e52-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="37e52-145">Les composants spécifiques qui ne fonctionnent pas sous Windows XP sont dénommés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="37e52-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="37e52-146">Prérequis</span><span class="sxs-lookup"><span data-stu-id="37e52-146">Prerequisites</span></span>

1.  <span data-ttu-id="37e52-147">Installez Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="37e52-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="37e52-148">Pour plus d’informations, consultez le [Centre de développement Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="37e52-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="37e52-149">Installez le SDK Windows pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37e52-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="37e52-150">Vous pouvez l’installer à partir de la page SDK Windows du [Centre de développement Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="37e52-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="37e52-151">Le kit de développement logiciel (SDK) comprend des utilitaires permettant de développer des applications pour les versions de système d’exploitation à partir de Windows XP via le plus récent.</span><span class="sxs-lookup"><span data-stu-id="37e52-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="37e52-152">Si vous n’installez pas le package à l’emplacement par défaut, ou si vous n’effectuez pas l’installation sur le lecteur système, qui est généralement le lecteur C, notez le chemin d’installation.</span><span class="sxs-lookup"><span data-stu-id="37e52-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="37e52-153">Configurez les paramètres de ligne de commande de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37e52-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="37e52-154">Ouvrez une fenêtre de commande Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37e52-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="37e52-155">Tapez **set path**.</span><span class="sxs-lookup"><span data-stu-id="37e52-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="37e52-156">Vérifiez que la variable PATH contient le chemin d’accès du dossier bin du kit de développement logiciel (SDK) Windows 7 :... \\ \\ Emplacement Windows v 7.0 des kits de développement logiciel Microsoft \\</span><span class="sxs-lookup"><span data-stu-id="37e52-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="37e52-157">Installez le package du module complémentaire API de niveau inférieur de Microsoft NLS.</span><span class="sxs-lookup"><span data-stu-id="37e52-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="37e52-158">Dans le cadre de ce didacticiel, ce package est nécessaire uniquement si vous souhaitez personnaliser l’application pour qu’elle s’exécute sur des versions de Windows antérieures à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37e52-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="37e52-159">Consultez [étape 5 : personnalisation de Hello MUI](#step-5-customizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="37e52-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="37e52-160">Téléchargez et installez le package à partir de son [site de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="37e52-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="37e52-161">Comme pour la SDK Windows, si vous n’installez pas le package à l’emplacement par défaut, ou si vous n’installez pas sur le lecteur système, qui est généralement le lecteur C, notez le chemin d’installation.</span><span class="sxs-lookup"><span data-stu-id="37e52-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="37e52-162">Si votre plateforme de développement est Windows XP ou Windows Server 2003, vérifiez que Nlsdl.dll est installé et inscrit correctement.</span><span class="sxs-lookup"><span data-stu-id="37e52-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="37e52-163">Accédez au dossier « Redist » sous l’emplacement du chemin d’installation.</span><span class="sxs-lookup"><span data-stu-id="37e52-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="37e52-164">Exécutez le nlsdl redistribuable approprié. \* . exe, par exemple nlsdl.x86.exe.</span><span class="sxs-lookup"><span data-stu-id="37e52-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="37e52-165">Cette étape installe et inscrit Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="37e52-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="37e52-166">Si vous développez une application qui utilise MUI et qui doit s’exécuter sur des versions de Windows antérieures à Windows Vista, Nlsdl.dll doit être présent sur la plateforme Windows de destination.</span><span class="sxs-lookup"><span data-stu-id="37e52-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="37e52-167">Dans la plupart des cas, cela signifie que l’application doit transporter et installer le programme d’installation redistribuable nlsdl (et pas simplement copier Nlsdl.dll lui-même).</span><span class="sxs-lookup"><span data-stu-id="37e52-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="37e52-168">Étape 0 : création de l’interface MUI Hello codée en dur</span><span class="sxs-lookup"><span data-stu-id="37e52-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="37e52-169">Ce didacticiel commence par la version monolingue de l’application Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="37e52-170">L’application suppose l’utilisation du langage de programmation C++, des chaînes de caractères larges et de la fonction [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="37e52-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="37e52-171">Commencez par créer l’application GuiStep \_ 0 initiale, ainsi que la solution HelloMUI, qui contient toutes les applications de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="37e52-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="37e52-172">Dans Visual Studio 2008, créez un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="37e52-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="37e52-173">Utilisez les paramètres et valeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="37e52-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="37e52-174">Type de projet : sous Visual C++ sélectionnez Win32, puis sous modèles Visual Studio installés, sélectionnez projet Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="37e52-175">Nom : GuiStep \_ 0.</span><span class="sxs-lookup"><span data-stu-id="37e52-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="37e52-176">Emplacement : *ProjectRootDirectory* (les étapes ultérieures font référence à ce répertoire).</span><span class="sxs-lookup"><span data-stu-id="37e52-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="37e52-177">Nom de la solution : HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="37e52-178">Sélectionnez Créer le répertoire pour la solution.</span><span class="sxs-lookup"><span data-stu-id="37e52-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="37e52-179">Dans l’Assistant application Win32, sélectionnez le type d’application par défaut : application Windows.</span><span class="sxs-lookup"><span data-stu-id="37e52-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="37e52-180">Configurez le modèle de thread de projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="37e52-181">Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 0, puis sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="37e52-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="37e52-182">Dans la boîte de dialogue pages de propriétés du projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="37e52-183">Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.</span><span class="sxs-lookup"><span data-stu-id="37e52-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="37e52-184">Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="37e52-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="37e52-185">Remplacez le contenu de GuiStep \_ 0. cpp par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="37e52-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  <span data-ttu-id="37e52-186">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="37e52-186">Build and run the application.</span></span>

<span data-ttu-id="37e52-187">Le code source simple ci-dessus rend le choix de conception simpliste qui consiste à coder en dur, ou incorporer, toute la sortie que l’utilisateur verra, dans ce cas le texte « Hello MUI ».</span><span class="sxs-lookup"><span data-stu-id="37e52-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="37e52-188">Ce choix limite l’utilitaire de l’application pour les utilisateurs qui ne reconnaissent pas le mot anglais « Hello ».</span><span class="sxs-lookup"><span data-stu-id="37e52-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="37e52-189">Étant donné que MUI est un acronyme anglais basé sur la technologie, il est supposé pour ce didacticiel que la chaîne reste « MUI » pour toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="37e52-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="37e52-190">Étape 1 : implémentation du module de ressources de base</span><span class="sxs-lookup"><span data-stu-id="37e52-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="37e52-191">Microsoft Win32 a longtemps exposé la possibilité pour les développeurs d’applications de séparer leurs données de ressources d’interface utilisateur du code source de l’application.</span><span class="sxs-lookup"><span data-stu-id="37e52-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="37e52-192">Cette séparation est fournie sous la forme du modèle de ressource Win32, dans lequel les chaînes, les bitmaps, les icônes, les messages et les autres éléments normalement affichés pour un utilisateur sont empaquetés dans une section distincte de l’exécutable, séparés du code exécutable.</span><span class="sxs-lookup"><span data-stu-id="37e52-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="37e52-193">Pour illustrer cette séparation entre le code exécutable et l’empaquetage des données de ressources, dans cette étape, le didacticiel place la chaîne « Hello » précédemment codée en dur (la ressource « en-US ») dans la section des ressources d’un module DLL du projet HelloModule en \_ \_ US.</span><span class="sxs-lookup"><span data-stu-id="37e52-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="37e52-194">Cette DLL Win32 peut également contenir des fonctionnalités exécutables de type bibliothèque (comme n’importe quelle autre DLL).</span><span class="sxs-lookup"><span data-stu-id="37e52-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="37e52-195">Mais pour vous aider à vous concentrer sur les aspects relatifs aux ressources Win32, nous laissons le code de la DLL runtime extrait dans DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="37e52-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="37e52-196">Les sections suivantes de ce didacticiel utilisent les données de ressource HelloModule créées ici et présentent également le code d’exécution approprié.</span><span class="sxs-lookup"><span data-stu-id="37e52-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="37e52-197">Pour construire un module de ressources Win32, commencez par créer une DLL avec une fonction DllMain extraite :</span><span class="sxs-lookup"><span data-stu-id="37e52-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="37e52-198">Ajoutez un nouveau projet à la solution HelloMUI :</span><span class="sxs-lookup"><span data-stu-id="37e52-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="37e52-199">Dans le menu fichier, sélectionnez Ajouter, puis nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="37e52-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="37e52-200">Type de projet : projet Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="37e52-201">Nom : HelloModule \_ en \_ US.</span><span class="sxs-lookup"><span data-stu-id="37e52-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="37e52-202">Emplacement : *ProjectRootDirectory* \\ HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="37e52-203">Dans l’Assistant application Win32, sélectionnez type d’application : DLL.</span><span class="sxs-lookup"><span data-stu-id="37e52-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="37e52-204">Configurez le modèle de thread de ce projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="37e52-205">Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet HelloModule en \_ \_ -US et sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="37e52-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="37e52-206">Dans la boîte de dialogue pages de propriétés du projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="37e52-207">Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.</span><span class="sxs-lookup"><span data-stu-id="37e52-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="37e52-208">Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="37e52-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="37e52-209">Examinez DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="37e52-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="37e52-210">(Vous pouvez ajouter le non référencé \_ Les macros de paramètre au code généré, comme nous l’avons vu ici, pour permettre la compilation au niveau d’avertissement 4.)</span><span class="sxs-lookup"><span data-stu-id="37e52-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  <span data-ttu-id="37e52-211">Ajoutez un fichier de définition de ressource HelloModule. RC au projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="37e52-212">Sous le projet HelloModule \_ \_ en US, cliquez avec le bouton droit sur le dossier fichiers de ressources, sélectionnez Ajouter, puis nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="37e52-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="37e52-213">Dans la boîte de dialogue Ajouter un nouvel élément, choisissez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="37e52-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="37e52-214">Catégories : sous Visual C++ sélectionnez ressource, puis sous « modèles Visual Studio installés », sélectionnez fichier de ressources (. RC).</span><span class="sxs-lookup"><span data-stu-id="37e52-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="37e52-215">Nom : HelloModule.</span><span class="sxs-lookup"><span data-stu-id="37e52-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="37e52-216">Emplacement : acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="37e52-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="37e52-217">Cliquez sur Ajouter.</span><span class="sxs-lookup"><span data-stu-id="37e52-217">Click Add.</span></span>

    3.  <span data-ttu-id="37e52-218">Spécifiez que le nouveau fichier HelloModule. RC sera enregistré au format Unicode :</span><span class="sxs-lookup"><span data-stu-id="37e52-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="37e52-219">Dans le Explorateur de solutions, cliquez avec le bouton droit sur HelloModule. RC, puis sélectionnez Afficher le code.</span><span class="sxs-lookup"><span data-stu-id="37e52-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="37e52-220">Si vous voyez un message indiquant que le fichier est déjà ouvert, et vous demande si vous voulez le fermer, cliquez sur Oui.</span><span class="sxs-lookup"><span data-stu-id="37e52-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="37e52-221">Avec le fichier affiché sous forme de texte, définissez le fichier de sélection de menu, puis les options d’enregistrement avancées.</span><span class="sxs-lookup"><span data-stu-id="37e52-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="37e52-222">Sous encodage, spécifiez Unicode-CodePage 1200.</span><span class="sxs-lookup"><span data-stu-id="37e52-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="37e52-223">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="37e52-223">Click OK.</span></span>
        6.  <span data-ttu-id="37e52-224">Enregistrez et fermez HelloModule. rc.</span><span class="sxs-lookup"><span data-stu-id="37e52-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="37e52-225">Ajoutez une table de chaînes contenant la chaîne « Hello » :</span><span class="sxs-lookup"><span data-stu-id="37e52-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="37e52-226">Dans le Affichage des ressources, cliquez avec le bouton droit sur HelloModule. RC, puis sélectionnez Ajouter une ressource.</span><span class="sxs-lookup"><span data-stu-id="37e52-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="37e52-227">Sélectionnez table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="37e52-227">Select String Table.</span></span>
        3.  <span data-ttu-id="37e52-228">Cliquez sur Nouveau.</span><span class="sxs-lookup"><span data-stu-id="37e52-228">Click New.</span></span>
        4.  <span data-ttu-id="37e52-229">Ajoutez une chaîne à la table de chaînes :</span><span class="sxs-lookup"><span data-stu-id="37e52-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="37e52-230">ID : HELLO \_ MUI \_ Str \_ 0.</span><span class="sxs-lookup"><span data-stu-id="37e52-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="37e52-231">Valeur : 0.</span><span class="sxs-lookup"><span data-stu-id="37e52-231">Value: 0.</span></span>
            3.  <span data-ttu-id="37e52-232">Légende : Bonjour.</span><span class="sxs-lookup"><span data-stu-id="37e52-232">Caption: Hello.</span></span>

        <span data-ttu-id="37e52-233">Si vous affichez HelloModule. RC en tant que texte, vous verrez plusieurs éléments de code source spécifiques aux ressources.</span><span class="sxs-lookup"><span data-stu-id="37e52-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="37e52-234">L’un des plus intéressants est la section qui décrit la chaîne « Hello » :</span><span class="sxs-lookup"><span data-stu-id="37e52-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        <span data-ttu-id="37e52-235">Cette chaîne « Hello » est la ressource qui doit être localisée (traduite) dans chaque langue que l’application espère prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="37e52-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="37e52-236">Par exemple, le HelloModule \_ ta \_ dans le projet (que vous allez créer à l’étape suivante) contient sa propre version localisée de HelloModule. RC pour « ta » :</span><span class="sxs-lookup"><span data-stu-id="37e52-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  <span data-ttu-id="37e52-237">Générez le \_ \_ projet HelloModule en US pour vous assurer qu’il n’y a pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="37e52-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="37e52-238">Créez six projets supplémentaires dans la solution HelloMUI (ou autant que vous le souhaitez) pour créer six autres dll de ressources pour d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="37e52-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="37e52-239">Utilisez les valeurs de ce tableau :</span><span class="sxs-lookup"><span data-stu-id="37e52-239">Use the values in this table:</span></span>

    | <span data-ttu-id="37e52-240">Nom du projet</span><span class="sxs-lookup"><span data-stu-id="37e52-240">Project name</span></span>        | <span data-ttu-id="37e52-241">Nom du fichier. RC</span><span class="sxs-lookup"><span data-stu-id="37e52-241">Name of .rc file</span></span> | <span data-ttu-id="37e52-242">Identificateur de chaîne</span><span class="sxs-lookup"><span data-stu-id="37e52-242">String ID</span></span>          | <span data-ttu-id="37e52-243">Valeur de chaîne</span><span class="sxs-lookup"><span data-stu-id="37e52-243">String value</span></span> | <span data-ttu-id="37e52-244">Légende de la chaîne</span><span class="sxs-lookup"><span data-stu-id="37e52-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="37e52-245">HelloModule \_ de \_</span><span class="sxs-lookup"><span data-stu-id="37e52-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="37e52-246">HelloModule</span><span class="sxs-lookup"><span data-stu-id="37e52-246">HelloModule</span></span>      | <span data-ttu-id="37e52-247">HELLO \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e52-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="37e52-248">0</span><span class="sxs-lookup"><span data-stu-id="37e52-248">0</span></span>            | <span data-ttu-id="37e52-249">Hallo</span><span class="sxs-lookup"><span data-stu-id="37e52-249">Hallo</span></span>          |
    | <span data-ttu-id="37e52-250">HelloModule \_ es \_ es</span><span class="sxs-lookup"><span data-stu-id="37e52-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="37e52-251">HelloModule</span><span class="sxs-lookup"><span data-stu-id="37e52-251">HelloModule</span></span>      | <span data-ttu-id="37e52-252">HELLO \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e52-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="37e52-253">0</span><span class="sxs-lookup"><span data-stu-id="37e52-253">0</span></span>            | <span data-ttu-id="37e52-254">Hola</span><span class="sxs-lookup"><span data-stu-id="37e52-254">Hola</span></span>           |
    | <span data-ttu-id="37e52-255">HelloModule \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="37e52-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="37e52-256">HelloModule</span><span class="sxs-lookup"><span data-stu-id="37e52-256">HelloModule</span></span>      | <span data-ttu-id="37e52-257">HELLO \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e52-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="37e52-258">0</span><span class="sxs-lookup"><span data-stu-id="37e52-258">0</span></span>            | <span data-ttu-id="37e52-259">Bonjour</span><span class="sxs-lookup"><span data-stu-id="37e52-259">Bonjour</span></span>        |
    | <span data-ttu-id="37e52-260">HelloModule \_ Hi \_ in</span><span class="sxs-lookup"><span data-stu-id="37e52-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="37e52-261">HelloModule</span><span class="sxs-lookup"><span data-stu-id="37e52-261">HelloModule</span></span>      | <span data-ttu-id="37e52-262">HELLO \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e52-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="37e52-263">0</span><span class="sxs-lookup"><span data-stu-id="37e52-263">0</span></span>            | <span data-ttu-id="37e52-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="37e52-264">नमस्</span></span>           |
    | <span data-ttu-id="37e52-265">Ru \_ ru HelloModule \_</span><span class="sxs-lookup"><span data-stu-id="37e52-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="37e52-266">HelloModule</span><span class="sxs-lookup"><span data-stu-id="37e52-266">HelloModule</span></span>      | <span data-ttu-id="37e52-267">HELLO \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e52-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="37e52-268">0</span><span class="sxs-lookup"><span data-stu-id="37e52-268">0</span></span>            | <span data-ttu-id="37e52-269">Здравствуйте</span><span class="sxs-lookup"><span data-stu-id="37e52-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="37e52-270">HelloModule \_ ta \_ dans</span><span class="sxs-lookup"><span data-stu-id="37e52-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="37e52-271">HelloModule</span><span class="sxs-lookup"><span data-stu-id="37e52-271">HelloModule</span></span>      | <span data-ttu-id="37e52-272">HELLO \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e52-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="37e52-273">0</span><span class="sxs-lookup"><span data-stu-id="37e52-273">0</span></span>            | <span data-ttu-id="37e52-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="37e52-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="37e52-275">Pour plus d’informations sur la syntaxe et la structure des fichiers. RC, consultez [à propos des fichiers de ressources](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="37e52-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="37e52-276">Étape 2 : génération du module de ressources de base</span><span class="sxs-lookup"><span data-stu-id="37e52-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="37e52-277">En utilisant les modèles de ressource précédents, la génération de l’un des sept projets HelloModule entraînerait la création de sept dll distinctes.</span><span class="sxs-lookup"><span data-stu-id="37e52-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="37e52-278">Chaque DLL contient une section de ressource avec une chaîne unique localisée dans la langue appropriée.</span><span class="sxs-lookup"><span data-stu-id="37e52-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="37e52-279">Bien qu’il soit approprié pour le modèle de ressource Win32 historique, cette conception ne tire pas parti de MUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="37e52-280">Dans le kit de développement logiciel (SDK) Windows Vista et versions ultérieures, MUI offre la possibilité de fractionner les exécutables en code source et en modules de contenu localisables.</span><span class="sxs-lookup"><span data-stu-id="37e52-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="37e52-281">Avec la personnalisation supplémentaire décrite plus loin à l’étape 5, les applications peuvent être activées pour que la prise en charge multilingue s’exécute sur les versions antérieures à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37e52-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="37e52-282">Les mécanismes principaux disponibles pour fractionner les ressources du code exécutable, à partir de Windows Vista, sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="37e52-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="37e52-283">À l’aide de rc.exe (compilateur RC) avec des commutateurs spécifiques, ou</span><span class="sxs-lookup"><span data-stu-id="37e52-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="37e52-284">À l’aide d’un outil de fractionnement de style après génération nommé muirct.exe.</span><span class="sxs-lookup"><span data-stu-id="37e52-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="37e52-285">Pour plus d’informations, consultez [utilitaires de ressource](resource-utilities.md) .</span><span class="sxs-lookup"><span data-stu-id="37e52-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="37e52-286">Par souci de simplicité, ce didacticiel utilise muirct.exe pour fractionner l’exécutable « Hello MUI ».</span><span class="sxs-lookup"><span data-stu-id="37e52-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="37e52-287">Fractionnement des différents modules de ressources linguistiques : vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="37e52-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="37e52-288">Un processus en plusieurs parties est impliqué dans le fractionnement des dll en un HelloModule.dll exécutable, ainsi qu’un HelloModule.dll. mui pour chacune des sept langues prises en charge dans ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="37e52-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="37e52-289">Cette vue d’ensemble décrit les étapes requises. la section suivante présente un fichier de commandes qui effectue ces étapes.</span><span class="sxs-lookup"><span data-stu-id="37e52-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="37e52-290">Tout d’abord, fractionnez le module HelloModule.dll en anglais uniquement à l’aide de la commande :</span><span class="sxs-lookup"><span data-stu-id="37e52-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="37e52-291">La ligne de commande ci-dessus utilise le fichier de configuration DoReverseMuiLoc. rcconfig.</span><span class="sxs-lookup"><span data-stu-id="37e52-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="37e52-292">Ce type de fichier de configuration est généralement utilisé par muirct.exe pour fractionner les ressources entre la DLL indépendante de la langue et les fichiers. mui dépendants de la langue.</span><span class="sxs-lookup"><span data-stu-id="37e52-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="37e52-293">Dans ce cas, le fichier XML DoReverseMuiLoc. rcconfig (répertorié dans la section suivante) indique de nombreux types de ressources, mais ils sont tous classés dans la catégorie de fichier « localizedResources » ou. mui, et il n’y a aucune ressource dans la catégorie indépendante de la langue.</span><span class="sxs-lookup"><span data-stu-id="37e52-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="37e52-294">Pour plus d’informations sur la préparation d’un fichier de configuration de ressources, consultez [préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="37e52-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="37e52-295">En plus de créer un fichier HelloModule.dll. mui qui contient la chaîne anglaise « Hello », muirct.exe incorpore également une ressource MUI dans le module HelloModule.dll pendant le fractionnement.</span><span class="sxs-lookup"><span data-stu-id="37e52-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="37e52-296">Afin de charger correctement au moment de l’exécution les ressources appropriées à partir des modules HelloModule.dll. mui spécifiques à une langue, les sommes de contrôle de chaque fichier. mui doivent être fixes pour correspondre aux sommes de contrôle du module de base-Neutral language-Neutral.</span><span class="sxs-lookup"><span data-stu-id="37e52-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="37e52-297">Cette opération s’effectue à l’aide d’une commande telle que :</span><span class="sxs-lookup"><span data-stu-id="37e52-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="37e52-298">De même, muirct.exe est appelé pour créer un fichier HelloModule.dll. mui pour chacun des autres langages.</span><span class="sxs-lookup"><span data-stu-id="37e52-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="37e52-299">Toutefois, dans ce cas, la DLL indépendante du langage est ignorée, car seule la première créée est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="37e52-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="37e52-300">Les commandes qui traitent les ressources espagnoles et françaises se présentent comme suit :</span><span class="sxs-lookup"><span data-stu-id="37e52-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="37e52-301">L’un des éléments les plus importants à noter dans les lignes de commande muirct.exe ci-dessus est que l’indicateur-x est utilisé pour spécifier un ID de langue cible.</span><span class="sxs-lookup"><span data-stu-id="37e52-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="37e52-302">La valeur fournie à muirct.exe est différente pour chaque module HelloModule.dll spécifique à une langue.</span><span class="sxs-lookup"><span data-stu-id="37e52-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="37e52-303">Cette valeur de langue est centrale et est utilisée par muirct.exe pour marquer de manière appropriée le fichier. mui durant le fractionnement.</span><span class="sxs-lookup"><span data-stu-id="37e52-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="37e52-304">Une valeur incorrecte génère des échecs de chargement des ressources pour ce fichier. mui particulier au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="37e52-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="37e52-305">Pour plus d’informations sur le mappage du nom de langage à LCID [, consultez constantes et chaînes](language-identifier-constants-and-strings.md) de l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="37e52-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="37e52-306">Chaque fichier. mui Split finit par être placé dans un répertoire correspondant à son nom de langue, immédiatement sous le répertoire dans lequel les HelloModule.dll indépendantes de la langue se trouvent.</span><span class="sxs-lookup"><span data-stu-id="37e52-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="37e52-307">Pour plus d’informations sur l’emplacement des fichiers. mui, consultez [déploiement d’applications](application-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="37e52-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="37e52-308">Fractionnement des différents modules de ressources linguistiques : création des fichiers</span><span class="sxs-lookup"><span data-stu-id="37e52-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="37e52-309">Pour ce didacticiel, vous créez un fichier de commandes contenant les commandes pour fractionner les différentes dll et vous l’appelez manuellement.</span><span class="sxs-lookup"><span data-stu-id="37e52-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="37e52-310">Notez que dans le cadre du travail de développement réel, vous pouvez réduire le risque d’erreurs de génération en incluant ces commandes en tant qu’événements pré-build ou après génération dans la solution HelloMUI, mais cela n’entre pas dans le cadre de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="37e52-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="37e52-311">Créez les fichiers pour la version Debug :</span><span class="sxs-lookup"><span data-stu-id="37e52-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="37e52-312">Créez un fichier de commandes DoReverseMuiLoc. cmd contenant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="37e52-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  <span data-ttu-id="37e52-313">Créez un fichier XML DoReverseMuiLoc. rcconfig contenant les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="37e52-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  <span data-ttu-id="37e52-314">Copiez DoReverseMuiLoc. cmd et DoReverseMuiLoc. rcconfig sur *ProjectRootDirectory* \\ HelloMUI \\ Debug.</span><span class="sxs-lookup"><span data-stu-id="37e52-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="37e52-315">Ouvrez l’invite de commandes de Visual Studio 2008 et accédez au répertoire de débogage.</span><span class="sxs-lookup"><span data-stu-id="37e52-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="37e52-316">Exécutez DoReverseMuiLoc. cmd.</span><span class="sxs-lookup"><span data-stu-id="37e52-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="37e52-317">Lorsque vous créez une version Release, vous copiez les mêmes fichiers DoReverseMuiLoc. cmd et DoReverseMuiLoc. rcconfig dans le répertoire de mise en version, puis vous exécutez le fichier de commandes.</span><span class="sxs-lookup"><span data-stu-id="37e52-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="37e52-318">Étape 3 : création d’un Resource-Savvy « Hello MUI »</span><span class="sxs-lookup"><span data-stu-id="37e52-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="37e52-319">En s’appuyant sur le0.exe GuiStep initial codé en dur \_ de l’exemple ci-dessus, vous pouviez étendre la portée de l’application à plusieurs utilisateurs de langage en choisissant d’incorporer le modèle de ressource Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="37e52-320">Le nouveau code d’exécution présenté dans cette étape comprend la logique de chargement de module ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) et de récupération de chaîne ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).</span><span class="sxs-lookup"><span data-stu-id="37e52-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="37e52-321">Ajoutez un nouveau projet à la solution HelloMUI (à l’aide du fichier de sélection de menu, ajoutez et nouveau projet) avec les paramètres et valeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="37e52-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="37e52-322">Type de projet : projet Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="37e52-323">Nom : GuiStep \_ 1.</span><span class="sxs-lookup"><span data-stu-id="37e52-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="37e52-324">Emplacement : acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="37e52-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="37e52-325">Dans l’Assistant application Win32, sélectionnez le type d’application par défaut : application Windows.</span><span class="sxs-lookup"><span data-stu-id="37e52-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="37e52-326">Définissez ce projet pour qu’il s’exécute à partir de Visual Studio et configurez son modèle de thread :</span><span class="sxs-lookup"><span data-stu-id="37e52-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="37e52-327">Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 1, puis sélectionnez Définir comme projet de démarrage.</span><span class="sxs-lookup"><span data-stu-id="37e52-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="37e52-328">Cliquez à nouveau avec le bouton droit et sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="37e52-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="37e52-329">Dans la boîte de dialogue pages de propriétés du projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="37e52-330">Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.</span><span class="sxs-lookup"><span data-stu-id="37e52-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="37e52-331">Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="37e52-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="37e52-332">Remplacez le contenu de GuiStep \_ 1. cpp par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="37e52-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  <span data-ttu-id="37e52-333">Générez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="37e52-333">Build and run the application.</span></span> <span data-ttu-id="37e52-334">La sortie s’affiche dans la langue actuellement définie en tant que langue d’affichage de l’ordinateur (à condition qu’il s’agit de l’une des sept langues que nous avons générées).</span><span class="sxs-lookup"><span data-stu-id="37e52-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="37e52-335">Étape 4 : globalisation de « Hello MUI »</span><span class="sxs-lookup"><span data-stu-id="37e52-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="37e52-336">Bien que l’exemple précédent soit en mesure d’afficher sa sortie dans différentes langues, il est très petit dans plusieurs domaines.</span><span class="sxs-lookup"><span data-stu-id="37e52-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="37e52-337">Le plus notable est peut-être que l’application n’est disponible que dans un petit sous-ensemble de langues par rapport au système d’exploitation Windows lui-même.</span><span class="sxs-lookup"><span data-stu-id="37e52-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="37e52-338">Si, par exemple, l' \_ application GuiStep 1 de l’étape précédente ont été installées sur une version japonaise de Windows, des échecs d’emplacement de ressource seraient probablement possibles.</span><span class="sxs-lookup"><span data-stu-id="37e52-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="37e52-339">Pour résoudre ce problème, vous avez deux options principales :</span><span class="sxs-lookup"><span data-stu-id="37e52-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="37e52-340">Assurez-vous que les ressources d’un langage de secours ultime prédéterminé sont incluses.</span><span class="sxs-lookup"><span data-stu-id="37e52-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="37e52-341">Permet à l’utilisateur final de configurer ses préférences linguistiques parmi le sous-ensemble de langues spécifiquement pris en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="37e52-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="37e52-342">Parmi ces options, celle qui fournit un langage de secours ultime est très recommandée et est implémentée dans ce didacticiel en passant l’indicateur-g à muirct.exe, comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="37e52-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="37e52-343">Cet indicateur indique muirct.exe d’effectuer une langue spécifique (de-0x0407) pour le langage de secours ultime associé au module dll indépendant du langage (HelloModule.dll).</span><span class="sxs-lookup"><span data-stu-id="37e52-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="37e52-344">Au moment de l’exécution, ce paramètre est utilisé en dernier recours pour générer du texte à afficher à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37e52-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="37e52-345">Dans le cas où un langage de secours ultime est introuvable et qu’aucune ressource appropriée n’est disponible dans le fichier binaire indépendant de la langue, le chargement de la ressource échoue.</span><span class="sxs-lookup"><span data-stu-id="37e52-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="37e52-346">Par conséquent, vous devez déterminer avec soin les scénarios que votre application peut rencontrer et planifier le langage de secours ultime en conséquence.</span><span class="sxs-lookup"><span data-stu-id="37e52-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="37e52-347">L’autre option qui consiste à autoriser les préférences linguistiques configurables et à charger des ressources basées sur cette hiérarchie définie par l’utilisateur peut augmenter la satisfaction des clients.</span><span class="sxs-lookup"><span data-stu-id="37e52-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="37e52-348">Malheureusement, cela complique également les fonctionnalités nécessaires au sein de l’application.</span><span class="sxs-lookup"><span data-stu-id="37e52-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="37e52-349">Cette étape du didacticiel utilise un mécanisme de fichier texte simplifié pour activer la configuration linguistique personnalisée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37e52-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="37e52-350">Le fichier texte est analysé au moment de l’exécution par l’application, et la liste des langues analysées et validées est utilisée pour établir une liste de secours personnalisée.</span><span class="sxs-lookup"><span data-stu-id="37e52-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="37e52-351">Une fois la liste de secours personnalisée établie, les API Windows chargent les ressources en fonction de la priorité de langue définie dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="37e52-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="37e52-352">Le reste du code est similaire à celui trouvé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="37e52-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="37e52-353">Ajoutez un nouveau projet à la solution HelloMUI (à l’aide du fichier de sélection de menu, ajoutez et nouveau projet) avec les paramètres et valeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="37e52-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="37e52-354">Type de projet : projet Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="37e52-355">Nom : GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="37e52-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="37e52-356">Emplacement : acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="37e52-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="37e52-357">Dans l’Assistant application Win32, sélectionnez le type d’application par défaut : application Windows.</span><span class="sxs-lookup"><span data-stu-id="37e52-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="37e52-358">Définissez ce projet pour qu’il s’exécute à partir de Visual Studio et configurez son modèle de thread :</span><span class="sxs-lookup"><span data-stu-id="37e52-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="37e52-359">Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 2 et sélectionnez Définir comme projet de démarrage.</span><span class="sxs-lookup"><span data-stu-id="37e52-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="37e52-360">Cliquez à nouveau avec le bouton droit et sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="37e52-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="37e52-361">Dans la boîte de dialogue pages de propriétés du projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="37e52-362">Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.</span><span class="sxs-lookup"><span data-stu-id="37e52-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="37e52-363">Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="37e52-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="37e52-364">Remplacez le contenu de GuiStep \_ 2. cpp par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="37e52-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="37e52-365">Créez un fichier texte Unicode langs.txt contenant la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="37e52-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="37e52-366">Veillez à enregistrer le fichier au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="37e52-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="37e52-367">Copiez langs.txt dans le répertoire à partir duquel le programme s’exécutera :</span><span class="sxs-lookup"><span data-stu-id="37e52-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="37e52-368">Si vous exécutez à partir de Visual Studio, copiez-le dans *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="37e52-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="37e52-369">Si vous exécutez à partir de l’Explorateur Windows, copiez-le dans le même répertoire que GuiStep \_2.exe.</span><span class="sxs-lookup"><span data-stu-id="37e52-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="37e52-370">Générez et exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="37e52-370">Build and run the project.</span></span> <span data-ttu-id="37e52-371">Essayez de modifier langs.txt pour que différentes langues s’affichent au début de la liste.</span><span class="sxs-lookup"><span data-stu-id="37e52-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="37e52-372">Étape 5 : personnalisation de « Hello MUI »</span><span class="sxs-lookup"><span data-stu-id="37e52-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="37e52-373">Un certain nombre de fonctionnalités d’exécution mentionnées jusqu’à présent dans ce didacticiel sont disponibles uniquement sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="37e52-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="37e52-374">Vous souhaiterez peut-être réutiliser les efforts investis dans la localisation et le fractionnement des ressources en faisant fonctionner l’application sur les versions de système d’exploitation Windows de niveau inférieur, telles que Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37e52-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="37e52-375">Ce processus implique l’ajustement de l’exemple précédent dans deux domaines clés :</span><span class="sxs-lookup"><span data-stu-id="37e52-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="37e52-376">Les fonctions de chargement des ressources antérieures à Windows Vista (telles que [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), etc.) ne prennent pas en charge l’interface MUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="37e52-377">Les applications qui sont livrées avec des ressources fractionnées (fichiers LN et. MUI) doivent charger les modules de ressources à l’aide de l’une des deux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="37e52-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="37e52-378">Si l’application doit être exécutée uniquement sur Windows Vista et versions ultérieures, elle doit charger les modules de ressources avec [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="37e52-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="37e52-379">Si l’application doit être exécutée sur des versions antérieures à Windows Vista, ainsi que sur Windows Vista ou version ultérieure, elle doit utiliser [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), qui est une fonction de niveau inférieur spécifique fournie dans le kit de développement logiciel (SDK) Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37e52-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="37e52-380">La prise en charge de l’ordre de gestion linguistique et de la langue de secours dans les versions antérieures à Windows Vista du système d’exploitation Windows diffère considérablement de celle de Windows Vista et des versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="37e52-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="37e52-381">Pour cette raison, les applications qui autorisent la langue de secours configurée par l’utilisateur doivent ajuster les pratiques de gestion de la langue :</span><span class="sxs-lookup"><span data-stu-id="37e52-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="37e52-382">Si l’application doit être exécutée uniquement sur Windows Vista et versions ultérieures, la définition de la liste de langues à l’aide de [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) est suffisante.</span><span class="sxs-lookup"><span data-stu-id="37e52-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="37e52-383">Si l’application doit être exécutée sur toutes les versions de Windows, du code doit être construit pour s’exécuter sur les plateformes de niveau inférieur pour itérer au sein de la liste des langues configurées par l’utilisateur et détecter le module de ressources souhaité.</span><span class="sxs-lookup"><span data-stu-id="37e52-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="37e52-384">Cela peut être observé dans les sections 1C et 2 du code fourni plus loin dans cette étape.</span><span class="sxs-lookup"><span data-stu-id="37e52-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="37e52-385">Créez un projet qui peut utiliser les modules de ressources localisés sur n’importe quelle version de Windows :</span><span class="sxs-lookup"><span data-stu-id="37e52-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="37e52-386">Ajoutez un nouveau projet à la solution HelloMUI (à l’aide du fichier de sélection de menu, ajoutez et nouveau projet) avec les paramètres et valeurs suivants :</span><span class="sxs-lookup"><span data-stu-id="37e52-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="37e52-387">Type de projet : projet Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="37e52-388">Nom : GuiStep \_ 3.</span><span class="sxs-lookup"><span data-stu-id="37e52-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="37e52-389">Emplacement : acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="37e52-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="37e52-390">Dans l’Assistant application Win32, sélectionnez le type d’application par défaut : application Windows.</span><span class="sxs-lookup"><span data-stu-id="37e52-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="37e52-391">Définissez ce projet pour qu’il s’exécute à partir de Visual Studio et configurez son modèle de thread.</span><span class="sxs-lookup"><span data-stu-id="37e52-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="37e52-392">En outre, configurez-le pour ajouter les en-têtes et les bibliothèques nécessaires.</span><span class="sxs-lookup"><span data-stu-id="37e52-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="37e52-393">Les chemins d’accès utilisés dans ce didacticiel supposent que le kit de développement logiciel (SDK) Windows 7 et le package des API de niveau inférieur de Microsoft NLS ont été installés dans leurs répertoires par défaut.</span><span class="sxs-lookup"><span data-stu-id="37e52-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="37e52-394">Si ce n’est pas le cas, modifiez les chemins d’accès de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="37e52-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="37e52-395">Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 3 et sélectionnez Définir comme projet de démarrage.</span><span class="sxs-lookup"><span data-stu-id="37e52-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="37e52-396">Cliquez à nouveau avec le bouton droit et sélectionnez Propriétés.</span><span class="sxs-lookup"><span data-stu-id="37e52-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="37e52-397">Dans la boîte de dialogue pages de propriétés du projet :</span><span class="sxs-lookup"><span data-stu-id="37e52-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="37e52-398">Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.</span><span class="sxs-lookup"><span data-stu-id="37e52-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="37e52-399">Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).</span><span class="sxs-lookup"><span data-stu-id="37e52-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="37e52-400">Sélectionnez général et ajouter aux autres répertoires Include :</span><span class="sxs-lookup"><span data-stu-id="37e52-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="37e52-401">« C : \\ API de niveau inférieur de Microsoft nls \\ include ».</span><span class="sxs-lookup"><span data-stu-id="37e52-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="37e52-402">Sélectionnez langage et Set traiter WCHAR \_ t comme type intégré : non (/Zc : WCHAR \_ t-).</span><span class="sxs-lookup"><span data-stu-id="37e52-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="37e52-403">Sélectionnez avancé et définissez Convention d’appel : \_ StdCall (/GZ).</span><span class="sxs-lookup"><span data-stu-id="37e52-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="37e52-404">Sous propriétés de configuration, développez éditeur de liens, sélectionnez entrée, puis ajoutez à des dépendances supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="37e52-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="37e52-405">« C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ lib \\ MUILoad. lib ».</span><span class="sxs-lookup"><span data-stu-id="37e52-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="37e52-406">« C : \\ API de niveau inférieur Microsoft nls \\ lib \\ x86 \\ nlsdl. lib ».</span><span class="sxs-lookup"><span data-stu-id="37e52-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="37e52-407">Remplacez le contenu de GuiStep \_ 3. cpp par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="37e52-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="37e52-408">Créez ou copiez langs.txt dans le répertoire approprié, comme décrit précédemment à l ['étape 4 : globalisation de « Hello MUI »](#step-4-globalizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="37e52-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="37e52-409">Générez et exécutez le projet.</span><span class="sxs-lookup"><span data-stu-id="37e52-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="37e52-410">Si l’application doit s’exécuter sur des versions de Windows antérieures à Windows Vista, veillez à lire les documents fournis avec le package des [API de niveau inférieur de Microsoft nls](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) pour savoir comment redistribuer Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="37e52-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="37e52-411">Considérations supplémentaires pour MUI</span><span class="sxs-lookup"><span data-stu-id="37e52-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="37e52-412">Prise en charge des applications console</span><span class="sxs-lookup"><span data-stu-id="37e52-412">Support for Console Applications</span></span>

<span data-ttu-id="37e52-413">Les techniques abordées dans ce didacticiel peuvent également être utilisées dans les applications console.</span><span class="sxs-lookup"><span data-stu-id="37e52-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="37e52-414">Toutefois, contrairement à la plupart des contrôles d’interface utilisateur graphique standard, la fenêtre de commande Windows ne peut pas afficher de caractères pour tous les langages.</span><span class="sxs-lookup"><span data-stu-id="37e52-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="37e52-415">Pour cette raison, les applications console multilingues requièrent une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="37e52-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="37e52-416">L’appel des API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) ou [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) avec des indicateurs de filtrage spécifiques entraîne la suppression, par les fonctions de chargement des ressources, des sondes de ressources de langue pour des langues spécifiques qui ne sont normalement pas affichées dans une fenêtre de commande.</span><span class="sxs-lookup"><span data-stu-id="37e52-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="37e52-417">Lorsque ces indicateurs sont définis, les algorithmes de définition de langue autorisent uniquement les langues qui s’affichent correctement dans la fenêtre de commande à se trouver dans la liste de secours.</span><span class="sxs-lookup"><span data-stu-id="37e52-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="37e52-418">Pour plus d’informations sur l’utilisation de ces API pour générer une application console multilingue, consultez les sections Notes de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) et [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="37e52-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="37e52-419">Détermination des langues à prendre en charge au Run-Time</span><span class="sxs-lookup"><span data-stu-id="37e52-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="37e52-420">Vous pouvez adopter l’une des suggestions de conception suivantes pour déterminer les langues que votre application doit prendre en charge au moment de l’exécution :</span><span class="sxs-lookup"><span data-stu-id="37e52-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="37e52-421">**Pendant l’installation, autorisez l’utilisateur final à sélectionner la langue par défaut dans la liste des langues prises en charge.**</span><span class="sxs-lookup"><span data-stu-id="37e52-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="37e52-422">**Lire une liste de langues à partir d’un fichier de configuration**</span><span class="sxs-lookup"><span data-stu-id="37e52-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="37e52-423">Certains des projets de ce didacticiel contiennent une fonction utilisée pour analyser un fichier de configuration langs.txt, qui contient une liste de langues.</span><span class="sxs-lookup"><span data-stu-id="37e52-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="37e52-424">Étant donné que cette fonction prend une entrée externe, validez les langues fournies comme entrée.</span><span class="sxs-lookup"><span data-stu-id="37e52-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="37e52-425">Pour plus d’informations sur l’exécution de cette validation, consultez les fonctions [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) ou [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) .</span><span class="sxs-lookup"><span data-stu-id="37e52-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="37e52-426">**Interroger le système d’exploitation pour déterminer les langues installées**</span><span class="sxs-lookup"><span data-stu-id="37e52-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="37e52-427">Cette approche permet à l’application d’utiliser la même langue que le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="37e52-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="37e52-428">Bien que cela ne nécessite pas d’invite de l’utilisateur, si vous choisissez cette option, sachez que les langues du système d’exploitation peuvent être ajoutées ou supprimées à tout moment et peuvent changer après l’installation de l’application par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37e52-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="37e52-429">Sachez également que dans certains cas, le système d’exploitation est installé avec une prise en charge de langue limitée, et l’application offre plus de valeur si elle prend en charge les langues que le système d’exploitation ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="37e52-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="37e52-430">Pour plus d’informations sur la façon de déterminer les langues actuellement installées dans le système d’exploitation, consultez la fonction [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .</span><span class="sxs-lookup"><span data-stu-id="37e52-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="37e52-431">Prise en charge des scripts complexes dans les versions antérieures à Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37e52-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="37e52-432">Lorsqu’une application qui prend en charge certains scripts complexes s’exécute sur une version de Windows antérieure à Windows Vista, le texte de ce script peut ne pas s’afficher correctement dans les composants de l’interface utilisateur graphique.</span><span class="sxs-lookup"><span data-stu-id="37e52-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="37e52-433">Par exemple, dans le projet de niveau inférieur de ce didacticiel, les scripts hi-IN et ta peuvent ne pas s’afficher dans la boîte de message en raison de problèmes liés au traitement de scripts complexes et au manque de polices associées.</span><span class="sxs-lookup"><span data-stu-id="37e52-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="37e52-434">En règle générale, les problèmes de cette nature se présentent sous forme de carrés dans le composant GUI.</span><span class="sxs-lookup"><span data-stu-id="37e52-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="37e52-435">Pour plus d’informations sur l’activation du traitement complexe des scripts [, consultez prise en charge des scripts et des polices dans Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span><span class="sxs-lookup"><span data-stu-id="37e52-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="37e52-436">Résumé</span><span class="sxs-lookup"><span data-stu-id="37e52-436">Summary</span></span>

<span data-ttu-id="37e52-437">Ce didacticiel a globalisé une application monolingue et a démontré les meilleures pratiques suivantes.</span><span class="sxs-lookup"><span data-stu-id="37e52-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="37e52-438">Concevez l’application pour tirer parti du modèle de ressource Win32.</span><span class="sxs-lookup"><span data-stu-id="37e52-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="37e52-439">Utilisez le fractionnement MUI des ressources en fichiers binaires satellites (fichiers. MUI).</span><span class="sxs-lookup"><span data-stu-id="37e52-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="37e52-440">Assurez-vous que le processus de localisation met à jour les ressources dans les fichiers. mui afin qu’elles soient adaptées à la langue cible.</span><span class="sxs-lookup"><span data-stu-id="37e52-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="37e52-441">Assurez-vous que l’empaquetage et le déploiement de l’application, des fichiers. mui associés et du contenu de configuration sont effectués correctement pour permettre aux API de chargement des ressources de rechercher le contenu localisé.</span><span class="sxs-lookup"><span data-stu-id="37e52-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="37e52-442">Fournissez à l’utilisateur final un mécanisme pour ajuster la configuration de la langue de l’application.</span><span class="sxs-lookup"><span data-stu-id="37e52-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="37e52-443">Ajustez le code d’exécution pour tirer parti de la configuration du langage, afin de rendre l’application plus réactive aux besoins de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="37e52-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
