---
title: Attribut temporaire
description: L’attribut Temporary spécifie si une sélection est temporaire.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Attribut temporaire lecteur Windows Media
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542245"
---
# <a name="temporary-attribute"></a><span data-ttu-id="5cc9b-104">Attribut temporaire</span><span class="sxs-lookup"><span data-stu-id="5cc9b-104">Temporary Attribute</span></span>

<span data-ttu-id="5cc9b-105">L’attribut **Temporary** spécifie si une sélection est temporaire.</span><span class="sxs-lookup"><span data-stu-id="5cc9b-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="5cc9b-106">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5cc9b-106">**Remarks**</span></span>

<span data-ttu-id="5cc9b-107">Si vous avez récupéré une sélection à partir de la bibliothèque, les modifications apportées à la sélection sont reflétées dans la bibliothèque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5cc9b-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="5cc9b-108">Pour éviter cela, appelez [IWMPPlaylist :: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) en passant le nom d’attribut « Temporary » et la valeur « true ».</span><span class="sxs-lookup"><span data-stu-id="5cc9b-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="5cc9b-109">Cela convertit votre instance de playlist en sélection temporaire, qui peut être modifiée en toute sécurité sans modifier la sélection d’origine.</span><span class="sxs-lookup"><span data-stu-id="5cc9b-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="5cc9b-110">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5cc9b-110">**Applies To**</span></span>

-   [<span data-ttu-id="5cc9b-111">Sélections</span><span class="sxs-lookup"><span data-stu-id="5cc9b-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="5cc9b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cc9b-112">Requirements</span></span>



| <span data-ttu-id="5cc9b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cc9b-113">Requirement</span></span> | <span data-ttu-id="5cc9b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cc9b-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="5cc9b-115">Version</span><span class="sxs-lookup"><span data-stu-id="5cc9b-115">Version</span></span><br/> | <span data-ttu-id="5cc9b-116">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="5cc9b-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cc9b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cc9b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc9b-118">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="5cc9b-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





