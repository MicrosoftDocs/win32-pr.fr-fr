---
title: Élément clockType (ChannelPublishingType)
description: Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- EventLog, élément clockType
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6b85537ec209f39da87e74db6881abdf60e488b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384028"
---
# <a name="clocktype-channelpublishingtype-element"></a><span data-ttu-id="b8702-104">Élément clockType (ChannelPublishingType)</span><span class="sxs-lookup"><span data-stu-id="b8702-104">clockType (ChannelPublishingType) Element</span></span>

<span data-ttu-id="b8702-105">Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement.</span><span class="sxs-lookup"><span data-stu-id="b8702-105">The clock resolution to use when logging the time stamp for each event.</span></span>

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="b8702-106">L’élément **clockType** est défini par le type complexe [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8702-106">The **clockType** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8702-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8702-107">Requirements</span></span>



| <span data-ttu-id="b8702-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8702-108">Requirement</span></span> | <span data-ttu-id="b8702-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8702-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8702-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8702-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b8702-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8702-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8702-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8702-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b8702-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8702-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8702-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8702-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8702-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="b8702-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="b8702-116">**publication (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="b8702-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





