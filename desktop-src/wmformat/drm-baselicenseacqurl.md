---
title: DRM_BaseLicenseAcqURL
description: L' \_ attribut DRM BaseLicenseAcqURL contient une URL de base partielle à laquelle une application de joueur doit accéder pour obtenir une licence pour le contenu.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- Format Windows Media DRM_BaseLicenseAcqURL
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101245"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="df5ff-104">\_BASELICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="df5ff-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="df5ff-105">L’attribut **DRM \_ BaseLicenseAcqURL** contient une URL de base partielle à laquelle une application de joueur doit accéder pour obtenir une licence pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="df5ff-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="df5ff-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="df5ff-106">Global Constant</span></span>

<span data-ttu-id="df5ff-107">g \_ wszWMDRM \_ BaseLicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="df5ff-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="df5ff-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="df5ff-108">Data Type</span></span>

<span data-ttu-id="df5ff-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="df5ff-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="df5ff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="df5ff-110">Remarks</span></span>

<span data-ttu-id="df5ff-111">Il s’agit d’une propriété en lecture-écriture facultative qui est définie et récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="df5ff-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="df5ff-112">Il est fourni pour permettre aux systèmes de distribution de licences d’utiliser des chemins d’accès relatifs dans les propriétés de l’URL d’acquisition de licence.</span><span class="sxs-lookup"><span data-stu-id="df5ff-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="df5ff-113">Après avoir défini cette propriété, toutes les URL d’acquisition de licence partielles dans les en-têtes de contenu auront l’URL de base ajoutée au début de l’URL partielle pour former une URL complète pour l’application de lecteur à laquelle naviguer.</span><span class="sxs-lookup"><span data-stu-id="df5ff-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="df5ff-114">L’appel de **IWMDRMReader :: GetDRMProperty** pour **DRM \_ BaseLicenseAcqURL** ne fonctionne que dans la même session que celle qui a été définie.</span><span class="sxs-lookup"><span data-stu-id="df5ff-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="df5ff-115">La propriété n’est pas stockée dans l’en-tête de contenu ; Il est dynamique, et seule l’URL relative est stockée dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="df5ff-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="df5ff-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df5ff-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5ff-117">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="df5ff-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




