---
title: Type complexe headerFieldsType
description: Définit les éléments qui spécifient les champs d’un en-tête de message électronique.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- Planificateur de tâches de type complexe headerFieldsType
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464806"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="b97b7-104">Type complexe headerFieldsType</span><span class="sxs-lookup"><span data-stu-id="b97b7-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="b97b7-105">Définit les éléments qui spécifient les champs d’un en-tête de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b97b7-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b97b7-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b97b7-106">Child elements</span></span>



| <span data-ttu-id="b97b7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="b97b7-107">Element</span></span>                                                                         | <span data-ttu-id="b97b7-108">Type</span><span class="sxs-lookup"><span data-stu-id="b97b7-108">Type</span></span>                                                                       | <span data-ttu-id="b97b7-109">Description</span><span class="sxs-lookup"><span data-stu-id="b97b7-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="b97b7-110">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="b97b7-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="b97b7-111">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="b97b7-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="b97b7-112">Spécifie un champ dans un en-tête de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b97b7-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="b97b7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b97b7-113">Requirements</span></span>



| <span data-ttu-id="b97b7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b97b7-114">Requirement</span></span> | <span data-ttu-id="b97b7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97b7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b97b7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b97b7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b97b7-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b97b7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b97b7-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b97b7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





