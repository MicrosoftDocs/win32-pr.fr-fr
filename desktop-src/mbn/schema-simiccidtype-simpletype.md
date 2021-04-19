---
description: Définit un type pour l’élément SimIccID du profil haut débit mobile.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Type simple simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544685"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="08250-103">Type simple simIccIDType</span><span class="sxs-lookup"><span data-stu-id="08250-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="08250-104">Le type simple **simIccIDType** définit un type pour l’élément [**SimIccID**](schema-simiccid-mbnprofile-element.md) du profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="08250-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="08250-105">Ce type est une collection de chiffres et/ou de lettres majuscules et minuscules, d’au moins un caractère et d’une longueur maximale de 20 caractères.</span><span class="sxs-lookup"><span data-stu-id="08250-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="08250-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="08250-106">Patterns</span></span>

<span data-ttu-id="08250-107">Le type simple **simIccIDType** est un jeton qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="08250-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="08250-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08250-108">Requirements</span></span>



| <span data-ttu-id="08250-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08250-109">Requirement</span></span> | <span data-ttu-id="08250-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="08250-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="08250-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08250-111">Minimum supported client</span></span><br/> | <span data-ttu-id="08250-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="08250-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="08250-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08250-113">Minimum supported server</span></span><br/> | <span data-ttu-id="08250-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="08250-114">None supported</span></span><br/>                         |



 

 




