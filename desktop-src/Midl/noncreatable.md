---
title: noncreatable (attribut)
description: L’attribut \ noncreatable \ définit un objet qui ne peut pas être instancié par lui-même.
ms.assetid: 75d7b978-0f82-4e8a-89c2-ffd5b9a691d6
keywords:
- MIDL d’attribut noncreatable
topic_type:
- apiref
api_name:
- noncreatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2aa54be3416087c06651a4bb58902a0469e8f0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314808"
---
# <a name="noncreatable-attribute"></a><span data-ttu-id="6fd57-104">noncreatable (attribut)</span><span class="sxs-lookup"><span data-stu-id="6fd57-104">noncreatable attribute</span></span>

<span data-ttu-id="6fd57-105">L’attribut **\[ noncreatable \]** définit un objet qui ne peut pas être instancié par lui-même.</span><span class="sxs-lookup"><span data-stu-id="6fd57-105">The **\[noncreatable\]** attribute defines an object that cannot be instantiated by itself.</span></span>

``` syntax
[
  coclass-attribute-list, 
    noncreatable
]
coclass coclass-name
{
  coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="6fd57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fd57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd57-107">*coclass-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="6fd57-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd57-108">Autres attributs qui s’appliquent à la classe.</span><span class="sxs-lookup"><span data-stu-id="6fd57-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="6fd57-109">*nom de la coclasse*</span><span class="sxs-lookup"><span data-stu-id="6fd57-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd57-110">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="6fd57-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="6fd57-111">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="6fd57-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6fd57-112">Liste des interfaces pour la classe.</span><span class="sxs-lookup"><span data-stu-id="6fd57-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fd57-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6fd57-113">Remarks</span></span>

<span data-ttu-id="6fd57-114">Utilisez l’attribut **\[ noncreatable \]** sur une instruction [**coclass**](coclass.md) pour indiquer aux utilisateurs qu’ils ne peuvent pas créer un nouvel objet de cette classe au niveau supérieur, c’est-à-dire en appelant **CreateInstance** ou **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="6fd57-114">Use the **\[noncreatable\]** attribute on a [**coclass**](coclass.md) statement to indicate to users that they cannot create a new object of this class at the top level—that is, by calling **CreateInstance** or **CoCreateInstance**.</span></span> <span data-ttu-id="6fd57-115">L’instanciation d’un objet de cette classe requiert un appel de méthode à un autre objet.</span><span class="sxs-lookup"><span data-stu-id="6fd57-115">Instantiation of an object of this class requires a method call to another object.</span></span> <span data-ttu-id="6fd57-116">Par exemple, dans Microsoft Excel, l’objet « Cell » ne peut pas être créé et doit être obtenu à partir d’un objet de feuille de calcul Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6fd57-116">For example, in Microsoft Excel, the "Cell" object is noncreatable and must be obtained from a Microsoft Excel Worksheet object.</span></span>

<span data-ttu-id="6fd57-117">Les méthodes qui retournent des instances de classes pouvant être créées doivent retourner le type exact de l’objet, plutôt que des types **Variant** ou **IDispatch** \* .</span><span class="sxs-lookup"><span data-stu-id="6fd57-117">Methods that return instances of noncreatable classes should return the exact type of the object, rather than **VARIANT** or **IDispatch**\* types.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="6fd57-118">Représentation TYPEFLAG :</span><span class="sxs-lookup"><span data-stu-id="6fd57-118">Typeflag Representation:</span></span>

<span data-ttu-id="6fd57-119">Absence de FCANCREATE TYPEFLAG \_ .</span><span class="sxs-lookup"><span data-stu-id="6fd57-119">The absence of TYPEFLAG\_FCANCREATE.</span></span>

## <a name="examples"></a><span data-ttu-id="6fd57-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="6fd57-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is MyCOClass"),
    noncreatable
]
coclass MyCoClass
{
    [default] interface IMyClass;
    [default, source] dispinterface IMyClassEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="6fd57-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fd57-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd57-122">**coclasse**</span><span class="sxs-lookup"><span data-stu-id="6fd57-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="6fd57-123">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="6fd57-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6fd57-124">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="6fd57-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6fd57-125">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="6fd57-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 