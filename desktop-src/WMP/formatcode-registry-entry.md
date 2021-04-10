---
title: Entrée de Registre FormatCode
description: Entrée de Registre FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Lecteur Windows Media, entrées de Registre FormatCode
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées FormatCode
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- Entrées de Registre FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104198750"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="5dde0-111">Entrée de Registre FormatCode</span><span class="sxs-lookup"><span data-stu-id="5dde0-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="5dde0-112">Lorsque le lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension.</span><span class="sxs-lookup"><span data-stu-id="5dde0-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="5dde0-113">La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5dde0-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="5dde0-114">L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée **FormatCode** .</span><span class="sxs-lookup"><span data-stu-id="5dde0-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="5dde0-115">L’entrée de Registre **FormatCode** spécifie le code de format MTP (Media Transport Protocol) pour les fichiers qui ont l’extension personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5dde0-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="5dde0-116">L’entrée de Registre **FormatCode** se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="5dde0-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="5dde0-117">Nom</span><span class="sxs-lookup"><span data-stu-id="5dde0-117">Name</span></span>       | <span data-ttu-id="5dde0-118">Type</span><span class="sxs-lookup"><span data-stu-id="5dde0-118">Type</span></span>           | <span data-ttu-id="5dde0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dde0-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="5dde0-120">FormatCode</span><span class="sxs-lookup"><span data-stu-id="5dde0-120">FormatCode</span></span> | <span data-ttu-id="5dde0-121">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="5dde0-121">**REG\_DWORD**</span></span> | <span data-ttu-id="5dde0-122">Entier positif 16 bits qui identifie le format du fichier.</span><span class="sxs-lookup"><span data-stu-id="5dde0-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="5dde0-123">Lorsque l’utilisateur tente de copier un fichier multimédia numérique ayant une extension de nom de fichier personnalisée sur un appareil mobile, le lecteur Windows Media recherche un code de format associé à l’extension de nom de fichier personnalisée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5dde0-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="5dde0-124">Si le lecteur Windows Media trouve un code de format, il utilise MTP pour déterminer si l’appareil prend en charge le format de fichier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5dde0-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="5dde0-125">Si l’appareil prend en charge le format, le fichier multimédia est copié sur l’appareil sans être transcodé.</span><span class="sxs-lookup"><span data-stu-id="5dde0-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="5dde0-126">Un appareil qui prend en charge MTP peut fournir le lecteur Windows Media avec un jeu de données DeviceInfo, qui contient, entre autres choses, une liste de codes de format pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5dde0-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="5dde0-127">Si vous êtes en train de développer un format de fichier personnalisé, vous pouvez demander un code de format auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dde0-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="5dde0-128">Pour plus d’informations sur la demande d’un code de format, consultez le kit de portage de protocole Microsoft Media transport, disponible dans le [Centre de développement Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="5dde0-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dde0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5dde0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dde0-130">**Paramètres de registre de l’extension de nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="5dde0-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




