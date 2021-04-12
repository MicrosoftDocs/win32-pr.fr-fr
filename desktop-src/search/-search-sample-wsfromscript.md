---
description: L’exemple de code WSFromScript montre comment interroger la recherche Windows à partir d’un script Microsoft Visual Basic à l’aide de Microsoft ActiveX Data Objects (ADO).
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: WSFromScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318165"
---
# <a name="wsfromscript"></a><span data-ttu-id="678c2-103">WSFromScript</span><span class="sxs-lookup"><span data-stu-id="678c2-103">WSFromScript</span></span>

<span data-ttu-id="678c2-104">L’exemple de code WSFromScript montre comment interroger la recherche Windows à partir d’un script Microsoft Visual Basic à l’aide de Microsoft ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="678c2-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="678c2-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="678c2-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="678c2-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="678c2-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="678c2-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="678c2-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="678c2-108">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="678c2-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="678c2-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="678c2-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="678c2-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="678c2-110">Requirements</span></span>

| <span data-ttu-id="678c2-111">Produit</span><span class="sxs-lookup"><span data-stu-id="678c2-111">Product</span></span>     | <span data-ttu-id="678c2-112">Version du produit</span><span class="sxs-lookup"><span data-stu-id="678c2-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="678c2-113">Windows</span><span class="sxs-lookup"><span data-stu-id="678c2-113">Windows</span></span>     | <span data-ttu-id="678c2-114">Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="678c2-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="678c2-115">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="678c2-115">Windows SDK</span></span> | <span data-ttu-id="678c2-116">7,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="678c2-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="678c2-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="678c2-117">Downloading the Sample</span></span>

<span data-ttu-id="678c2-118">Cet exemple est disponible à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="678c2-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="678c2-119">Emplacement</span><span class="sxs-lookup"><span data-stu-id="678c2-119">Location</span></span>      | <span data-ttu-id="678c2-120">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="678c2-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="678c2-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="678c2-121">GitHub</span></span>  | [<span data-ttu-id="678c2-122">Exemple WSFromScript</span><span class="sxs-lookup"><span data-stu-id="678c2-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="678c2-123">Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="678c2-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="678c2-124">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="678c2-124">Building the Sample</span></span>

<span data-ttu-id="678c2-125">Pour générer l’exemple à partir de la fenêtre d’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="678c2-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="678c2-126">Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **QueryEverything** .</span><span class="sxs-lookup"><span data-stu-id="678c2-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="678c2-127">Par exemple, le chemin d’installation complet par défaut du kit de développement logiciel (SDK) Windows 7 est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` .</span><span class="sxs-lookup"><span data-stu-id="678c2-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="678c2-128">Entrez `cscript QueryEverything.vbs`.</span><span class="sxs-lookup"><span data-stu-id="678c2-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="678c2-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="678c2-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="678c2-130">Conceptuel</span><span class="sxs-lookup"><span data-stu-id="678c2-130">Conceptual</span></span>

<span data-ttu-id="678c2-131">[**Informations de référence sur le langage VBScript**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="678c2-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="678c2-132">Autres exemples</span><span class="sxs-lookup"><span data-stu-id="678c2-132">Other Samples</span></span>

[<span data-ttu-id="678c2-133">Rechercher des exemples de code</span><span class="sxs-lookup"><span data-stu-id="678c2-133">Search Code Samples</span></span>](-search-samples-ovw.md)
