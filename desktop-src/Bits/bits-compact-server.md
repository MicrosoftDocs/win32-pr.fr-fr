---
title: BITS Compact Server
description: Le serveur compact Server Service de transfert intelligent en arrière-plan (BITS) est un serveur de fichiers HTTP/HTTPs autonome qui permet de transférer de façon asynchrone un nombre limité de fichiers volumineux entre les ordinateurs.
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842525"
---
# <a name="bits-compact-server"></a><span data-ttu-id="89db5-103">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="89db5-103">BITS Compact Server</span></span>

<span data-ttu-id="89db5-104">Le serveur compact Server Service de transfert intelligent en arrière-plan (BITS) est un serveur de fichiers HTTP/HTTPs autonome qui permet de transférer de façon asynchrone un nombre limité de fichiers volumineux entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="89db5-104">The Background Intelligent Transfer Service (BITS) Compact Server is a stand-alone HTTP/HTTPS file server that provides the ability to transfer a limited number of large files asynchronously between computers.</span></span> <span data-ttu-id="89db5-105">Le serveur compact est construit en tant que service NT et utilise HTTP.SYS.</span><span class="sxs-lookup"><span data-stu-id="89db5-105">The Compact Server is built as an NT Service and uses HTTP.SYS.</span></span>

<span data-ttu-id="89db5-106">Le serveur BITS Compact Server est destiné aux entreprises et aux petites entreprises dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="89db5-106">The BITS Compact Server is intended for use by enterprise and small business customers under the following conditions:</span></span>

-   <span data-ttu-id="89db5-107">L’utilisation anticipée est un maximum de 25 groupes d’URL, et chaque groupe d’URL prend en charge 3 transferts de fichiers simultanés.</span><span class="sxs-lookup"><span data-stu-id="89db5-107">The anticipated usage is a maximum of 25 URL groups, and each URL group supports 3 simultaneous file transfers.</span></span>
-   <span data-ttu-id="89db5-108">Les transferts de fichiers se produisent entre des ordinateurs dans le même domaine ou des domaines approuvés mutuellement.</span><span class="sxs-lookup"><span data-stu-id="89db5-108">File transfers occur between computers in the same domain or mutually trusted domains.</span></span>
-   <span data-ttu-id="89db5-109">Les transferts de fichiers ne sont pas destinés aux clients accessibles sur Internet.</span><span class="sxs-lookup"><span data-stu-id="89db5-109">File transfers are not intended for Internet-facing clients.</span></span>

## <a name="installing-the-bits-compact-server"></a><span data-ttu-id="89db5-110">Installation de BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="89db5-110">Installing the BITS Compact Server</span></span>

<span data-ttu-id="89db5-111">BITS Compact Server est un composant serveur facultatif.</span><span class="sxs-lookup"><span data-stu-id="89db5-111">The BITS Compact Server is an optional server component.</span></span> <span data-ttu-id="89db5-112">Vous pouvez utiliser l’une des options suivantes pour installer BITS Compact Server :</span><span class="sxs-lookup"><span data-stu-id="89db5-112">You can use one of the following options to install the BITS Compact Server:</span></span>

-   <span data-ttu-id="89db5-113">Gestionnaire de serveur</span><span class="sxs-lookup"><span data-stu-id="89db5-113">Server Manager</span></span>

-   <span data-ttu-id="89db5-114">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="89db5-114">Windows PowerShell</span></span>

-   <span data-ttu-id="89db5-115">Gestionnaire de package</span><span class="sxs-lookup"><span data-stu-id="89db5-115">Package Manager</span></span>

<span data-ttu-id="89db5-116">**Pour installer BITS Compact Server à l’aide de Gestionnaire de serveur**</span><span class="sxs-lookup"><span data-stu-id="89db5-116">**To install the BITS Compact Server by using Server Manager**</span></span>

1.  <span data-ttu-id="89db5-117">Dans la section **Résumé des fonctionnalités** de la **Gestionnaire de serveur**, cliquez sur Ajouter des **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="89db5-117">In the **Features Summary** section of the **Server Manager**, click **Add Features**.</span></span>
2.  <span data-ttu-id="89db5-118">Dans l’Assistant Ajout de fonctionnalités, sélectionnez **service de transfert intelligent en arrière-plan (bits)** et **Compact Server**.</span><span class="sxs-lookup"><span data-stu-id="89db5-118">In the Add Features Wizard, select **Background Intelligent Transfer Service (BITS)** and **Compact Server**.</span></span>
3.  <span data-ttu-id="89db5-119">Suivez les instructions de l’Assistant, y compris l’installation des logiciels requis, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="89db5-119">Follow the wizard instructions, including installing the required software if indicated.</span></span>

<span data-ttu-id="89db5-120">Pour plus d’informations, consultez l’aide en ligne de **Gestionnaire de serveur** .</span><span class="sxs-lookup"><span data-stu-id="89db5-120">For more information, see the **Server Manager** online help.</span></span>

<span data-ttu-id="89db5-121">**Pour installer BITS Compact Server à l’aide de Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="89db5-121">**To install the BITS Compact Server by using Windows PowerShell**</span></span>

