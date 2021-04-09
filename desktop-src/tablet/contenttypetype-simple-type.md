---
description: Définit le type qui définit des valeurs valides pour l’attribut de type du lecteur du journal des éléments de contenu \[ \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Type simple ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034666"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="6682b-103">Type simple ContentTypeType</span><span class="sxs-lookup"><span data-stu-id="6682b-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="6682b-104">Définit le type qui définit des valeurs valides pour l’attribut de *type* du [ \[ lecteur \] du journal des éléments de contenu](content-element--journal-reader.md).</span><span class="sxs-lookup"><span data-stu-id="6682b-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="6682b-105">Modèles</span><span class="sxs-lookup"><span data-stu-id="6682b-105">Patterns</span></span>

<span data-ttu-id="6682b-106">Le type simple **ContentTypeType** est une chaîne qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="6682b-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="6682b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6682b-107">Remarks</span></span>

<span data-ttu-id="6682b-108">Les valeurs valides sont « normal » et « inerte ».</span><span class="sxs-lookup"><span data-stu-id="6682b-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="6682b-109">Si le type est « inerte », le contenu contenu est une page de journal qui est l’arrière-plan en lecture seule/non modifiable pour le document.</span><span class="sxs-lookup"><span data-stu-id="6682b-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="6682b-110">Cela se produit lorsqu’un document est créé à l’aide du pilote d’imprimante du rédacteur de note de journal.</span><span class="sxs-lookup"><span data-stu-id="6682b-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="6682b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6682b-111">Requirements</span></span>



| <span data-ttu-id="6682b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6682b-112">Requirement</span></span> | <span data-ttu-id="6682b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6682b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6682b-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6682b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6682b-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6682b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6682b-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6682b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6682b-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6682b-117">None supported</span></span><br/>                                     |



 

 




