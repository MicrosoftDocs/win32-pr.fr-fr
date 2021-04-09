---
description: Définit un type pour l’élément abonné du profil haut débit mobile.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Type simple subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033959"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="a96b2-103">Type simple subscriberIdType</span><span class="sxs-lookup"><span data-stu-id="a96b2-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="a96b2-104">Le type simple **subscriberIdType** définit un type pour l’élément [**abonné**](schema-subscriberid-mbnprofile-element.md) du profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="a96b2-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="a96b2-105">Ce type est une collection d’un ou de plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="a96b2-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="a96b2-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a96b2-106">Requirements</span></span>



| <span data-ttu-id="a96b2-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a96b2-107">Requirement</span></span> | <span data-ttu-id="a96b2-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a96b2-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a96b2-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a96b2-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a96b2-110">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a96b2-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a96b2-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a96b2-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a96b2-112">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a96b2-112">None supported</span></span><br/>                         |



 

 




