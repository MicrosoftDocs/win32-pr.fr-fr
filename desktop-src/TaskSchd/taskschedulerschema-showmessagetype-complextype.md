---
title: Type complexe showMessageType
description: Définit les éléments qui représentent une action qui affiche une boîte de message.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- Planificateur de tâches de type complexe showMessageType
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942420"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="60080-104">Type complexe showMessageType</span><span class="sxs-lookup"><span data-stu-id="60080-104">showMessageType Complex Type</span></span>

<span data-ttu-id="60080-105">Définit les éléments qui représentent une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="60080-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="60080-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="60080-106">Child elements</span></span>



| <span data-ttu-id="60080-107">Élément</span><span class="sxs-lookup"><span data-stu-id="60080-107">Element</span></span>                                                            | <span data-ttu-id="60080-108">Type</span><span class="sxs-lookup"><span data-stu-id="60080-108">Type</span></span>           | <span data-ttu-id="60080-109">Description</span><span class="sxs-lookup"><span data-stu-id="60080-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="60080-110">**Corps**</span><span class="sxs-lookup"><span data-stu-id="60080-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="60080-111">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="60080-111">nonEmptyString</span></span> | <span data-ttu-id="60080-112">Spécifie le texte à afficher dans le corps de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="60080-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="60080-113">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="60080-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="60080-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="60080-114">nonEmptyString</span></span> | <span data-ttu-id="60080-115">Spécifie le titre de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="60080-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="60080-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60080-116">Requirements</span></span>



| <span data-ttu-id="60080-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60080-117">Requirement</span></span> | <span data-ttu-id="60080-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="60080-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60080-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60080-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60080-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60080-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60080-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60080-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60080-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60080-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





