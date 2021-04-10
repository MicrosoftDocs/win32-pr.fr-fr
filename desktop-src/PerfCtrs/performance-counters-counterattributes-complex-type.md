---
description: Définit une liste qui contient jusqu’à cinq attributs de compteur.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Type complexe counterAttributes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952004"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="c3d55-103">Type complexe counterAttributes</span><span class="sxs-lookup"><span data-stu-id="c3d55-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="c3d55-104">Définit une liste qui contient jusqu’à cinq attributs de compteur.</span><span class="sxs-lookup"><span data-stu-id="c3d55-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c3d55-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c3d55-105">Child elements</span></span>



| <span data-ttu-id="c3d55-106">Élément</span><span class="sxs-lookup"><span data-stu-id="c3d55-106">Element</span></span>              | <span data-ttu-id="c3d55-107">Type</span><span class="sxs-lookup"><span data-stu-id="c3d55-107">Type</span></span>                                                                               | <span data-ttu-id="c3d55-108">Description</span><span class="sxs-lookup"><span data-stu-id="c3d55-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d55-109">**counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="c3d55-109">**counterAttribute**</span></span> | [<span data-ttu-id="c3d55-110">**homme : counterAttribute**</span><span class="sxs-lookup"><span data-stu-id="c3d55-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="c3d55-111">Attribut de compteur qui spécifie le mode d’affichage des données de compteur dans une application consommateur.</span><span class="sxs-lookup"><span data-stu-id="c3d55-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c3d55-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3d55-112">Requirements</span></span>



| <span data-ttu-id="c3d55-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3d55-113">Requirement</span></span> | <span data-ttu-id="c3d55-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3d55-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3d55-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d55-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d55-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3d55-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3d55-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3d55-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d55-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3d55-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




