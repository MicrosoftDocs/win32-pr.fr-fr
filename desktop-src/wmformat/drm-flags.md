---
title: DRM_Flags
description: La \_ propriété indicateurs DRM est utilisée avec le contenu DRM version 1 uniquement pour spécifier les droits qui seront contenus dans la licence locale.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- Format Windows Media DRM_Flags
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940679"
---
# <a name="drm_flags"></a><span data-ttu-id="36bd3-104">\_Indicateurs DRM</span><span class="sxs-lookup"><span data-stu-id="36bd3-104">DRM\_Flags</span></span>

<span data-ttu-id="36bd3-105">La **propriété \_ indicateurs DRM** est utilisée avec le contenu DRM version 1 uniquement pour spécifier les droits qui seront contenus dans la licence locale.</span><span class="sxs-lookup"><span data-stu-id="36bd3-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="36bd3-106">Les droits sont spécifiés avec les valeurs définies par le type d’énumération des **\_ droits WMT** .</span><span class="sxs-lookup"><span data-stu-id="36bd3-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="36bd3-107">Il est possible de sélectionner plusieurs valeurs en les associant à l' **opérateur de bits or.**</span><span class="sxs-lookup"><span data-stu-id="36bd3-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="36bd3-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="36bd3-108">Global Constant</span></span>

<span data-ttu-id="36bd3-109">\_indicateurs wszWMDRM \_ g</span><span class="sxs-lookup"><span data-stu-id="36bd3-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="36bd3-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="36bd3-110">Data Type</span></span>

<span data-ttu-id="36bd3-111">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="36bd3-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="36bd3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="36bd3-112">Remarks</span></span>

<span data-ttu-id="36bd3-113">Lors de l’accès à l’interface **IWMHeaderInfo3** de l’objet Writer, vous pouvez ajouter ou modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="36bd3-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="36bd3-114">Dans d’autres objets (éditeur de métadonnées, lecteur et lecteur synchrone), cette valeur est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="36bd3-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="36bd3-115">Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour définir cette propriété lors de la création de contenu DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="36bd3-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="36bd3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36bd3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bd3-117">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="36bd3-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




