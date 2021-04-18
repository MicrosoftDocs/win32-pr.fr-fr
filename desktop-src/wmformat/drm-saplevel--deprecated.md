---
title: DRM_SAPLEVEL (déconseillée)
description: Spécifie le niveau de chemin d’accès audio sécurisé (SAP) pris en charge par votre application.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- Format Windows Media DRM_SAPLEVEL (obsolète)
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522771"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="210c7-104">\_SAPLEVEL DRM (déconseillé)</span><span class="sxs-lookup"><span data-stu-id="210c7-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="210c7-105">\[**DRM \_ SAPLEVEL** n’est plus disponible pour une utilisation à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="210c7-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="210c7-106">Au lieu de cela, utilisez PUMA (Protected user mode audio) dans la bibliothèque Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="210c7-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="210c7-107">\]</span><span class="sxs-lookup"><span data-stu-id="210c7-107">\]</span></span>

<span data-ttu-id="210c7-108">La propriété **DRM \_ SAPLEVEL** spécifie le niveau de chemin d’accès audio sécurisé (SAP) pris en charge par votre application.</span><span class="sxs-lookup"><span data-stu-id="210c7-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="210c7-109">Constante globale</span><span class="sxs-lookup"><span data-stu-id="210c7-109">Global Constant</span></span>

<span data-ttu-id="210c7-110">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="210c7-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="210c7-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="210c7-111">Data Type</span></span>

<span data-ttu-id="210c7-112">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="210c7-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="210c7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="210c7-113">Remarks</span></span>

<span data-ttu-id="210c7-114">Il s’agit d’une propriété en écriture seule qui est définie en appelant [**IWMDRMReader :: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="210c7-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="210c7-115">La valeur est une représentation sous forme de chaîne de caractères larges du niveau SAP, telle que L "200".</span><span class="sxs-lookup"><span data-stu-id="210c7-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="210c7-116">Les valeurs actuellement prises en charge sont 200 et 300.</span><span class="sxs-lookup"><span data-stu-id="210c7-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="210c7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="210c7-117">Requirements</span></span>



| <span data-ttu-id="210c7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="210c7-118">Requirement</span></span> | <span data-ttu-id="210c7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="210c7-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="210c7-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="210c7-120">End of client support</span></span><br/> | <span data-ttu-id="210c7-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="210c7-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="210c7-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="210c7-122">End of server support</span></span><br/> | <span data-ttu-id="210c7-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="210c7-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="210c7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="210c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210c7-125">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="210c7-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





