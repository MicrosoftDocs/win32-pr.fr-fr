---
title: DRM_DRMHeader_KeyID
description: L' \_ attribut DRM DRMHeader \_ KeyId contient l’ID de clé du fichier.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- Format Windows Media DRM_DRMHeader_KeyID
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314287"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="4f4b4-104">\_DRMHEADER DRM \_ KeyId</span><span class="sxs-lookup"><span data-stu-id="4f4b4-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="4f4b4-105">L’attribut **DRM \_ DRMHeader \_ KEYID** contient l’ID de clé du fichier.</span><span class="sxs-lookup"><span data-stu-id="4f4b4-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4f4b4-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="4f4b4-106">Global Constant</span></span>

<span data-ttu-id="4f4b4-107">g \_ wszWMDRM \_ DRMHeader \_ KeyId</span><span class="sxs-lookup"><span data-stu-id="4f4b4-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="4f4b4-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="4f4b4-108">Data Type</span></span>

<span data-ttu-id="4f4b4-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="4f4b4-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="4f4b4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4f4b4-110">Remarks</span></span>

<span data-ttu-id="4f4b4-111">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="4f4b4-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="4f4b4-112">Il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="4f4b4-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="4f4b4-113">Pour définir l’ID de clé sur le fichier à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , vous devez utiliser la propriété [**DRM \_ KeyId**](drm-keyid.md) .</span><span class="sxs-lookup"><span data-stu-id="4f4b4-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f4b4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f4b4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4b4-115">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="4f4b4-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




