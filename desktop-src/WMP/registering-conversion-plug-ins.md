---
title: Inscription des plug-ins de conversion
description: Inscription des plug-ins de conversion
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Lecteur Windows Media, plug-ins de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, inscription
- Registre, plug-ins de conversion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513459"
---
# <a name="registering-conversion-plug-ins"></a><span data-ttu-id="3c755-108">Inscription des plug-ins de conversion</span><span class="sxs-lookup"><span data-stu-id="3c755-108">Registering Conversion Plug-ins</span></span>

<span data-ttu-id="3c755-109">Les formats tiers doivent être inscrits avant que le lecteur Windows Media puisse instancier et utiliser le plug-in de conversion.</span><span class="sxs-lookup"><span data-stu-id="3c755-109">Third-party formats must be registered before Windows Media Player can instantiate and use the conversion plug-in.</span></span> <span data-ttu-id="3c755-110">Pour inscrire votre fichier à des fins de conversion, vous devez inscrire l’extension de nom de fichier associée à votre format.</span><span class="sxs-lookup"><span data-stu-id="3c755-110">To register your file for conversion, you must register the file name extension associated with your format.</span></span>

<span data-ttu-id="3c755-111">La liste des extensions de nom de fichier inscrites est conservée sous la forme d’un ensemble de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="3c755-111">The list of registered file name extensions is maintained as a set of registry keys.</span></span> <span data-ttu-id="3c755-112">Pour plus d’informations sur l’inscription de formats tiers, consultez Paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3c755-112">For details about registering third-party formats, see [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="3c755-113">Le tableau suivant répertorie les paramètres de valeur de Registre permettant d’inscrire un format tiers pour la conversion à l’aide d’un plug-in de conversion.</span><span class="sxs-lookup"><span data-stu-id="3c755-113">The following table lists the registry value settings to register a third-party format for conversion by using a conversion plug-in.</span></span>



| <span data-ttu-id="3c755-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c755-114">Value</span></span>                  | <span data-ttu-id="3c755-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3c755-115">Setting</span></span>                                                     |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="3c755-116">**Runtime**</span><span class="sxs-lookup"><span data-stu-id="3c755-116">**Runtime**</span></span>            | <span data-ttu-id="3c755-117">13</span><span class="sxs-lookup"><span data-stu-id="3c755-117">13</span></span>                                                          |
| <span data-ttu-id="3c755-118">**autorisations**</span><span class="sxs-lookup"><span data-stu-id="3c755-118">**Permissions**</span></span>        | <span data-ttu-id="3c755-119">8 (autorisation pour la bibliothèque).</span><span class="sxs-lookup"><span data-stu-id="3c755-119">8 (Permission for the library).</span></span>                             |
| <span data-ttu-id="3c755-120">**ConvertPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="3c755-120">**ConvertPluginCLSID**</span></span> | <span data-ttu-id="3c755-121">ID de classe du plug-in de conversion, au format de registre.</span><span class="sxs-lookup"><span data-stu-id="3c755-121">The class ID of the conversion plug-in, in registry format.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3c755-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c755-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c755-123">**Référence de programmation de plug-ins de conversion**</span><span class="sxs-lookup"><span data-stu-id="3c755-123">**Conversion Plug-ins Programming Reference**</span></span>](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




