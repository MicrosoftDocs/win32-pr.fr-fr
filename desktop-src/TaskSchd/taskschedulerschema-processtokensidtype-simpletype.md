---
title: Type simple processTokenSidType
description: Définit les valeurs possibles pour l’élément ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Planificateur de tâches de type simple processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384355"
---
# <a name="processtokensidtype-simple-type"></a><span data-ttu-id="843eb-104">Type simple processTokenSidType</span><span class="sxs-lookup"><span data-stu-id="843eb-104">processTokenSidType Simple Type</span></span>

<span data-ttu-id="843eb-105">Définit les valeurs possibles pour l’élément [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="843eb-105">Defines the possible values for the [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="843eb-106">Valeurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="843eb-106">Enumeration values</span></span>

<span data-ttu-id="843eb-107">Le type simple **processTokenSidType** définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="843eb-107">The **processTokenSidType** simple type defines the following values.</span></span>



| <span data-ttu-id="843eb-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="843eb-108">Value</span></span>        | <span data-ttu-id="843eb-109">Description</span><span class="sxs-lookup"><span data-stu-id="843eb-109">Description</span></span>                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="843eb-110">Aucune</span><span class="sxs-lookup"><span data-stu-id="843eb-110">None</span></span>         | <span data-ttu-id="843eb-111">Les tâches sont exécutées dans un processus qui ne contient pas de SID de jeton de processus (aucune modification n’est apportée à la liste des groupes de jetons de processus).</span><span class="sxs-lookup"><span data-stu-id="843eb-111">Tasks are run in a process that does not contain a process token SID (no changes will be made to the process token groups list).</span></span><br/> |
| <span data-ttu-id="843eb-112">Non restreint</span><span class="sxs-lookup"><span data-stu-id="843eb-112">Unrestricted</span></span> | <span data-ttu-id="843eb-113">Un SID de tâche est dérivé du chemin d’accès complet à la tâche et est ajouté à la liste des groupes de jetons de processus.</span><span class="sxs-lookup"><span data-stu-id="843eb-113">A task SID will be derived from the full task path and will be added to the process token groups list.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="843eb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="843eb-114">Requirements</span></span>



| <span data-ttu-id="843eb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="843eb-115">Requirement</span></span> | <span data-ttu-id="843eb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="843eb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="843eb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="843eb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="843eb-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="843eb-118">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="843eb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="843eb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="843eb-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="843eb-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





