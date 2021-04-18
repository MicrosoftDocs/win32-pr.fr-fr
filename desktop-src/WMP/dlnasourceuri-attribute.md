---
title: Attribut DLNASourceURI
description: L’attribut DLNASourceURI est l’URI (Universal Resource Identifier) de l’élément.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Attribut DLNASourceURI lecteur Windows Media
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540419"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="2f059-104">Attribut DLNASourceURI</span><span class="sxs-lookup"><span data-stu-id="2f059-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="2f059-105">L’attribut **DLNASourceURI** est l’URI (Universal Resource Identifier) de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2f059-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2f059-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="2f059-106">Applies To</span></span>

-   [<span data-ttu-id="2f059-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="2f059-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="2f059-108">**Autres éléments**</span><span class="sxs-lookup"><span data-stu-id="2f059-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="2f059-109">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="2f059-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="2f059-110">**Éléments de sélection**</span><span class="sxs-lookup"><span data-stu-id="2f059-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="2f059-111">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="2f059-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="2f059-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2f059-112">Remarks</span></span>

<span data-ttu-id="2f059-113">Si l’élément se trouve dans la bibliothèque locale de l’utilisateur actuel, cet attribut, l’attribut [**SourceURL**](sourceurl-attribute.md) et la valeur retournée par [**IWMPMedia :: \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) sont tous identiques.</span><span class="sxs-lookup"><span data-stu-id="2f059-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="2f059-114">Si l’élément ne se trouve pas dans la bibliothèque locale de l’utilisateur actuel, mais appartient à une bibliothèque distante, cet attribut est un identificateur de la forme DLNA-playsingle://*xxx*.</span><span class="sxs-lookup"><span data-stu-id="2f059-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="2f059-115">Vous pouvez transmettre un URI DLNA-playsingle à la méthode [**IWMPCore3 :: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) pour obtenir une interface [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) qui vous permet d’afficher les métadonnées de l’élément multimédia et éventuellement de modifier l’évaluation de l’étoile de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="2f059-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="2f059-116">Notez, toutefois, que l’URI DLNA-playsingle doit être destiné à un service d’annuaire de contenu (CDS) déjà découvert par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2f059-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="2f059-117">La méthode **newMedia** ne lance pas la découverte UPnP et ne recherche pas les CDs.</span><span class="sxs-lookup"><span data-stu-id="2f059-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="2f059-118">Vous pouvez modifier l’évaluation de l’étoile d’un élément multimédia dans une bibliothèque distante uniquement si la bibliothèque distante prend en charge l’opération de modification.</span><span class="sxs-lookup"><span data-stu-id="2f059-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="2f059-119">Les bibliothèques distantes hébergées sur un ordinateur exécutant Windows 7 prennent en charge l’opération de modification.</span><span class="sxs-lookup"><span data-stu-id="2f059-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="2f059-120">Les bibliothèques distantes hébergées sur un ordinateur exécutant un système d’exploitation Windows antérieur à Windows 7 ne prennent pas en charge l’opération de modification.</span><span class="sxs-lookup"><span data-stu-id="2f059-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f059-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f059-121">Requirements</span></span>



| <span data-ttu-id="2f059-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f059-122">Requirement</span></span> | <span data-ttu-id="2f059-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f059-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="2f059-124">Version</span><span class="sxs-lookup"><span data-stu-id="2f059-124">Version</span></span><br/> | <span data-ttu-id="2f059-125">Lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="2f059-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f059-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f059-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f059-127">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="2f059-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





