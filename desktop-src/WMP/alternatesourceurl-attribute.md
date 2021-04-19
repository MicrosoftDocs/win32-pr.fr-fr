---
title: Attribut AlternateSourceURL
description: L’attribut AlternateSourceURL est un localisateur de ressources uniforme pour l’élément multimédia qui sert d’alternative aux attributs DLNASourceURI et SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Attribut AlternateSourceURL lecteur Windows Media
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535992"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="b306b-104">Attribut AlternateSourceURL</span><span class="sxs-lookup"><span data-stu-id="b306b-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="b306b-105">L’attribut **AlternateSourceURL** est un localisateur de ressources uniforme pour l’élément multimédia qui sert d’alternative aux attributs [**DLNASourceURI**](dlnasourceuri-attribute.md) et [**SourceURL**](sourceurl-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b306b-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b306b-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="b306b-106">Applies To</span></span>

-   [<span data-ttu-id="b306b-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="b306b-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b306b-108">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="b306b-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="b306b-109">**Éléments de sélection**</span><span class="sxs-lookup"><span data-stu-id="b306b-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b306b-110">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="b306b-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b306b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b306b-111">Remarks</span></span>

<span data-ttu-id="b306b-112">Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="b306b-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="b306b-113">Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé.</span><span class="sxs-lookup"><span data-stu-id="b306b-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="b306b-114">Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="b306b-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="b306b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b306b-115">Requirements</span></span>



| <span data-ttu-id="b306b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b306b-116">Requirement</span></span> | <span data-ttu-id="b306b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b306b-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="b306b-118">Version</span><span class="sxs-lookup"><span data-stu-id="b306b-118">Version</span></span><br/> | <span data-ttu-id="b306b-119">Lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="b306b-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b306b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b306b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b306b-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="b306b-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





