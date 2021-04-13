---
description: Définit un type de chaîne pour l’élément ProviderName dans le profil haut débit mobile.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Type simple providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526020"
---
# <a name="providernametype-simple-type"></a><span data-ttu-id="29e13-103">Type simple providerNameType</span><span class="sxs-lookup"><span data-stu-id="29e13-103">providerNameType Simple Type</span></span>

<span data-ttu-id="29e13-104">Le type simple **providerNameType** définit un type de chaîne pour l’élément [**providerName**](schema-providername-providertype-element.md) dans le profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="29e13-104">The **providerNameType** simple type defines a string type for the [**ProviderName**](schema-providername-providertype-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="29e13-105">Cette chaîne doit comporter au moins un caractère et comporter jusqu’à 20 caractères.</span><span class="sxs-lookup"><span data-stu-id="29e13-105">This string is at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="29e13-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29e13-106">Requirements</span></span>



| <span data-ttu-id="29e13-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29e13-107">Requirement</span></span> | <span data-ttu-id="29e13-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="29e13-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="29e13-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e13-109">Minimum supported client</span></span><br/> | <span data-ttu-id="29e13-110">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="29e13-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="29e13-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e13-111">Minimum supported server</span></span><br/> | <span data-ttu-id="29e13-112">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e13-112">None supported</span></span><br/>                         |



 

 




