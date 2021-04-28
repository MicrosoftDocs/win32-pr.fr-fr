---
description: 'MF_MT_FSSourceTypeDecoded attribute : spécifie si un décodeur peut utiliser des horodatages de décodage lors de la définition d’horodatages.'
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093087"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="b5521-103">\_ \_ Attribut FSSourceTypeDecoded MF MT</span><span class="sxs-lookup"><span data-stu-id="b5521-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="b5521-104">Spécifie qu’un type de média est décodé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b5521-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5521-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b5521-105">Data type</span></span>

<span data-ttu-id="b5521-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5521-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="b5521-107">Notes </span><span class="sxs-lookup"><span data-stu-id="b5521-107">Remarks</span></span>
<span data-ttu-id="b5521-108">Un type de média est marqué comme un attribut pour indiquer qu’il n’existe pas sur la source physique et est synthétisé par le pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5521-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="b5521-109">La valeur 1 (TRUE) indique que le type de média est synthétisé.</span><span class="sxs-lookup"><span data-stu-id="b5521-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="b5521-110">La valeur 0 (FALSe), ou la valeur qui n’est pas présente, indique qu’elle ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="b5521-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="b5521-111">Dans la version actuelle, cet attribut doit être spécifié à l’aide de la valeur GUID suivante au lieu de la constante MD_MT_FSSourceTypeDecoded :</span><span class="sxs-lookup"><span data-stu-id="b5521-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="b5521-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5521-112">Requirements</span></span>



| <span data-ttu-id="b5521-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5521-113">Requirement</span></span> | <span data-ttu-id="b5521-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5521-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5521-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5521-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b5521-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b5521-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b5521-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5521-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b5521-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b5521-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="b5521-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5521-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5521-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b5521-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




