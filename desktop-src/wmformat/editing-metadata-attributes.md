---
title: Modification des attributs de métadonnées
description: Modification des attributs de métadonnées
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK, modification des attributs de métadonnées
- ASF (Advanced Systems Format), modification des attributs de métadonnées
- ASF (format de systèmes avancés), modification des attributs de métadonnées
- métadonnées, modifier les attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381556"
---
# <a name="editing-metadata-attributes"></a><span data-ttu-id="9b993-107">Modification des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9b993-107">Editing Metadata Attributes</span></span>

<span data-ttu-id="9b993-108">La modification des attributs de métadonnées est très similaire à la définition de nouveaux attributs.</span><span class="sxs-lookup"><span data-stu-id="9b993-108">Editing metadata attributes is very similar to setting new ones.</span></span> <span data-ttu-id="9b993-109">Au lieu d’utiliser [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), utilisez [**IWMHeaderInfo3 :: ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span><span class="sxs-lookup"><span data-stu-id="9b993-109">Instead of using [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span></span> <span data-ttu-id="9b993-110">**ModifyAttribute** est identique à **AddAttribute** , sauf que vous ne spécifiez pas de nom d’attribut et que le numéro d’index est un paramètre d’entrée au lieu d’une sortie.</span><span class="sxs-lookup"><span data-stu-id="9b993-110">**ModifyAttribute** is identical to **AddAttribute** except that you do not specify an attribute name, and the index number is an input parameter instead of an output.</span></span>

<span data-ttu-id="9b993-111">Vous pouvez utiliser le nombre de flux 0xFFFF pour spécifier un attribut à modifier à l’aide de son index global.</span><span class="sxs-lookup"><span data-stu-id="9b993-111">You can use stream number 0xFFFF to specify an attribute to modify using its global index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b993-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b993-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b993-113">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="9b993-113">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




