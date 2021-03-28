---
description: Montre comment personnaliser le fichier dans la boîte de dialogue d’utilisation de pour afficher des informations et des options supplémentaires pour les fichiers qui sont actuellement ouverts dans l’application.
title: Fichier en cours d’utilisation, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319346"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="c0c3c-103">Fichier en cours d’utilisation, exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-103">File Is In Use Sample</span></span>

<span data-ttu-id="c0c3c-104">Montre comment personnaliser le **fichier dans** la boîte de dialogue d’utilisation de pour afficher des informations et des options supplémentaires pour les fichiers qui sont actuellement ouverts dans l’application.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="c0c3c-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c0c3c-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0c3c-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c0c3c-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c0c3c-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c0c3c-109">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="c0c3c-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c0c3c-110">Requirements</span></span>



| <span data-ttu-id="c0c3c-111">Produit</span><span class="sxs-lookup"><span data-stu-id="c0c3c-111">Product</span></span>                                | <span data-ttu-id="c0c3c-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="c0c3c-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c0c3c-113">Windows</span><span class="sxs-lookup"><span data-stu-id="c0c3c-113">Windows</span></span>                                | <span data-ttu-id="c0c3c-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c3c-114">Windows Vista</span></span>           |
| <span data-ttu-id="c0c3c-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="c0c3c-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c0c3c-116">6.1</span><span class="sxs-lookup"><span data-stu-id="c0c3c-116">6.1</span></span>                     |



 

<span data-ttu-id="c0c3c-117">Pour obtenir des spécifications supplémentaires, consultez le \_ fichier IFileIsInUsesample.docx inclus avec l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c0c3c-118">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-118">Downloading the Sample</span></span>

| <span data-ttu-id="c0c3c-119">Emplacement</span><span class="sxs-lookup"><span data-stu-id="c0c3c-119">Location</span></span>      | <span data-ttu-id="c0c3c-120">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="c0c3c-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c3c-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="c0c3c-121">GitHub</span></span>  | [<span data-ttu-id="c0c3c-122">Exemple FileIsInUse</span><span class="sxs-lookup"><span data-stu-id="c0c3c-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="c0c3c-123">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-123">Building the Sample</span></span>

<span data-ttu-id="c0c3c-124">Pour générer l’exemple à partir de la fenêtre d’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="c0c3c-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="c0c3c-125">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **FileIsInUse** .</span><span class="sxs-lookup"><span data-stu-id="c0c3c-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="c0c3c-126">Entrez `msbuild FileIsInUse.sln`.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="c0c3c-127">Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :</span><span class="sxs-lookup"><span data-stu-id="c0c3c-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c0c3c-128">Ouvrez l’Explorateur Windows et accédez au répertoire du projet **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="c0c3c-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="c0c3c-129">Par exemple, le chemin d’installation complet par défaut est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .</span><span class="sxs-lookup"><span data-stu-id="c0c3c-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="c0c3c-130">Double-cliquez sur l’icône du fichier FileIsInUseSample. sln pour ouvrir le projet dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="c0c3c-131">L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c0c3c-132">Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».</span><span class="sxs-lookup"><span data-stu-id="c0c3c-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="c0c3c-133">Dans le menu **générer** , sélectionnez **générer la solution**.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c0c3c-134">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="c0c3c-134">Running the Sample</span></span>

1.  <span data-ttu-id="c0c3c-135">Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="c0c3c-136">À l’invite de commandes, entrez `FileIsInUseSample.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de FileIsInUseSample.exe.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="c0c3c-137">Pour plus d’informations sur cet exemple de code, consultez le \_ fichier IFileIsInUsesample.docx inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c0c3c-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 



