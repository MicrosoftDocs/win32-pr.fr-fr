---
description: Montre comment utiliser les interfaces VSS pour créer un fournisseur de matériel VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Outil et exemple VssSampleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517502"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="0ba2d-103">Outil et exemple VssSampleProvider</span><span class="sxs-lookup"><span data-stu-id="0ba2d-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="0ba2d-104">Montre comment utiliser les [interfaces](volume-shadow-copy-api-interfaces.md) VSS pour créer un fournisseur de matériel VSS.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="0ba2d-105">L’outil et l’exemple VssSampleProvider sont inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ba2d-106">Vous pouvez télécharger le SDK Windows à partir du [Kit de développement logiciel (SDK) Windows pour Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span><span class="sxs-lookup"><span data-stu-id="0ba2d-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="0ba2d-107">Dans l’installation SDK Windows, l’outil VssSampleProvider se trouve dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour windows 64 bits) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (pour Windows 32 bits).</span><span class="sxs-lookup"><span data-stu-id="0ba2d-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="0ba2d-108">Les fournisseurs de matériel sont uniquement pris en charge sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="0ba2d-109">Sur un système d’exploitation client Windows, vous pouvez compiler l’exemple VssSampleProvider, mais vous ne pouvez pas l’inscrire en tant que fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="0ba2d-110">L’outil VssSampleProvider se compose des fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="0ba2d-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="0ba2d-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="0ba2d-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="0ba2d-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="0ba2d-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="0ba2d-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="0ba2d-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="0ba2d-114">Vstorinterface.dll</span></span>

<span data-ttu-id="0ba2d-115">L’exemple VssSampleProvider comprend les scripts d’installation et de désinstallation suivants :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="0ba2d-116">Install-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="0ba2d-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="0ba2d-117">Uninstall-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="0ba2d-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="0ba2d-118">Inscrire \_app.vbs</span><span class="sxs-lookup"><span data-stu-id="0ba2d-118">Register\_app.vbs</span></span>

<span data-ttu-id="0ba2d-119">**Pour installer et utiliser l’exemple VssSampleProvider**</span><span class="sxs-lookup"><span data-stu-id="0ba2d-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="0ba2d-120">Accédez au répertoire `Program Files (x86)\Windows Kits\8.0\bin\`.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="0ba2d-121">Ce répertoire contient virtualstoragevss.sys et vstorcontrol.exe.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="0ba2d-122">Ouvrez une fenêtre d’invite de commandes dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="0ba2d-123">Pour installer le pilote de stockage virtuel, dans la fenêtre d’invite de commandes, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="0ba2d-124">Pour installer l’exemple de fournisseur VSS, dans la fenêtre d’invite de commandes, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="0ba2d-125">Pour créer un numéro d’unité logique virtuelle, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="0ba2d-126">Dans la fenêtre d’invite de commandes, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="0ba2d-127">Cette commande crée un LUN virtuel dont l’identificateur de stockage est le **fournisseur d’exemples de matériel VSS**.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="0ba2d-128">Pour créer des numéros d’unités logiques virtuels supplémentaires, répétez cette étape.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="0ba2d-129">L’exemple de fournisseur VSS reconnaît un numéro d’unité logique uniquement si le **fournisseur de matériel exemple VSS** fait partie de l’identificateur de stockage.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="0ba2d-130">Pour plus d’informations sur l’identificateur de stockage, consultez le billet de blog suivant.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="0ba2d-131">LUN-resynchronisation avec DiskShadow et le stockage virtuel</span><span class="sxs-lookup"><span data-stu-id="0ba2d-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="0ba2d-132">Dans la fenêtre d’invite de commandes, utilisez diskpart.exe pour formater le disque virtuel et lui attribuer une lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="0ba2d-133">Voici un exemple de script à exécuter à l’invite de commandes Diskpart.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="0ba2d-134">Pour exécuter l’exemple de fournisseur, dans la fenêtre d’invite de commandes, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="0ba2d-135">*<drive>* représente la lettre de lecteur du numéro d’unité logique virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0ba2d-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="0ba2d-136">Pour désinstaller l’exemple de fournisseur VSS, dans la fenêtre d’invite de commandes, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="0ba2d-137">Pour désinstaller le pilote de stockage virtuel, dans la fenêtre d’invite de commandes, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0ba2d-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