1.  <span data-ttu-id="89db5-122">Dans une invite de commandes Windows PowerShell, tapez la commande suivante : **import-module ServerManager**.</span><span class="sxs-lookup"><span data-stu-id="89db5-122">In a Windows PowerShell command prompt, type the following command: **Import-Module ServerManager**.</span></span> <span data-ttu-id="89db5-123">Appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="89db5-123">Then press Enter.</span></span>
2.  <span data-ttu-id="89db5-124">Tapez la commande suivante : **Add-WINDOWSFEATURE bits-Compact-Server**.</span><span class="sxs-lookup"><span data-stu-id="89db5-124">Type the following command: **Add-WindowsFeature BITS-Compact-Server**.</span></span> <span data-ttu-id="89db5-125">Appuyez sur Entrée.</span><span class="sxs-lookup"><span data-stu-id="89db5-125">Then press Enter.</span></span>

<span data-ttu-id="89db5-126">L’exemple de texte suivant illustre l’installation de BITS Compact Server à l’aide des applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="89db5-126">The following text-based example demonstrates installing the BITS Compact Server using Windows PowerShell cmdlets.</span></span>

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

<span data-ttu-id="89db5-127">Pour plus d’informations sur l’utilisation des applets de commande, consultez la documentation de [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="89db5-127">For information about using cmdlets, see the [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) documentation.</span></span>

<span data-ttu-id="89db5-128">Pour plus d’informations sur l’applet de commande Import-Module, consultez [import-module](/previous-versions//dd347701(v=technet.10)) dans la bibliothèque Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="89db5-128">For more information about the Import-Module cmdlet, see [Import-Module](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="89db5-129">Pour obtenir de l’aide à partir de la ligne de commande, tapez **« obtenir-aide import-module »**.</span><span class="sxs-lookup"><span data-stu-id="89db5-129">For help at the command line, type **get-help import-module**.</span></span>

<span data-ttu-id="89db5-130">Pour plus d’informations sur l’applet de commande Add-WindowsFeature, consultez [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) dans la bibliothèque Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="89db5-130">For more information about the Add-WindowsFeature cmdlet, see [Add-WindowsFeature](/previous-versions//dd347701(v=technet.10)) in the Microsoft TechNet Library.</span></span> <span data-ttu-id="89db5-131">Pour obtenir de l’aide sur la ligne de commande, tapez **« obtenir-help Add-WindowsFeature »**.</span><span class="sxs-lookup"><span data-stu-id="89db5-131">For help at the command line, type **get-help Add-WindowsFeature**.</span></span>

<span data-ttu-id="89db5-132">**Pour installer BITS Compact Server à l’aide du gestionnaire de package**</span><span class="sxs-lookup"><span data-stu-id="89db5-132">**To install the BITS Compact Server by using Package Manager**</span></span>

-   <span data-ttu-id="89db5-133">Entrez la commande suivante : **PkgMgr.exe/IU : LightweightServer**.</span><span class="sxs-lookup"><span data-stu-id="89db5-133">Enter the following command: **PkgMgr.exe /iu:LightweightServer**.</span></span>

> [!Note]  
> <span data-ttu-id="89db5-134">Les paramètres sont perdus si le service Compact Server est redémarré ou si l’ordinateur est redémarré.</span><span class="sxs-lookup"><span data-stu-id="89db5-134">The settings are lost if the Compact Server service is restarted or if the computer is rebooted.</span></span>

 

## <a name="bits-compact-server-remote-management"></a><span data-ttu-id="89db5-135">Gestion à distance de BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="89db5-135">BITS Compact Server Remote Management</span></span>

<span data-ttu-id="89db5-136">Le serveur BITS Compact avec la gestion à distance BITS permet des transferts de fichiers à distance plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="89db5-136">The BITS Compact Server with BITS Remote Management enables more secure remote file transfers.</span></span> <span data-ttu-id="89db5-137">La gestion à distance BITS utilise un fournisseur de Windows Management Instrumentation (WMI) pour permettre à un administrateur système ou à une application de contrôleur de créer à distance des tâches de transfert BITS sur les clients et de publier des fichiers pour l’hébergement sur le serveur BITS Compact Server.</span><span class="sxs-lookup"><span data-stu-id="89db5-137">BITS Remote Management uses a Windows Management Instrumentation (WMI) provider to let a system administrator or a controller application remotely create BITS transfer jobs on the clients and to publish files for hosting on the BITS Compact Server.</span></span> <span data-ttu-id="89db5-138">Le fournisseur BITS peut également être utilisé pour permettre à une application d’utiliser à distance le client BITS conjointement avec le serveur BITS Compact Server pour transférer des fichiers d’un ordinateur distant à un autre ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="89db5-138">The BITS provider can also be used to enable an application to remotely use the BITS client in conjunction with the BITS Compact Server to transfer files from one remote computer to another remote computer.</span></span>

<span data-ttu-id="89db5-139">Pour plus d’informations, consultez la documentation du [fournisseur bits](/previous-versions/windows/desktop/bitsprov/bits-provider) .</span><span class="sxs-lookup"><span data-stu-id="89db5-139">For more information, see the [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89db5-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89db5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89db5-141">Fournisseur BITS</span><span class="sxs-lookup"><span data-stu-id="89db5-141">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 