---
title: Élément Security (SystemPropertiesType)
description: Identifie l’utilisateur qui a enregistré l’événement.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- EventLog, élément de sécurité
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105796"
---
# <a name="security-systempropertiestype-element"></a><span data-ttu-id="903cb-104">Élément Security (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="903cb-104">Security (SystemPropertiesType) Element</span></span>

<span data-ttu-id="903cb-105">Identifie l’utilisateur qui a enregistré l’événement.</span><span class="sxs-lookup"><span data-stu-id="903cb-105">Identifies the user that logged the event.</span></span>

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="903cb-106">L’élément de **sécurité** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="903cb-106">The **Security** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="903cb-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="903cb-107">Attributes</span></span>



| <span data-ttu-id="903cb-108">Nom</span><span class="sxs-lookup"><span data-stu-id="903cb-108">Name</span></span>   | <span data-ttu-id="903cb-109">Type</span><span class="sxs-lookup"><span data-stu-id="903cb-109">Type</span></span>   | <span data-ttu-id="903cb-110">Description</span><span class="sxs-lookup"><span data-stu-id="903cb-110">Description</span></span>                                                          |
|--------|--------|----------------------------------------------------------------------|
| <span data-ttu-id="903cb-111">UserID</span><span class="sxs-lookup"><span data-stu-id="903cb-111">UserID</span></span> | <span data-ttu-id="903cb-112">string</span><span class="sxs-lookup"><span data-stu-id="903cb-112">string</span></span> | <span data-ttu-id="903cb-113">Identificateur de sécurité (SID) de l’utilisateur sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="903cb-113">The security identifier (SID) of the user in string form.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="903cb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="903cb-114">Requirements</span></span>



| <span data-ttu-id="903cb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="903cb-115">Requirement</span></span> | <span data-ttu-id="903cb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="903cb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="903cb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="903cb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="903cb-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="903cb-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="903cb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="903cb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="903cb-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="903cb-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="903cb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="903cb-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="903cb-122">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="903cb-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="903cb-123">**Système (EventType)**</span><span class="sxs-lookup"><span data-stu-id="903cb-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





