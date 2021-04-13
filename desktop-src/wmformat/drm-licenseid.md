---
title: DRM_LicenseID
description: La \_ propriété DRM LicenseID contient une chaîne extraite de la licence associée au fichier actuellement ouvert qui identifie de façon unique cette licence.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- Format Windows Media DRM_LicenseID
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314347"
---
# <a name="drm_licenseid"></a><span data-ttu-id="1d7be-104">\_LICENSEID DRM</span><span class="sxs-lookup"><span data-stu-id="1d7be-104">DRM\_LicenseID</span></span>

<span data-ttu-id="1d7be-105">La propriété **DRM \_ LicenseID** contient une chaîne extraite de la licence associée au fichier actuellement ouvert qui identifie de façon unique cette licence.</span><span class="sxs-lookup"><span data-stu-id="1d7be-105">The **DRM\_LicenseID** property contains a string retrieved from the license associated with the currently open file that uniquely identifies that license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1d7be-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="1d7be-106">Global Constant</span></span>

<span data-ttu-id="1d7be-107">g \_ wszWMDRM \_ LicenseID</span><span class="sxs-lookup"><span data-stu-id="1d7be-107">g\_wszWMDRM\_LicenseID</span></span>

## <a name="data-type"></a><span data-ttu-id="1d7be-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="1d7be-108">Data Type</span></span>

<span data-ttu-id="1d7be-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1d7be-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d7be-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1d7be-110">Remarks</span></span>

<span data-ttu-id="1d7be-111">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="1d7be-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="1d7be-112">Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="1d7be-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

<span data-ttu-id="1d7be-113">L’ID de licence est stocké dans une licence, et non dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="1d7be-113">The license ID is stored in a license, not in an ASF file.</span></span> <span data-ttu-id="1d7be-114">Chaque licence a un ID unique affecté par le générateur de licences au moment de la création de la licence.</span><span class="sxs-lookup"><span data-stu-id="1d7be-114">Each individual license has a unique ID which is assigned by the license generator at the time the license is created.</span></span> <span data-ttu-id="1d7be-115">Par exemple, si vous obtenez deux licences pour le même contenu, chacune d’entre elles aura un attribut LicenseID différent.</span><span class="sxs-lookup"><span data-stu-id="1d7be-115">For example, if you obtain two licenses for the same content, each one will have a different LicenseID attribute.</span></span> <span data-ttu-id="1d7be-116">En règle générale, les applications n’ont pas besoin de récupérer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="1d7be-116">Typically, applications have no need to retrieve this value.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d7be-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d7be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d7be-118">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="1d7be-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




