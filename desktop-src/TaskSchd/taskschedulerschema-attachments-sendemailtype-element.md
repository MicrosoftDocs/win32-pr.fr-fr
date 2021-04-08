---
title: Élément Attachments (sendEmailType)
description: Contient une liste de pièces jointes dans le message électronique.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Élément Attachments Planificateur de tâches
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742772"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="0c258-104">Élément Attachments (sendEmailType)</span><span class="sxs-lookup"><span data-stu-id="0c258-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="0c258-105">Contient une liste de pièces jointes dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="0c258-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="0c258-106">L’élément **Attachments** est défini par le type complexe [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0c258-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0c258-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0c258-107">Parent element</span></span>



| <span data-ttu-id="0c258-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0c258-108">Element</span></span>                                                                              | <span data-ttu-id="0c258-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="0c258-109">Derived from</span></span>                                                           | <span data-ttu-id="0c258-110">Description</span><span class="sxs-lookup"><span data-stu-id="0c258-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="0c258-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="0c258-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="0c258-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="0c258-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="0c258-113">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="0c258-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0c258-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c258-114">Child elements</span></span>



| <span data-ttu-id="0c258-115">Élément</span><span class="sxs-lookup"><span data-stu-id="0c258-115">Element</span></span>                                                          | <span data-ttu-id="0c258-116">Type</span><span class="sxs-lookup"><span data-stu-id="0c258-116">Type</span></span>                                                                    | <span data-ttu-id="0c258-117">Description</span><span class="sxs-lookup"><span data-stu-id="0c258-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c258-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0c258-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="0c258-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="0c258-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="0c258-120">Spécifie le chemin d’accès à un fichier qui est envoyé en tant que pièce jointe dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="0c258-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0c258-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0c258-121">Remarks</span></span>

<span data-ttu-id="0c258-122">Pour le développement C++, consultez la [**propriété Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="0c258-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="0c258-123">Pour le développement de scripts, consultez [**EmailAction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="0c258-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c258-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c258-124">Requirements</span></span>



| <span data-ttu-id="0c258-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c258-125">Requirement</span></span> | <span data-ttu-id="0c258-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c258-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c258-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c258-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0c258-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c258-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c258-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c258-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0c258-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c258-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





