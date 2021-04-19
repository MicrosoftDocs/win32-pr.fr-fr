---
title: Type complexe UserDataType
description: Définit un fragment XML qui spécifie la disposition des données d’événement.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- UserDataType type complexe EventLog
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106544163"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="0975e-104">Type complexe UserDataType</span><span class="sxs-lookup"><span data-stu-id="0975e-104">UserDataType Complex Type</span></span>

<span data-ttu-id="0975e-105">Définit un fragment XML qui spécifie la disposition des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="0975e-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="0975e-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0975e-106">Requirements</span></span>



| <span data-ttu-id="0975e-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0975e-107">Requirement</span></span> | <span data-ttu-id="0975e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="0975e-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0975e-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0975e-109">Minimum supported client</span></span><br/> | <span data-ttu-id="0975e-110">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0975e-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0975e-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0975e-111">Minimum supported server</span></span><br/> | <span data-ttu-id="0975e-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0975e-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





