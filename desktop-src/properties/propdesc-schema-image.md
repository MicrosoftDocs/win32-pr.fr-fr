---
description: image
ms.assetid: 89893C4E-4F4E-4d85-9623-08607B4383E5
title: image, élément (schéma de description de propriété)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24ecb1b88b8b724ce299a81281f926972180743
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104987"
---
# <a name="image"></a><span data-ttu-id="60c2e-103">image</span><span class="sxs-lookup"><span data-stu-id="60c2e-103">image</span></span>

<span data-ttu-id="60c2e-104">Il ne doit y avoir qu’un seul élément [image]() pour chaque élément parent.</span><span class="sxs-lookup"><span data-stu-id="60c2e-104">There should be only one [image]() element for each parent element.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c2e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60c2e-105">Syntax</span></span>


```
<!-- image -->
<xs:element name="image">
    <xs:complexType>
        <xs:attribute name="res" use="required">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:maxLength value="260"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="60c2e-106">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="60c2e-106">Element Information</span></span>



| <span data-ttu-id="60c2e-107">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="60c2e-107">Parent Elements</span></span>                                                                  | <span data-ttu-id="60c2e-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="60c2e-108">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| <span data-ttu-id="60c2e-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="60c2e-109">[enum](./propdesc-schema-enum.md), [enumRange](./propdesc-schema-enumrange.md)</span></span> | <span data-ttu-id="60c2e-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="60c2e-110">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="60c2e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="60c2e-111">Attributes</span></span>



| <span data-ttu-id="60c2e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="60c2e-112">Attribute</span></span> | <span data-ttu-id="60c2e-113">Description</span><span class="sxs-lookup"><span data-stu-id="60c2e-113">Description</span></span>       |
|-----------|-------------------|
| <span data-ttu-id="60c2e-114">res</span><span class="sxs-lookup"><span data-stu-id="60c2e-114">res</span></span>       | <span data-ttu-id="60c2e-115">Public.</span><span class="sxs-lookup"><span data-stu-id="60c2e-115">Public.</span></span> <span data-ttu-id="60c2e-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="60c2e-116">Required.</span></span> |



 

 

 
