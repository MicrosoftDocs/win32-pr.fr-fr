---
title: nonbrowsable (attribut)
description: Utilisez l’attribut \ non Browsable \ pour baliser une interface ou un membre dispinterface qui ne doit pas être affiché dans un Explorateur de propriétés.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- MIDL d’attribut ne pouvant être exploré
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940889"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="89295-104">nonbrowsable (attribut)</span><span class="sxs-lookup"><span data-stu-id="89295-104">nonbrowsable attribute</span></span>

<span data-ttu-id="89295-105">Utilisez l’attribut non **\[ navigable \]** pour baliser une interface ou un membre dispinterface qui ne doit pas être affiché dans un Explorateur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="89295-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="89295-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89295-107">*property-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="89295-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="89295-108">Autres attributs qui s’appliquent à la propriété.</span><span class="sxs-lookup"><span data-stu-id="89295-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="89295-109">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="89295-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="89295-110">Type des données retournées par la méthode.</span><span class="sxs-lookup"><span data-stu-id="89295-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="89295-111">*nom de la propriété*</span><span class="sxs-lookup"><span data-stu-id="89295-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="89295-112">Nom de la propriété ou de la méthode.</span><span class="sxs-lookup"><span data-stu-id="89295-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="89295-113">*prop-param-List*</span><span class="sxs-lookup"><span data-stu-id="89295-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="89295-114">Zéro, un ou plusieurs paramètres à passer à la méthode.</span><span class="sxs-lookup"><span data-stu-id="89295-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89295-115">Notes</span><span class="sxs-lookup"><span data-stu-id="89295-115">Remarks</span></span>

<span data-ttu-id="89295-116">Certaines propriétés ne doivent pas être affichées dans un Explorateur de propriétés.</span><span class="sxs-lookup"><span data-stu-id="89295-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="89295-117">Cela peut être dû au fait que la récupération de la valeur prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="89295-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="89295-118">L’exemple empêche l’utilisateur de tenter de récupérer la propriété *Count* , qui retourne le nombre de lignes dans la feuille de réponse dynamique. Ce nombre peut représenter les résultats d’une requête très volumineuse.</span><span class="sxs-lookup"><span data-stu-id="89295-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="89295-119">D’autres propriétés peuvent avoir des effets inattendus sur le navigateur.</span><span class="sxs-lookup"><span data-stu-id="89295-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="89295-120">Par exemple, considérez un contrôle avec la propriété « IsSelected » pour indiquer si le contrôle est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="89295-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="89295-121">Si « IsSelected » est défini sur false, un navigateur de propriétés basé sur une sélection parcourt un autre objet.</span><span class="sxs-lookup"><span data-stu-id="89295-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="89295-122">Notez qu’une propriété marquée comme non **\[ consultable \]** apparaît toujours dans un Explorateur d’objets, qui n’affiche pas les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="89295-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="89295-123">Représentation TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="89295-123">Typeflag Representation</span></span>

<span data-ttu-id="89295-124">Présence de FUNCFLAG \_ FNONBROWSABLE ou VARFLAG \_ FNONBROWSABLE.</span><span class="sxs-lookup"><span data-stu-id="89295-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="89295-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="89295-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="89295-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89295-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89295-127">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="89295-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="89295-128">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="89295-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="89295-129">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="89295-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 