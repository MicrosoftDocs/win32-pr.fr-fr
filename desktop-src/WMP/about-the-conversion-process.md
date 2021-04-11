---
title: À propos du processus de conversion
description: À propos du processus de conversion
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player, processus de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030821"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="29c53-107">À propos du processus de conversion</span><span class="sxs-lookup"><span data-stu-id="29c53-107">About the Conversion Process</span></span>

<span data-ttu-id="29c53-108">Une fois que le lecteur Windows Media a instancié le plug-in de conversion, le processus se déroule comme suit :</span><span class="sxs-lookup"><span data-stu-id="29c53-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="29c53-109">Le lecteur appelle [IWMPConvert :: convertfile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span><span class="sxs-lookup"><span data-stu-id="29c53-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="29c53-110">Le plug-in convertit le fichier fourni dans le paramètre *bstrInputFile* au format ASF.</span><span class="sxs-lookup"><span data-stu-id="29c53-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="29c53-111">Si la conversion échoue pour une raison quelconque, le plug-in retourne un code d’erreur approprié et le processus s’arrête.</span><span class="sxs-lookup"><span data-stu-id="29c53-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="29c53-112">Si la conversion réussit, le plug-in place le fichier converti dans le dossier fourni dans le paramètre *bstrDestinationFolder* et retourne le chemin d’accès complet au fichier converti via le paramètre *pbstrOutputFile* .</span><span class="sxs-lookup"><span data-stu-id="29c53-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="29c53-113">Le plug-in retourne un code de réussite de **convertfile**.</span><span class="sxs-lookup"><span data-stu-id="29c53-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="29c53-114">Le lecteur copie le fichier converti dans un dossier dans la hiérarchie des dossiers musicaux de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29c53-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="29c53-115">L’emplacement exact où le lecteur copie le fichier dépend du contenu.</span><span class="sxs-lookup"><span data-stu-id="29c53-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="29c53-116">Dans le cadre de ce processus, le lecteur peut renommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="29c53-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="29c53-117">Le lecteur copie le fichier d’origine (non converti) dans un dossier de la hiérarchie des dossiers musicaux de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29c53-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="29c53-118">Dans le cadre de ce processus, le lecteur peut renommer le fichier.</span><span class="sxs-lookup"><span data-stu-id="29c53-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="29c53-119">Il s’agit de la copie du fichier que le lecteur utilise lorsque l’utilisateur synchronise le contenu de l’ordinateur sur un appareil qui requiert le format de fichier d’origine.</span><span class="sxs-lookup"><span data-stu-id="29c53-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="29c53-120">Ce fichier s’appelle un *fichier caché*.</span><span class="sxs-lookup"><span data-stu-id="29c53-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="29c53-121">Le lecteur ajoute à la bibliothèque des informations sur le fichier converti.</span><span class="sxs-lookup"><span data-stu-id="29c53-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="29c53-122">Cela comprend la définition de la valeur de l’attribut **ShadowFilePath** sur le nouvel emplacement d’enregistrement du fichier caché.</span><span class="sxs-lookup"><span data-stu-id="29c53-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="29c53-123">Si vous devez utiliser le fichier converti, vous pouvez interroger la bibliothèque pour récupérer le contenu à l’aide des attributs **ContentDistributor** et **WM/UniqueFileIdentifier** .</span><span class="sxs-lookup"><span data-stu-id="29c53-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="29c53-124">Si vous devez utiliser le fichier caché, vous devez tout de même récupérer l’objet **multimédia** du fichier converti, puis interroger l’attribut **ShadowFilePath** .</span><span class="sxs-lookup"><span data-stu-id="29c53-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="29c53-125">Consultez [Ajout de métadonnées aux fichiers convertis](adding-metadata-to-converted-files.md).</span><span class="sxs-lookup"><span data-stu-id="29c53-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29c53-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29c53-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29c53-127">**À propos des plug-ins de conversion**</span><span class="sxs-lookup"><span data-stu-id="29c53-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="29c53-128">**Ajout de métadonnées aux fichiers convertis**</span><span class="sxs-lookup"><span data-stu-id="29c53-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="29c53-129">**Lecture des valeurs d’attribut**</span><span class="sxs-lookup"><span data-stu-id="29c53-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="29c53-130">**Attribut ShadowFilePath**</span><span class="sxs-lookup"><span data-stu-id="29c53-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="29c53-131">**Attribut WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="29c53-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="29c53-132">**Attribut WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="29c53-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




