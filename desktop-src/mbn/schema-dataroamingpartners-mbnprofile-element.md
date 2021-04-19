---
description: Spécifie la liste des fournisseurs de réseau préférés au moment de l’itinérance.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Élément DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517532"
---
# <a name="dataroamingpartners-mbnprofile-element"></a><span data-ttu-id="33ddb-103">Élément DataRoamingPartners (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="33ddb-103">DataRoamingPartners (MBNProfile) Element</span></span>

<span data-ttu-id="33ddb-104">L’élément **DataRoamingPartners (MBNProfile)** spécifie la liste des fournisseurs de réseau préférés au moment de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="33ddb-104">The **DataRoamingPartners (MBNProfile)** element specifies the list of preferred network providers at the time of roaming.</span></span>

<span data-ttu-id="33ddb-105">Le service haut débit mobile utilise cet élément pour sélectionner le réseau préféré fourni lors de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="33ddb-105">The Mobile Broadband service uses this element to select the preferred network provide while roaming.</span></span>

<span data-ttu-id="33ddb-106">L’élément possède l’élément enfant suivant, qui doit être défini au moins une fois, mais peut être défini plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="33ddb-106">The element has the following child element which must be defined at least once but can be defined multiple times.</span></span>

-   [<span data-ttu-id="33ddb-107">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="33ddb-107">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md)

<span data-ttu-id="33ddb-108">Cet élément peut avoir au maximum une occurrence.</span><span class="sxs-lookup"><span data-stu-id="33ddb-108">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="33ddb-109">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="33ddb-109">This element is optional.</span></span>

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="33ddb-110">L’élément **DataRoamingPartners** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="33ddb-110">The **DataRoamingPartners** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="33ddb-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="33ddb-111">Child elements</span></span>



| <span data-ttu-id="33ddb-112">Élément</span><span class="sxs-lookup"><span data-stu-id="33ddb-112">Element</span></span>                                                         | <span data-ttu-id="33ddb-113">Type</span><span class="sxs-lookup"><span data-stu-id="33ddb-113">Type</span></span>                                                    | <span data-ttu-id="33ddb-114">Description</span><span class="sxs-lookup"><span data-stu-id="33ddb-114">Description</span></span>                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="33ddb-115">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="33ddb-115">**Provider**</span></span>](schema-provider-dataroamingpartners-element.md) | [<span data-ttu-id="33ddb-116">**providerType**</span><span class="sxs-lookup"><span data-stu-id="33ddb-116">**providerType**</span></span>](schema-providertype-complextype.md) | <span data-ttu-id="33ddb-117">Nom et ID de fournisseur d’un réseau cellulaire.</span><span class="sxs-lookup"><span data-stu-id="33ddb-117">Name and provider ID of a cellular network.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="33ddb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33ddb-118">Requirements</span></span>



| <span data-ttu-id="33ddb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33ddb-119">Requirement</span></span> | <span data-ttu-id="33ddb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="33ddb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="33ddb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33ddb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33ddb-122">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33ddb-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="33ddb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33ddb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33ddb-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33ddb-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="33ddb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33ddb-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="33ddb-126">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="33ddb-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="33ddb-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="33ddb-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="33ddb-128">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="33ddb-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="33ddb-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="33ddb-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




