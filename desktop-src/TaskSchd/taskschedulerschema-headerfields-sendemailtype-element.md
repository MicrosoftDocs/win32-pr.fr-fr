---
title: Élément HeaderFields (sendEmailType)
description: Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Élément HeaderFields Planificateur de tâches
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508850"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="3431c-104">Élément HeaderFields (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="3431c-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="3431c-105">Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.</span><span class="sxs-lookup"><span data-stu-id="3431c-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="3431c-106">L’élément **HeaderFields** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3431c-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3431c-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="3431c-107">Parent element</span></span>



| <span data-ttu-id="3431c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="3431c-108">Element</span></span>                                                                              | <span data-ttu-id="3431c-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="3431c-109">Derived from</span></span>                                                           | <span data-ttu-id="3431c-110">Description</span><span class="sxs-lookup"><span data-stu-id="3431c-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="3431c-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="3431c-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="3431c-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="3431c-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="3431c-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3431c-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="3431c-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3431c-114">Child elements</span></span>



| <span data-ttu-id="3431c-115">Élément</span><span class="sxs-lookup"><span data-stu-id="3431c-115">Element</span></span>                                                                         | <span data-ttu-id="3431c-116">Type</span><span class="sxs-lookup"><span data-stu-id="3431c-116">Type</span></span>                                                                       | <span data-ttu-id="3431c-117">Description</span><span class="sxs-lookup"><span data-stu-id="3431c-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="3431c-118">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="3431c-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="3431c-119">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="3431c-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="3431c-120">Contient un champ pour un en-tête dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3431c-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="3431c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="3431c-121">Remarks</span></span>

<span data-ttu-id="3431c-122">Pour le développement C++, consultez la [**propriété HeaderFields de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="3431c-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="3431c-123">Pour le développement de scripts, consultez [**EmailAction. HeaderFields**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="3431c-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3431c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3431c-124">Requirements</span></span>



| <span data-ttu-id="3431c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3431c-125">Requirement</span></span> | <span data-ttu-id="3431c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3431c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3431c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3431c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3431c-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3431c-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3431c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3431c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3431c-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3431c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





