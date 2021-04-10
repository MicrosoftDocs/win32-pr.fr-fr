---
description: Définit la section du manifeste d’instrumentation qui identifie le fournisseur et les compteurs qu’ils fournissent.
ms.assetid: c661f1af-ebe8-4f8a-b77e-a2229f45facd
title: Type complexe des compteurs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ad87b79175b0cecdec17ad081340fa0be2b90b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952003"
---
# <a name="counters-complex-type"></a><span data-ttu-id="231f2-103">Type complexe des compteurs</span><span class="sxs-lookup"><span data-stu-id="231f2-103">counters Complex Type</span></span>

<span data-ttu-id="231f2-104">Définit la section du manifeste d’instrumentation qui identifie le fournisseur et les compteurs qu’ils fournissent.</span><span class="sxs-lookup"><span data-stu-id="231f2-104">Defines the section of the instrumentation manifest that identifies the provider and the counters that they provide.</span></span>

``` syntax
<xs:complexType name="counters">
    <xs:choice
        minOccurs="1"
        maxOccurs="1"
    >
        <xs:element name="provider"
            type="man:provider"
         />
    </xs:choice>
    <xs:attribute name="schemaVersion"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="1.1"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="231f2-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="231f2-105">Child elements</span></span>



| <span data-ttu-id="231f2-106">Élément</span><span class="sxs-lookup"><span data-stu-id="231f2-106">Element</span></span>      | <span data-ttu-id="231f2-107">Type</span><span class="sxs-lookup"><span data-stu-id="231f2-107">Type</span></span>                                                               | <span data-ttu-id="231f2-108">Description</span><span class="sxs-lookup"><span data-stu-id="231f2-108">Description</span></span>                                              |
|--------------|--------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="231f2-109">**moteur**</span><span class="sxs-lookup"><span data-stu-id="231f2-109">**provider**</span></span> | [<span data-ttu-id="231f2-110">**homme : fournisseur**</span><span class="sxs-lookup"><span data-stu-id="231f2-110">**man:provider**</span></span>](performance-counters-provider-complex-type.md) | <span data-ttu-id="231f2-111">Identifie un fournisseur qui fournit des compteurs.</span><span class="sxs-lookup"><span data-stu-id="231f2-111">Identifies a provider that provides counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="231f2-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="231f2-112">Attributes</span></span>



| <span data-ttu-id="231f2-113">Nom</span><span class="sxs-lookup"><span data-stu-id="231f2-113">Name</span></span>          | <span data-ttu-id="231f2-114">Type</span><span class="sxs-lookup"><span data-stu-id="231f2-114">Type</span></span> | <span data-ttu-id="231f2-115">Description</span><span class="sxs-lookup"><span data-stu-id="231f2-115">Description</span></span>                                                      |
|---------------|------|------------------------------------------------------------------|
| <span data-ttu-id="231f2-116">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="231f2-116">schemaVersion</span></span> |      | <span data-ttu-id="231f2-117">Version du schéma utilisé pour écrire le manifeste.</span><span class="sxs-lookup"><span data-stu-id="231f2-117">The version of the schema used to write the manifest.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="231f2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="231f2-118">Requirements</span></span>



| <span data-ttu-id="231f2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="231f2-119">Requirement</span></span> | <span data-ttu-id="231f2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="231f2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="231f2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="231f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="231f2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="231f2-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="231f2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="231f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="231f2-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="231f2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="231f2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="231f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231f2-126">**Instrumentation**</span><span class="sxs-lookup"><span data-stu-id="231f2-126">**instrumentation**</span></span>](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype)
</dt> </dl>

 

