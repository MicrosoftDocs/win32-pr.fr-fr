---
title: Type complexe attachmentsType
description: Définit les éléments utilisés pour spécifier une pièce jointe envoyée avec un message électronique.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- Planificateur de tâches de type complexe attachmentsType
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511792"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="db654-104">Type complexe attachmentsType</span><span class="sxs-lookup"><span data-stu-id="db654-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="db654-105">Définit les éléments utilisés pour spécifier une pièce jointe envoyée avec un message électronique.</span><span class="sxs-lookup"><span data-stu-id="db654-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="db654-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="db654-106">Child elements</span></span>



| <span data-ttu-id="db654-107">Élément</span><span class="sxs-lookup"><span data-stu-id="db654-107">Element</span></span>                                                          | <span data-ttu-id="db654-108">Type</span><span class="sxs-lookup"><span data-stu-id="db654-108">Type</span></span>                                                                    | <span data-ttu-id="db654-109">Description</span><span class="sxs-lookup"><span data-stu-id="db654-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db654-110">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="db654-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="db654-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="db654-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="db654-112">Spécifie le chemin d’accès à un fichier qui est envoyé en tant que pièce jointe dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="db654-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="db654-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db654-113">Requirements</span></span>



| <span data-ttu-id="db654-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db654-114">Requirement</span></span> | <span data-ttu-id="db654-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="db654-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db654-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db654-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db654-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db654-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db654-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db654-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db654-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db654-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





