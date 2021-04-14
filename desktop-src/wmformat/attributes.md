---
title: Attributs (kit de développement logiciel (SDK) Windows Media format 11)
description: Attributs
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383687"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="40546-107">Attributs (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="40546-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="40546-108">Un attribut est un élément individuel de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="40546-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="40546-109">La plupart des attributs peuvent être définis par votre application et sont écrits dans l’en-tête d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="40546-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="40546-110">Certains des attributs prédéfinis sont des attributs codés.</span><span class="sxs-lookup"><span data-stu-id="40546-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="40546-111">Ces attributs ne sont pas stockés dans l’en-tête d’un fichier ASF, mais sont calculés par les objets du kit de développement logiciel (SDK) du format Windows Media lorsque le fichier est chargé.</span><span class="sxs-lookup"><span data-stu-id="40546-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="40546-112">Étant donné que les attributs codés sont toujours calculés, ils sont en lecture seule par nature.</span><span class="sxs-lookup"><span data-stu-id="40546-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="40546-113">Ce kit de développement logiciel (SDK) comprend de nombreuses définitions d’attributs que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="40546-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="40546-114">Vous pouvez également créer vos propres attributs pour décrire le contenu.</span><span class="sxs-lookup"><span data-stu-id="40546-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="40546-115">Les sections suivantes décrivent les attributs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="40546-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="40546-116">Section</span><span class="sxs-lookup"><span data-stu-id="40546-116">Section</span></span>                                                                | <span data-ttu-id="40546-117">Description</span><span class="sxs-lookup"><span data-stu-id="40546-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40546-118">Liste d’attributs</span><span class="sxs-lookup"><span data-stu-id="40546-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="40546-119">Fournit une liste alphabétique de tous les attributs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="40546-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="40546-120">Après la liste, chaque attribut est décrit individuellement.</span><span class="sxs-lookup"><span data-stu-id="40546-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="40546-121">Attributs avec plusieurs valeurs</span><span class="sxs-lookup"><span data-stu-id="40546-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="40546-122">Répertorie les attributs qui peuvent être ajoutés plusieurs fois à un fichier.</span><span class="sxs-lookup"><span data-stu-id="40546-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="40546-123">Attributs par type</span><span class="sxs-lookup"><span data-stu-id="40546-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="40546-124">Contient des listes d’attributs triés par type.</span><span class="sxs-lookup"><span data-stu-id="40546-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="40546-125">Il s’agit notamment des listes d’attributs à usage spécifique (comme ceux qui traitent de la gestion des droits numériques) et des listes d’attributs suggérés par type de contenu.</span><span class="sxs-lookup"><span data-stu-id="40546-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="40546-126">Prise en charge des balises ID3</span><span class="sxs-lookup"><span data-stu-id="40546-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="40546-127">Répertorie les attributs qui sont compatibles avec les balises ID3.</span><span class="sxs-lookup"><span data-stu-id="40546-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="40546-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40546-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40546-129">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="40546-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="40546-130">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="40546-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="40546-131">**IWMHeaderInfo :: SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="40546-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="40546-132">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="40546-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




