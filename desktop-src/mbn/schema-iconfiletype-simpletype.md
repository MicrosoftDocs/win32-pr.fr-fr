---
description: Définit un type de chaîne pour l’élément ICONFilePath dans le profil haut débit mobile.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Type simple iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112898"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="c4b57-103">Type simple iconFileType</span><span class="sxs-lookup"><span data-stu-id="c4b57-103">iconFileType Simple Type</span></span>

<span data-ttu-id="c4b57-104">Le type simple **iconFileType** définit un type de chaîne pour l’élément [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) dans le profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="c4b57-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="c4b57-105">Cette chaîne comporte au moins un caractère et 1024 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="c4b57-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="c4b57-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4b57-106">Requirements</span></span>



| <span data-ttu-id="c4b57-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4b57-107">Requirement</span></span> | <span data-ttu-id="c4b57-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4b57-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c4b57-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4b57-109">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b57-110">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c4b57-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c4b57-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4b57-111">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b57-112">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4b57-112">None supported</span></span><br/>                         |



 

 




