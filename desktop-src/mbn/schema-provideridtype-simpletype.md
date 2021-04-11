---
description: Définit un type pour l’élément ProviderID du profil haut débit mobile.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Type simple providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112891"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="9d06b-103">Type simple providerIdType</span><span class="sxs-lookup"><span data-stu-id="9d06b-103">providerIdType Simple Type</span></span>

<span data-ttu-id="9d06b-104">Le type simple **providerIdType** définit un type pour l’élément [**ProviderID**](schema-providerid-providertype-element.md) du profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="9d06b-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="9d06b-105">Ce type est une collection de chiffres d’au moins un chiffre long et de 6 chiffres au maximum.</span><span class="sxs-lookup"><span data-stu-id="9d06b-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="9d06b-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="9d06b-106">Patterns</span></span>

<span data-ttu-id="9d06b-107">Le type simple **providerIdType** est un jeton qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="9d06b-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="9d06b-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d06b-108">Requirements</span></span>



| <span data-ttu-id="9d06b-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d06b-109">Requirement</span></span> | <span data-ttu-id="9d06b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d06b-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="9d06b-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d06b-111">Minimum supported client</span></span><br/> | <span data-ttu-id="9d06b-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9d06b-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="9d06b-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d06b-113">Minimum supported server</span></span><br/> | <span data-ttu-id="9d06b-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d06b-114">None supported</span></span><br/>                         |



 

 




