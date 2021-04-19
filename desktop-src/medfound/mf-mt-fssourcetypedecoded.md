---
description: Spécifie si un décodeur peut utiliser des horodatages de décodage (DTS) lors de la définition des horodatages.
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ad80b0b7b29677ed0bee2f86a2c12c56c08441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531211"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="824e4-103">\_ \_ Attribut FSSourceTypeDecoded MF MT</span><span class="sxs-lookup"><span data-stu-id="824e4-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="824e4-104">Spécifie qu’un type de média est décodé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="824e4-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="824e4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="824e4-105">Data type</span></span>

<span data-ttu-id="824e4-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="824e4-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="824e4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="824e4-107">Remarks</span></span>
<span data-ttu-id="824e4-108">Un type de média est marqué comme un attribut pour indiquer qu’il n’existe pas sur la source physique et est synthétisé par le pipeline.</span><span class="sxs-lookup"><span data-stu-id="824e4-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="824e4-109">La valeur 1 (TRUE) indique que le type de média est synthétisé.</span><span class="sxs-lookup"><span data-stu-id="824e4-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="824e4-110">La valeur 0 (FALSe), ou la valeur qui n’est pas présente, indique qu’elle ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="824e4-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="824e4-111">Dans la version actuelle, cet attribut doit être spécifié à l’aide de la valeur GUID suivante au lieu de la constante MD_MT_FSSourceTypeDecoded :</span><span class="sxs-lookup"><span data-stu-id="824e4-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="824e4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="824e4-112">Requirements</span></span>



| <span data-ttu-id="824e4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="824e4-113">Requirement</span></span> | <span data-ttu-id="824e4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="824e4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="824e4-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="824e4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="824e4-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="824e4-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="824e4-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="824e4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="824e4-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="824e4-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="824e4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="824e4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824e4-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="824e4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




