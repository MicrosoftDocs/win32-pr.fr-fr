---
title: DRM_ActionAllowed_CollaborativePlay
description: L' \_ attribut DRM ActionAllowed \_ CollaborativePlay indique si la licence permet de lire le contenu en collaboration.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- Format Windows Media DRM_ActionAllowed_CollaborativePlay
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381549"
---
# <a name="drm_actionallowed_collaborativeplay"></a><span data-ttu-id="65b57-104">\_ACTIONALLOWED DRM \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="65b57-104">DRM\_ActionAllowed\_CollaborativePlay</span></span>

<span data-ttu-id="65b57-105">L’attribut **DRM \_ ActionAllowed \_ CollaborativePlay** indique si la licence permet de lire le contenu en collaboration.</span><span class="sxs-lookup"><span data-stu-id="65b57-105">The **DRM\_ActionAllowed\_CollaborativePlay** attribute indicates whether the license allows the content to be played collaboratively.</span></span>

## <a name="global-constant"></a><span data-ttu-id="65b57-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="65b57-106">Global Constant</span></span>

<span data-ttu-id="65b57-107">g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="65b57-107">g\_wszWMDRM\_ActionAllowed\_CollaborativePlay</span></span>

## <a name="data-type"></a><span data-ttu-id="65b57-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="65b57-108">Data Type</span></span>

<span data-ttu-id="65b57-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="65b57-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="65b57-110">Notes</span><span class="sxs-lookup"><span data-stu-id="65b57-110">Remarks</span></span>

<span data-ttu-id="65b57-111">Le droit de travail collaboratif s’applique à la lecture de contenu protégé dans le cadre d’une session de collaboration utilisant des services d’égal à égal.</span><span class="sxs-lookup"><span data-stu-id="65b57-111">The collaborative play right applies to playing protected content as part of a collaborative session using peer-to-peer services.</span></span> <span data-ttu-id="65b57-112">Par exemple, les utilisateurs de MSN Messenger 2004 peuvent lire du contenu protégé dans une session MusicMix.</span><span class="sxs-lookup"><span data-stu-id="65b57-112">For example, users of MSN Messenger 2004 can play protected content in a MusicMix session.</span></span> <span data-ttu-id="65b57-113">Ce droit ne peut être utilisé que pour fournir un fichier protégé à une seule session à la fois et tous les utilisateurs participant à la session doivent être en ligne pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="65b57-113">This right can only be used to contribute a protected file to a single session at one time, and all users participating in the session must be online to render the content.</span></span>

<span data-ttu-id="65b57-114">Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="65b57-114">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="65b57-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65b57-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b57-116">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="65b57-116">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




