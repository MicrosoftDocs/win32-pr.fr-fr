---
description: Windows Server 2008 R2 ajoute la prise en charge de la reconnaissance de l’écriture manuscrite côté serveur à Windows. Cette rubrique explique comment reconnaître l’écriture manuscrite dans Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconnaissance de l’écriture manuscrite dans Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032055"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="64a96-104">Reconnaissance de l’écriture manuscrite dans Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64a96-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="64a96-105">Windows Server 2008 R2 prend en charge la reconnaissance de l’écriture manuscrite côté serveur.</span><span class="sxs-lookup"><span data-stu-id="64a96-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="64a96-106">La reconnaissance côté serveur permet à un serveur de reconnaître du contenu à partir d’une entrée de stylet sur des pages Web.</span><span class="sxs-lookup"><span data-stu-id="64a96-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="64a96-107">Cela s’avère particulièrement utile lorsque les utilisateurs d’un réseau spécifient des termes qui sont interprétés à l’aide d’un dictionnaire personnalisé.</span><span class="sxs-lookup"><span data-stu-id="64a96-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="64a96-108">Par exemple, si vous avez une application médicale qui a interrogé une base de données de serveur pour connaître les noms des patients, ces noms peuvent être ajoutés à une autre base de données qui serait transmise à l’aide de recherches à partir d’un formulaire Silverlight manuscrit.</span><span class="sxs-lookup"><span data-stu-id="64a96-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="64a96-109">Configurer votre serveur pour la reconnaissance Server-Side</span><span class="sxs-lookup"><span data-stu-id="64a96-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="64a96-110">Les étapes suivantes doivent être suivies pour configurer la reconnaissance côté serveur.</span><span class="sxs-lookup"><span data-stu-id="64a96-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="64a96-111">Installer Services de prise en charge de l’écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="64a96-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="64a96-112">Installer la prise en charge du serveur Web (IIS) et du serveur d’applications</span><span class="sxs-lookup"><span data-stu-id="64a96-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="64a96-113">Activer le rôle expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="64a96-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="64a96-114">Démarrer le service d’entrée Tablet PC</span><span class="sxs-lookup"><span data-stu-id="64a96-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="64a96-115">Installer Services de prise en charge de l’écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="64a96-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="64a96-116">Pour installer les services d’encre et d’écriture manuscrite, ouvrez le gestionnaire de serveur en cliquant sur l’icône Gestionnaire de serveur à partir de la barre de lancement rapide.</span><span class="sxs-lookup"><span data-stu-id="64a96-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="64a96-117">Dans le menu **fonctionnalités** , cliquez sur **Ajouter des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="64a96-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="64a96-118">Veillez à activer la case à cocher **services de prise en charge de l’écriture manuscrite** .</span><span class="sxs-lookup"><span data-stu-id="64a96-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="64a96-119">L’illustration suivante montre la boîte de dialogue **Sélectionner des fonctionnalités** avec **services de prise en charge de l’écriture manuscrite** sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64a96-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="64a96-120">![Case à cocher de la boîte de dialogue Sélectionner les fonctionnalités avec les services d’encre et d’écriture activée](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="64a96-121">*Case à cocher de la boîte de dialogue Sélectionner les fonctionnalités avec les services d’encre et d’écriture activée*</span><span class="sxs-lookup"><span data-stu-id="64a96-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="64a96-122">Prise en charge de l’installation du serveur Web (IIS) et du serveur d’applications</span><span class="sxs-lookup"><span data-stu-id="64a96-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="64a96-123">Ouvrez le gestionnaire de serveur comme vous l’avez fait pour la première étape.</span><span class="sxs-lookup"><span data-stu-id="64a96-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="64a96-124">Ensuite, vous devrez ajouter les rôles serveur Web (IIS) et serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="64a96-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="64a96-125">Dans le menu **rôles** , cliquez sur **Ajouter des rôles**.</span><span class="sxs-lookup"><span data-stu-id="64a96-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="64a96-126">L’Assistant Ajout de rôles s’affiche.</span><span class="sxs-lookup"><span data-stu-id="64a96-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="64a96-127">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="64a96-127">Click **Next**.</span></span> <span data-ttu-id="64a96-128">Assurez-vous que **serveur d’applications** et **serveur Web (IIS)** sont sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="64a96-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="64a96-129">L’illustration suivante montre la boîte de dialogue **Sélectionner des rôles de serveurs** avec les rôles serveur **Web (IIS)** et **serveur d’applications** sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="64a96-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="64a96-130">![Boîte de dialogue Sélectionner des rôles de serveurs avec les rôles serveur Web (IIS) et serveur d’applications sélectionnés](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="64a96-131">*Boîte de dialogue Sélectionner des rôles de serveurs avec les rôles serveur Web (IIS) et serveur d’applications sélectionnés*</span><span class="sxs-lookup"><span data-stu-id="64a96-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="64a96-132">Lorsque vous sélectionnez le **serveur d’applications**, vous êtes invité à installer l’infrastructure ASP.net.</span><span class="sxs-lookup"><span data-stu-id="64a96-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="64a96-133">Cliquez sur le bouton **Ajouter les fonctionnalités requises** .</span><span class="sxs-lookup"><span data-stu-id="64a96-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="64a96-134">Une fois que vous avez cliqué sur **suivant**, une boîte de dialogue d’aperçu s’affiche. Cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="64a96-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="64a96-135">La boîte de dialogue **Sélectionner des services de rôle** doit maintenant être disponible.</span><span class="sxs-lookup"><span data-stu-id="64a96-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="64a96-136">Vérifiez que **serveur Web (IIS)** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="64a96-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="64a96-137">L’illustration suivante montre la boîte de dialogue **Sélectionner les services de rôle** avec le serveur Web (IIS) activé.</span><span class="sxs-lookup"><span data-stu-id="64a96-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="64a96-138">![Boîte de dialogue Sélectionner les services de rôle avec le serveur Web (IIS) activé](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="64a96-139">*Boîte de dialogue Sélectionner les services de rôle avec le serveur Web (IIS) activé*</span><span class="sxs-lookup"><span data-stu-id="64a96-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="64a96-140">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="64a96-140">Click **Next**.</span></span> <span data-ttu-id="64a96-141">Une boîte de dialogue vue d’ensemble s’affiche. Cliquez de nouveau sur **suivant** .</span><span class="sxs-lookup"><span data-stu-id="64a96-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="64a96-142">Vous voyez maintenant une page proposant des options pour les rôles de serveur Web (IIS).</span><span class="sxs-lookup"><span data-stu-id="64a96-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="64a96-143">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="64a96-143">Click **Next**.</span></span> <span data-ttu-id="64a96-144">Sur la page suivante, le bouton **installer** devient actif.</span><span class="sxs-lookup"><span data-stu-id="64a96-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="64a96-145">Cliquez sur **installer** pour installer la prise en charge du serveur Web (IIS) et du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="64a96-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="64a96-146">Activer le rôle expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="64a96-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="64a96-147">Pour activer la fonctionnalité expérience utilisateur, cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **Gestionnaire de serveur**.</span><span class="sxs-lookup"><span data-stu-id="64a96-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="64a96-148">Sélectionnez **Ajouter des services** , puis sélectionnez le service **expérience utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="64a96-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="64a96-149">L’illustration suivante montre la boîte de dialogue **Sélectionner des fonctionnalités** avec l’option expérience utilisateur installée.</span><span class="sxs-lookup"><span data-stu-id="64a96-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="64a96-150">![Boîte de dialogue Sélectionner les fonctionnalités avec le service expérience utilisateur sélectionné](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="64a96-151">*Boîte de dialogue Sélectionner les fonctionnalités avec le service expérience utilisateur sélectionné*</span><span class="sxs-lookup"><span data-stu-id="64a96-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="64a96-152">Cliquez sur **suivant** pour installer la fonctionnalité expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="64a96-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="64a96-153">Démarrer le service tablette</span><span class="sxs-lookup"><span data-stu-id="64a96-153">Start the Tablet Service</span></span>

<span data-ttu-id="64a96-154">Une fois que vous avez installé le service expérience utilisateur, le service d’entrée du Tablet PC s’affiche dans le menu **services** .</span><span class="sxs-lookup"><span data-stu-id="64a96-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="64a96-155">Pour accéder au menu **services** , cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **services**.</span><span class="sxs-lookup"><span data-stu-id="64a96-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="64a96-156">Pour démarrer le service, cliquez avec le bouton droit sur **service d’entrée du Tablet PC** , puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="64a96-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="64a96-157">L’illustration suivante montre le menu **services** avec le service d’entrée Tablet PC démarré.</span><span class="sxs-lookup"><span data-stu-id="64a96-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="64a96-158">![Menu services avec le service d’entrée Tablet PC démarré](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="64a96-159">*Menu services avec le service d’entrée Tablet PC démarré*</span><span class="sxs-lookup"><span data-stu-id="64a96-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="64a96-160">Exécution de la reconnaissance des Server-Side à l’aide de Silverlight</span><span class="sxs-lookup"><span data-stu-id="64a96-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="64a96-161">Cette section montre comment créer une application Web qui utilise Silverlight pour capturer une entrée d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="64a96-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="64a96-162">Pour programmer le module de reconnaissance dans Visual Studio 2008, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="64a96-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="64a96-163">Installez et mettez à jour Visual Studio 2008 pour ajouter la prise en charge de Silverlight.</span><span class="sxs-lookup"><span data-stu-id="64a96-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="64a96-164">Créez un projet Silverlight dans Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="64a96-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="64a96-165">Ajoutez les références de service nécessaires à votre projet.</span><span class="sxs-lookup"><span data-stu-id="64a96-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="64a96-166">Créez un service WCF Silverlight pour la reconnaissance de l’encre.</span><span class="sxs-lookup"><span data-stu-id="64a96-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="64a96-167">Ajoutez la référence de service à votre projet client.</span><span class="sxs-lookup"><span data-stu-id="64a96-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="64a96-168">Ajoutez la classe InkCollector au projet InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="64a96-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="64a96-169">Supprimer les directives de transport sécurisées de la configuration du client</span><span class="sxs-lookup"><span data-stu-id="64a96-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="64a96-170">Installer et mettre à jour Visual Studio 2008 pour ajouter la prise en charge de Silverlight</span><span class="sxs-lookup"><span data-stu-id="64a96-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="64a96-171">Avant de commencer, vous devez effectuer les étapes suivantes sur votre serveur Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="64a96-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="64a96-172">Installez Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="64a96-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="64a96-173">Installez [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span><span class="sxs-lookup"><span data-stu-id="64a96-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="64a96-174">Installez le [Kit de développement logiciel (SDK) Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).</span><span class="sxs-lookup"><span data-stu-id="64a96-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="64a96-175">Après avoir installé ces applications et mises à jour, vous êtes prêt à créer votre application Web de reconnaissance côté serveur.</span><span class="sxs-lookup"><span data-stu-id="64a96-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="64a96-176">Créer un projet Web Silverlight dans Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="64a96-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="64a96-177">Dans le menu **Fichier**, cliquez sur **Nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="64a96-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="64a96-178">Sélectionnez le modèle application Silverlight dans la \# liste projet Visual C.</span><span class="sxs-lookup"><span data-stu-id="64a96-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="64a96-179">Nommez votre projet InkRecognition, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a96-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="64a96-180">L’illustration suivante montre le \# projet Silverlight C sélectionné et nommé InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="64a96-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="64a96-181">![\#projet Silverlight c sélectionné, avec le nom InkRecognition](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="64a96-182">*\#projet Silverlight c sélectionné, avec le nom InkRecognition*</span><span class="sxs-lookup"><span data-stu-id="64a96-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="64a96-183">Une fois que vous avez cliqué sur **OK**, une boîte de dialogue vous invite à ajouter une application Silverlight à votre projet.</span><span class="sxs-lookup"><span data-stu-id="64a96-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="64a96-184">Sélectionnez **Ajouter un nouveau projet Web ASP.net à la solution pour héberger Silverlight** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a96-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="64a96-185">L’illustration suivante montre comment configurer l’exemple de projet avant de cliquer sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a96-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="64a96-186">![Boîte de dialogue avec invite pour ajouter une application Silverlight à un projet](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="64a96-187">*Boîte de dialogue avec invite pour ajouter une application Silverlight à un projet*</span><span class="sxs-lookup"><span data-stu-id="64a96-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="64a96-188">Ajouter les références de service nécessaires à votre projet</span><span class="sxs-lookup"><span data-stu-id="64a96-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="64a96-189">Vous avez maintenant votre projet client Silverlight générique (InkRecognition) avec un projet Web (InkRecognition. Web) configuré dans votre solution.</span><span class="sxs-lookup"><span data-stu-id="64a96-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="64a96-190">Le projet s’ouvre avec page. xaml et default. aspx ouvert.</span><span class="sxs-lookup"><span data-stu-id="64a96-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="64a96-191">Fermez ces fenêtres et ajoutez les références System. Runtime. Serialization et System. ServiceModel au projet InkRecognition en cliquant avec le bouton droit sur le dossier références dans le projet InkRecognition et en sélectionnant **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="64a96-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="64a96-192">L’illustration suivante montre la boîte de dialogue avec les références requises sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="64a96-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="64a96-193">![Boîte de dialogue Ajouter des références avec System. Runtime. Serialization et System. ServiceModel sélectionné](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="64a96-194">*Boîte de dialogue Ajouter des références avec System. Runtime. Serialization et System. ServiceModel sélectionné*</span><span class="sxs-lookup"><span data-stu-id="64a96-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="64a96-195">Ensuite, vous devez ajouter les références System. ServiceModel et Microsoft. Ink au projet InkRecognition. Web.</span><span class="sxs-lookup"><span data-stu-id="64a96-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="64a96-196">La référence Microsoft. Ink n’apparaît pas dans les références .NET par défaut. par conséquent, recherchez Microsoft.Ink.dll dans votre dossier Windows.</span><span class="sxs-lookup"><span data-stu-id="64a96-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="64a96-197">Une fois que vous avez localisé la DLL, ajoutez l’assembly aux références du projet : sélectionnez l’onglet **Parcourir** , accédez au dossier contenant Microsoft.Ink.dll, sélectionnez Microsoft.Ink.dll, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a96-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="64a96-198">L’illustration suivante montre la solution du projet dans l’Explorateur Windows avec tous les assemblys de référence ajoutés.</span><span class="sxs-lookup"><span data-stu-id="64a96-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="64a96-199">![projet InkRecognition dans l’Explorateur Windows avec tous les assemblys de référence ajoutés](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="64a96-200">*projet InkRecognition dans l’Explorateur Windows avec tous les assemblys de référence ajoutés*</span><span class="sxs-lookup"><span data-stu-id="64a96-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="64a96-201">Créer un service WCF Silverlight pour la reconnaissance de l’encre</span><span class="sxs-lookup"><span data-stu-id="64a96-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="64a96-202">Ensuite, vous allez ajouter un service WCF pour la reconnaissance de l’encre au projet.</span><span class="sxs-lookup"><span data-stu-id="64a96-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="64a96-203">Cliquez avec le bouton droit sur votre projet InkRecognition. Web, cliquez sur **Ajouter**, puis sur **nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="64a96-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="64a96-204">Sélectionnez le modèle de service WCF Silverlight, remplacez le nom par InkRecogitionService, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="64a96-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="64a96-205">L’illustration suivante montre la boîte de dialogue **Ajouter un nouvel élément** avec le service WCF Silverlight sélectionné et nommé.</span><span class="sxs-lookup"><span data-stu-id="64a96-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="64a96-206">![Boîte de dialogue Ajouter un nouvel élément avec service WCF Silverlight sélectionné et nommé](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="64a96-207&quot;>*Boîte de dialogue Ajouter un nouvel élément avec service WCF Silverlight sélectionné et nommé*</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;64a96-207&quot;>*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id=&quot;64a96-208&quot;>Une fois que vous avez ajouté le service WCF Silverlight, le code de service derrière, InkRecognitionService. cs, s’ouvre.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;64a96-208&quot;>After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id=&quot;64a96-209&quot;>Remplacez le code du service par le code suivant.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;64a96-209&quot;>Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="64a96-210">Ajouter la référence de service à votre projet client</span><span class="sxs-lookup"><span data-stu-id="64a96-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="64a96-211">Maintenant que vous disposez de votre service WCF Silverlight pour InkRecognition, vous utiliserez le service à partir de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="64a96-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="64a96-212">Cliquez avec le bouton droit sur le projet InkRecognition, puis sélectionnez **Ajouter une référence de service**.</span><span class="sxs-lookup"><span data-stu-id="64a96-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="64a96-213">Dans la boîte de dialogue **Ajouter une référence de service** qui s’affiche, sélectionnez **découvrir** pour découvrir les services de la solution actuelle.</span><span class="sxs-lookup"><span data-stu-id="64a96-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="64a96-214">InkRecognitionService s’affiche dans le volet services.</span><span class="sxs-lookup"><span data-stu-id="64a96-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="64a96-215">Double-cliquez sur InkRecognitionService dans le volet services, remplacez l’espace de noms par InkRecognitionServiceReference, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="64a96-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="64a96-216">L’illustration suivante montre la boîte de dialogue **Ajouter une référence de service** avec l’option InkRecognitionService sélectionnée et l’espace de noms modifié.</span><span class="sxs-lookup"><span data-stu-id="64a96-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="64a96-217">![Boîte de dialogue Ajouter une référence de service avec inkrecognitionservice sélectionné et espace de noms modifié](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="64a96-218">*Boîte de dialogue Ajouter une référence de service avec inkrecognitionservice sélectionné et espace de noms modifié*</span><span class="sxs-lookup"><span data-stu-id="64a96-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="64a96-219">Ajouter la classe InkCollector au projet InkRecognition</span><span class="sxs-lookup"><span data-stu-id="64a96-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="64a96-220">Cliquez avec le bouton droit sur le projet InkRecognition, cliquez sur **Ajouter**, puis sur **nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="64a96-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="64a96-221">Dans le menu **Visual \# c** , sélectionnez **c \# classe**.</span><span class="sxs-lookup"><span data-stu-id="64a96-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="64a96-222">Nommez la classe InkCollector.</span><span class="sxs-lookup"><span data-stu-id="64a96-222">Name the class InkCollector.</span></span> <span data-ttu-id="64a96-223">L’illustration suivante montre la boîte de dialogue avec la \# classe C sélectionnée et nommée.</span><span class="sxs-lookup"><span data-stu-id="64a96-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="64a96-224">![Boîte de dialogue Ajouter un nouvel élément avec la \# classe c sélectionnée et nommée](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="64a96-225">*Boîte de dialogue Ajouter un nouvel élément avec la \# classe c sélectionnée et nommée*</span><span class="sxs-lookup"><span data-stu-id="64a96-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="64a96-226">Une fois que vous avez ajouté la classe InkCollector, la définition de classe s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="64a96-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="64a96-227">Remplacez le code dans le collecteur d’encre par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="64a96-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="64a96-228">Mettre à jour le XAML pour la page par défaut et ajouter un code-behind pour la reconnaissance de l’écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="64a96-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="64a96-229">Maintenant que vous avez une classe qui collecte de l’encre, vous devez mettre à jour le XAML dans page. XAML avec le code XAML suivant.</span><span class="sxs-lookup"><span data-stu-id="64a96-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="64a96-230">Le code suivant ajoute un dégradé jaune à la zone d’entrée, un contrôle InkCanvas et un bouton qui déclenche la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="64a96-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="64a96-231">Remplacez la page code-behind, page. Xaml. cs, par le code suivant, qui ajoute un gestionnaire d’événements pour le bouton **Recognize** .</span><span class="sxs-lookup"><span data-stu-id="64a96-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="64a96-232">Supprimer les directives de transport sécurisées de la configuration du client</span><span class="sxs-lookup"><span data-stu-id="64a96-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="64a96-233">Avant de pouvoir utiliser le service WCF, vous devez supprimer toutes les options de transport sécurisées de la configuration du service, car les transports sécurisés ne sont actuellement pas pris en charge dans les services WCF 2,0 de Silverlight.</span><span class="sxs-lookup"><span data-stu-id="64a96-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="64a96-234">À partir du projet InkRecognition, mettez à jour les paramètres de sécurité dans ServiceReferences. ClientConfig.</span><span class="sxs-lookup"><span data-stu-id="64a96-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="64a96-235">Modifier le code XML de sécurité</span><span class="sxs-lookup"><span data-stu-id="64a96-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="64a96-236">to</span><span class="sxs-lookup"><span data-stu-id="64a96-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="64a96-237">À présent, votre application doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="64a96-237">Now, your application should run.</span></span> <span data-ttu-id="64a96-238">L’illustration suivante montre comment l’application recherche dans awebpagewith une écriture manuscrite entrée dans la zone reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="64a96-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="64a96-239">![Application dans awebpagewith une entrée manuscrite entrée dans la zone de reconnaissance](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="64a96-240">*Application dans awebpagewith une entrée manuscrite entrée dans la zone de reconnaissance*</span><span class="sxs-lookup"><span data-stu-id="64a96-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="64a96-241">L’illustration suivante montre le texte reconnu dans la liste déroulante de **résultats** .</span><span class="sxs-lookup"><span data-stu-id="64a96-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="64a96-242">![Application dans awebpagewith texte reconnu dans la liste déroulante des résultats](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="64a96-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="64a96-243">*Application dans awebpagewith texte reconnu dans la liste déroulante des résultats*</span><span class="sxs-lookup"><span data-stu-id="64a96-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



