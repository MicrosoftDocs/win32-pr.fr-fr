---
title: Chiffrement et importation d’exemples de médias
description: Chiffrement et importation d’exemples de médias
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, chiffrement des exemples de supports
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), chiffrement des exemples de supports
- DRM (gestion des droits numériques), chiffrement des exemples de supports
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, chiffrement des exemples de médias
- API étendues du client, chiffrement des exemples de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381498"
---
# <a name="encrypting-and-importing-media-samples"></a><span data-ttu-id="fefb9-114">Chiffrement et importation d’exemples de médias</span><span class="sxs-lookup"><span data-stu-id="fefb9-114">Encrypting and Importing Media Samples</span></span>

<span data-ttu-id="fefb9-115">Pour chaque échantillon multimédia que vous chiffrez à l’aide de Windows Media DRM, vous devez générer une valeur Salt qui est strictement supérieure à la précédente (ce qui augmente de façon monotone).</span><span class="sxs-lookup"><span data-stu-id="fefb9-115">For each media sample that you encrypt using Windows Media DRM, you must generate a salt value that is strictly bigger than the previous one (monotonically increasing).</span></span> <span data-ttu-id="fefb9-116">Utilisez la nouvelle valeur salt pour créer une clé de chiffrement transitoire en appliquant l’algorithme de chiffrement SHA-1 au vecteur d’initialisation concaténé avec la valeur salt.</span><span class="sxs-lookup"><span data-stu-id="fefb9-116">Use the new salt value to create a transitory encryption key by applying the SHA-1 encryption algorithm to the initialization vector concatenated with the salt value.</span></span>

<span data-ttu-id="fefb9-117">Ensuite, chiffrez l’exemple en fonction de l’algorithme RC4 à l’aide de la clé transitoire générée.</span><span class="sxs-lookup"><span data-stu-id="fefb9-117">Next, encrypt the sample according to the RC4 algorithm using the generated transitory key.</span></span> <span data-ttu-id="fefb9-118">Avant que l’exemple ne soit passé au kit de développement logiciel (SDK), votre application doit associer la valeur Salt à l’exemple en définissant un attribut d’extension.</span><span class="sxs-lookup"><span data-stu-id="fefb9-118">Before the sample is passed to the SDK, your application must associate the salt value with the sample by setting an extension attribute.</span></span>

<span data-ttu-id="fefb9-119">Voici les étapes de chiffrement des exemples de média :</span><span class="sxs-lookup"><span data-stu-id="fefb9-119">Here are the steps for encrypting media samples:</span></span>

1.  <span data-ttu-id="fefb9-120">Appelez la méthode **QueryInterface** de l’exemple d’objet pour accéder à l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="fefb9-120">Call the **QueryInterface** method of the sample object to get the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface.</span></span>
2.  <span data-ttu-id="fefb9-121">Incrémentez la valeur salt.</span><span class="sxs-lookup"><span data-stu-id="fefb9-121">Increment the salt value.</span></span>
3.  <span data-ttu-id="fefb9-122">Chiffrez l’exemple à l’aide d’un algorithme de chiffrement RC1.</span><span class="sxs-lookup"><span data-stu-id="fefb9-122">Encrypt the sample using an RC1 encryption algorithm.</span></span> <span data-ttu-id="fefb9-123">Pour le chiffrement, vous créez une clé en concaténant le vecteur d’initialisation et la valeur salt.</span><span class="sxs-lookup"><span data-stu-id="fefb9-123">For the encryption you create a key by concatenating the initialization vector and the salt value.</span></span>
4.  <span data-ttu-id="fefb9-124">Fournissez la valeur Salt au kit de développement logiciel (SDK) en appelant [**INSSBuffer :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="fefb9-124">Provide the salt value to the SDK by calling [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fefb9-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fefb9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fefb9-126">**Importation DRM**</span><span class="sxs-lookup"><span data-stu-id="fefb9-126">**DRM Import**</span></span>](drm-import.md)
</dt> <dt>

[<span data-ttu-id="fefb9-127">**Exemple de chiffrement d’échantillon de média**</span><span class="sxs-lookup"><span data-stu-id="fefb9-127">**Media Sample Encryption Example**</span></span>](media-sample-encryption-example.md)
</dt> </dl>

 

 




