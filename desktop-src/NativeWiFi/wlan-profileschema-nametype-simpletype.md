---
description: Contient le nom ou la description d’un profil de réseau local sans fil.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Type simple nameType (LAN_policy) (profil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106541806"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a><span data-ttu-id="fca26-103">Type simple nameType (LAN_policy) pour profileschema</span><span class="sxs-lookup"><span data-stu-id="fca26-103">nameType Simple Type (LAN_policy) for profileschema</span></span>

<span data-ttu-id="fca26-104">Le type simple nameType peut contenir le nom ou une description d’un profil de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="fca26-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="fca26-105">Cette valeur de chaîne doit être comprise entre 1 et 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="fca26-105">This string value must be between 1 and 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
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

## <a name="requirements"></a><span data-ttu-id="fca26-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fca26-106">Requirements</span></span>



| <span data-ttu-id="fca26-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fca26-107">Requirement</span></span> | <span data-ttu-id="fca26-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="fca26-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fca26-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fca26-109">Minimum supported client</span></span><br/> | <span data-ttu-id="fca26-110">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fca26-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fca26-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fca26-111">Minimum supported server</span></span><br/> | <span data-ttu-id="fca26-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fca26-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fca26-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fca26-113">Redistributable</span></span><br/>          | <span data-ttu-id="fca26-114">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="fca26-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




