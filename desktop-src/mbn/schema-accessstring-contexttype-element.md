---
description: Identifie l’APN ou la chaîne de numérotation à utiliser pour établir une connexion de données.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Élément AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543459"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="e7f16-103">Élément AccessString (contextType)</span><span class="sxs-lookup"><span data-stu-id="e7f16-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="e7f16-104">L’élément **AccessString (ContextType)** identifie le APN ou la chaîne de numérotation à utiliser pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="e7f16-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="e7f16-105">Cet élément peut avoir une longueur maximale de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="e7f16-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="e7f16-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e7f16-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e7f16-107">L’élément **AccessString** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e7f16-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f16-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f16-108">Requirements</span></span>



| <span data-ttu-id="e7f16-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f16-109">Requirement</span></span> | <span data-ttu-id="e7f16-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f16-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="e7f16-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f16-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f16-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e7f16-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e7f16-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f16-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f16-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f16-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e7f16-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f16-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7f16-116">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="e7f16-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e7f16-117">**contextType**</span><span class="sxs-lookup"><span data-stu-id="e7f16-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="e7f16-118">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="e7f16-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e7f16-119">**Contexte (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="e7f16-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




