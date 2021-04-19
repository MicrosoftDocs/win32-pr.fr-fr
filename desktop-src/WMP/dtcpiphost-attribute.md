---
title: Attribut DTCPIPHost
description: L’attribut DTCPIPHost est le nom ou l’adresse IP de l’ordinateur ou du périphérique qui doit être contacté pour la transmission numérique protection du contenu via l’échange de clés authentifiées DTCP-IP (ACÉ) pour l’élément multimédia.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Attribut DTCPIPHost lecteur Windows Media
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525588"
---
# <a name="dtcpiphost-attribute"></a><span data-ttu-id="3ed4b-104">Attribut DTCPIPHost</span><span class="sxs-lookup"><span data-stu-id="3ed4b-104">DTCPIPHost Attribute</span></span>

<span data-ttu-id="3ed4b-105">L’attribut **DTCPIPHost** est le nom ou l’adresse IP de l’ordinateur ou du périphérique qui doit être contacté pour la Transmission numérique protection du contenu via l’échange de clés authentifiées DTCP-IP (ACÉ) pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="3ed4b-105">The **DTCPIPHost** attribute is the name or IP address of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3ed4b-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="3ed4b-106">Applies To</span></span>

-   [<span data-ttu-id="3ed4b-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="3ed4b-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="3ed4b-108">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="3ed4b-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="3ed4b-109">**Éléments de sélection**</span><span class="sxs-lookup"><span data-stu-id="3ed4b-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="3ed4b-110">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="3ed4b-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="3ed4b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3ed4b-111">Remarks</span></span>

<span data-ttu-id="3ed4b-112">Si cet attribut est disponible, l’élément multimédia est protégé à l’aide de DTCP-IP.</span><span class="sxs-lookup"><span data-stu-id="3ed4b-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="3ed4b-113">Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="3ed4b-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="3ed4b-114">Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé.</span><span class="sxs-lookup"><span data-stu-id="3ed4b-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="3ed4b-115">Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="3ed4b-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed4b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ed4b-116">Requirements</span></span>



| <span data-ttu-id="3ed4b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ed4b-117">Requirement</span></span> | <span data-ttu-id="3ed4b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ed4b-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="3ed4b-119">Version</span><span class="sxs-lookup"><span data-stu-id="3ed4b-119">Version</span></span><br/> | <span data-ttu-id="3ed4b-120">Lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="3ed4b-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ed4b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ed4b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed4b-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="3ed4b-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





