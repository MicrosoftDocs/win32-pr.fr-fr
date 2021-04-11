---
title: aggregatable (attribut)
description: L’attribut \ Aggregatable \ indique que la classe prend en charge l’agrégation.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- MIDL d’attribut agrégeables
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314843"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="57bd6-104">aggregatable (attribut)</span><span class="sxs-lookup"><span data-stu-id="57bd6-104">aggregatable attribute</span></span>

<span data-ttu-id="57bd6-105">L’attribut **\[ agrégeables \]** indique que la classe prend en charge l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="57bd6-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="57bd6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57bd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57bd6-107">*coclass-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="57bd6-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="57bd6-108">Autres attributs qui s’appliquent à la classe.</span><span class="sxs-lookup"><span data-stu-id="57bd6-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="57bd6-109">*nom de la coclasse*</span><span class="sxs-lookup"><span data-stu-id="57bd6-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="57bd6-110">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="57bd6-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="57bd6-111">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="57bd6-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="57bd6-112">Liste des interfaces pour la classe.</span><span class="sxs-lookup"><span data-stu-id="57bd6-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57bd6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="57bd6-113">Remarks</span></span>

<span data-ttu-id="57bd6-114">Utilisez l’attribut **\[ agrégeables \]** sur une instruction [**coclass**](coclass.md) pour permettre aux utilisateurs de savoir que la classe prend en charge les agrégations.</span><span class="sxs-lookup"><span data-stu-id="57bd6-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="57bd6-115">Autrement dit, la classe autorise l’exposition de ses interfaces par une classe de conteneur comme si ces interfaces étaient les propres interfaces du conteneur.</span><span class="sxs-lookup"><span data-stu-id="57bd6-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="57bd6-116">La représentation TYPEFLAG de cet attribut est TYPEFLAG \_ FAGGREGATABLE.</span><span class="sxs-lookup"><span data-stu-id="57bd6-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="57bd6-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="57bd6-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="57bd6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57bd6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57bd6-119">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="57bd6-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="57bd6-120">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="57bd6-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="57bd6-121">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="57bd6-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="57bd6-122">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="57bd6-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 