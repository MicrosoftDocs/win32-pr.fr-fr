---
title: Attribut DLNAServerUDN
description: L’attribut DLNAServerUDN est le nom d’appareil unique du serveur qui héberge l’élément multimédia.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Attribut DLNAServerUDN lecteur Windows Media
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525525"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="5e2d8-104">Attribut DLNAServerUDN</span><span class="sxs-lookup"><span data-stu-id="5e2d8-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="5e2d8-105">L’attribut **DLNAServerUDN** est le nom d’appareil unique du serveur qui héberge l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5e2d8-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="5e2d8-106">Applies To</span></span>

-   [<span data-ttu-id="5e2d8-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="5e2d8-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5e2d8-108">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="5e2d8-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="5e2d8-109">**Éléments de sélection**</span><span class="sxs-lookup"><span data-stu-id="5e2d8-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="5e2d8-110">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="5e2d8-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5e2d8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5e2d8-111">Remarks</span></span>

<span data-ttu-id="5e2d8-112">Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="5e2d8-113">Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé.</span><span class="sxs-lookup"><span data-stu-id="5e2d8-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="5e2d8-114">Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="5e2d8-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2d8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e2d8-115">Requirements</span></span>



| <span data-ttu-id="5e2d8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e2d8-116">Requirement</span></span> | <span data-ttu-id="5e2d8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e2d8-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="5e2d8-118">Version</span><span class="sxs-lookup"><span data-stu-id="5e2d8-118">Version</span></span><br/> | <span data-ttu-id="5e2d8-119">Lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="5e2d8-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e2d8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e2d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2d8-121">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="5e2d8-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





