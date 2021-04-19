---
description: Définit le type utilisé pour spécifier des valeurs valides pour la couleur de certains éléments dans un fichier journal XML.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Type simple ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513349"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="8d403-103">Type simple ColorType</span><span class="sxs-lookup"><span data-stu-id="8d403-103">ColorType Simple Type</span></span>

<span data-ttu-id="8d403-104">Définit le type utilisé pour spécifier des valeurs valides pour la couleur de certains éléments dans un fichier journal XML.</span><span class="sxs-lookup"><span data-stu-id="8d403-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="8d403-105">Notes</span><span class="sxs-lookup"><span data-stu-id="8d403-105">Remarks</span></span>

<span data-ttu-id="8d403-106">Une couleur peut être une valeur RVB hexadécimale au format \# RRGGBB.</span><span class="sxs-lookup"><span data-stu-id="8d403-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="8d403-107">Il doit correspondre à l’expression régulière suivante : \# \[ 0-9A-FA-F \] {6} .</span><span class="sxs-lookup"><span data-stu-id="8d403-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="8d403-108">Par exemple : « \# 4a79B5 ».</span><span class="sxs-lookup"><span data-stu-id="8d403-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="8d403-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d403-109">Requirements</span></span>



| <span data-ttu-id="8d403-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d403-110">Requirement</span></span> | <span data-ttu-id="8d403-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d403-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8d403-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d403-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8d403-113">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d403-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d403-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d403-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8d403-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d403-115">None supported</span></span><br/>                                     |



 

 




