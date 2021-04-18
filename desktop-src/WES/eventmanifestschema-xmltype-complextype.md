---
title: Type complexe XmlType
description: Définit un fragment XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Type complexe XmlType journal des événements
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384620"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="01baa-104">Type complexe XmlType</span><span class="sxs-lookup"><span data-stu-id="01baa-104">XmlType Complex Type</span></span>

<span data-ttu-id="01baa-105">Définit un fragment XML.</span><span class="sxs-lookup"><span data-stu-id="01baa-105">Defines an XML fragment.</span></span> <span data-ttu-id="01baa-106">Toute instance de schéma est autorisée ; le nœud de niveau supérieur du fragment doit contenir un attribut d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="01baa-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="01baa-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01baa-107">Requirements</span></span>



| <span data-ttu-id="01baa-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01baa-108">Requirement</span></span> | <span data-ttu-id="01baa-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="01baa-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01baa-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01baa-110">Minimum supported client</span></span><br/> | <span data-ttu-id="01baa-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01baa-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01baa-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01baa-112">Minimum supported server</span></span><br/> | <span data-ttu-id="01baa-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01baa-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





