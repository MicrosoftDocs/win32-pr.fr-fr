---
title: Élément sidType (ChannelPublishingType)
description: Détermine s’il faut inclure un identificateur de sécurité (SID) du principal avec chaque événement écrit dans le canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- EventLog, élément sidType
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509109"
---
# <a name="sidtype-channelpublishingtype-element"></a><span data-ttu-id="da07d-104">Élément sidType (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="da07d-104">sidType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="da07d-105">Détermine s’il faut inclure un identificateur de sécurité (SID) du principal avec chaque événement écrit dans le canal.</span><span class="sxs-lookup"><span data-stu-id="da07d-105">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span>

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="da07d-106">L’élément **sidType** est défini par le type complexe [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="da07d-106">The **sidType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="da07d-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da07d-107">Requirements</span></span>



| <span data-ttu-id="da07d-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da07d-108">Requirement</span></span> | <span data-ttu-id="da07d-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="da07d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da07d-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da07d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="da07d-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da07d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da07d-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da07d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="da07d-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da07d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da07d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da07d-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="da07d-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="da07d-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="da07d-116">**publication (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="da07d-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





