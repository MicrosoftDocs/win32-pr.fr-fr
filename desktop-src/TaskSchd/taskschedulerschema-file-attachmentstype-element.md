---
title: Élément file (attachmentsType)
description: Contient le chemin d’accès à un fichier envoyé sous forme de pièce jointe dans un message électronique.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Élément file Planificateur de tâches
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384363"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="7835b-104">Élément file (attachmentsType)</span><span class="sxs-lookup"><span data-stu-id="7835b-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="7835b-105">Contient le chemin d’accès à un fichier envoyé sous forme de pièce jointe dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="7835b-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="7835b-106">L’élément **file** est défini par le type complexe [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7835b-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7835b-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7835b-107">Parent element</span></span>



| <span data-ttu-id="7835b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7835b-108">Element</span></span>                                                                                      | <span data-ttu-id="7835b-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="7835b-109">Derived from</span></span>                                                               | <span data-ttu-id="7835b-110">Description</span><span class="sxs-lookup"><span data-stu-id="7835b-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="7835b-111">**Pièces jointes (sendEmailType)**</span><span class="sxs-lookup"><span data-stu-id="7835b-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="7835b-112">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="7835b-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="7835b-113">Contient une liste de pièces jointes dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="7835b-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7835b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7835b-114">Remarks</span></span>

<span data-ttu-id="7835b-115">Pour le développement C++, consultez la [**propriété Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="7835b-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="7835b-116">Pour le développement de scripts, consultez [**EmailAction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="7835b-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7835b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7835b-117">Requirements</span></span>



| <span data-ttu-id="7835b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7835b-118">Requirement</span></span> | <span data-ttu-id="7835b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7835b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7835b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7835b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7835b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7835b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7835b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7835b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7835b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7835b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





