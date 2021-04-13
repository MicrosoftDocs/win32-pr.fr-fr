---
title: Élément EventRecordID (SystemPropertiesType)
description: Numéro d’enregistrement affecté à l’événement lorsqu’il a été enregistré.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- EventLog, élément EventRecordID
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384008"
---
# <a name="eventrecordid-systempropertiestype-element"></a><span data-ttu-id="d87b2-104">Élément EventRecordID (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="d87b2-104">EventRecordID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="d87b2-105">Numéro d’enregistrement affecté à l’événement lorsqu’il a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="d87b2-105">The record number assigned to the event when it was logged.</span></span>

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d87b2-106">L’élément **EventRecordID** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d87b2-106">The **EventRecordID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87b2-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d87b2-107">Requirements</span></span>



| <span data-ttu-id="d87b2-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d87b2-108">Requirement</span></span> | <span data-ttu-id="d87b2-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d87b2-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d87b2-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d87b2-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d87b2-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d87b2-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d87b2-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d87b2-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d87b2-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d87b2-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





