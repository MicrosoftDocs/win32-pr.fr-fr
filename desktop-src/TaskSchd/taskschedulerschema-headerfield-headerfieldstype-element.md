---
title: Élément HeaderField (headerFieldsType)
description: Contient un champ pour un en-tête dans un message électronique.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Élément HeaderField Planificateur de tâches
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510580"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="c1d84-104">Élément HeaderField (headerFieldsType)</span><span class="sxs-lookup"><span data-stu-id="c1d84-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="c1d84-105">Contient un champ pour un en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="c1d84-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="c1d84-106">L’élément **HeaderField** est défini par le type complexe [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d84-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c1d84-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c1d84-107">Parent element</span></span>



| <span data-ttu-id="c1d84-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c1d84-108">Element</span></span>                                                                        | <span data-ttu-id="c1d84-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="c1d84-109">Derived from</span></span>                                                                 | <span data-ttu-id="c1d84-110">Description</span><span class="sxs-lookup"><span data-stu-id="c1d84-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1d84-111">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="c1d84-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="c1d84-112">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="c1d84-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="c1d84-113">Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.</span><span class="sxs-lookup"><span data-stu-id="c1d84-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c1d84-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1d84-114">Child elements</span></span>



| <span data-ttu-id="c1d84-115">Élément</span><span class="sxs-lookup"><span data-stu-id="c1d84-115">Element</span></span>                                                            | <span data-ttu-id="c1d84-116">Type</span><span class="sxs-lookup"><span data-stu-id="c1d84-116">Type</span></span>                                                                    | <span data-ttu-id="c1d84-117">Description</span><span class="sxs-lookup"><span data-stu-id="c1d84-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="c1d84-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c1d84-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="c1d84-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="c1d84-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="c1d84-120">Spécifie le nom du champ d’en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="c1d84-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="c1d84-121">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c1d84-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="c1d84-122">**string**</span><span class="sxs-lookup"><span data-stu-id="c1d84-122">**string**</span></span>                                                              | <span data-ttu-id="c1d84-123">Spécifie la valeur d’un champ d’en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="c1d84-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="c1d84-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c1d84-124">Remarks</span></span>

<span data-ttu-id="c1d84-125">Pour le développement C++, consultez la [**propriété HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="c1d84-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="c1d84-126">Pour le développement de scripts, consultez [**EmailAction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="c1d84-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d84-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1d84-127">Requirements</span></span>



| <span data-ttu-id="c1d84-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1d84-128">Requirement</span></span> | <span data-ttu-id="c1d84-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1d84-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1d84-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1d84-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d84-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1d84-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1d84-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1d84-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d84-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1d84-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





