---
description: Définit un type de chaîne pour le profil haut débit mobile.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: type simple nameType (haut débit mobile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512989"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="f5997-103">type simple nameType (haut débit mobile)</span><span class="sxs-lookup"><span data-stu-id="f5997-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="f5997-104">Le type simple **NameType** définit un type de chaîne pour le profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="f5997-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="f5997-105">Cette chaîne comporte au moins un caractère et 255 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="f5997-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="f5997-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5997-106">Requirements</span></span>



| <span data-ttu-id="f5997-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5997-107">Requirement</span></span> | <span data-ttu-id="f5997-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5997-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="f5997-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5997-109">Minimum supported client</span></span><br/> | <span data-ttu-id="f5997-110">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f5997-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f5997-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5997-111">Minimum supported server</span></span><br/> | <span data-ttu-id="f5997-112">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5997-112">None supported</span></span><br/>                         |



 

 




