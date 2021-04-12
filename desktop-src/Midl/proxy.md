---
title: attribut de proxy
description: L’attribut \ proxy \ empêche Automation de s’inscrire en tant que gestionnaire proxy/stub pour une interface double.
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- MIDL, attribut de proxy
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa8c9d305b7f51a012ae26d7b1a76d2e3011fd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462966"
---
# <a name="proxy-attribute"></a><span data-ttu-id="a94ee-104">attribut de proxy</span><span class="sxs-lookup"><span data-stu-id="a94ee-104">proxy attribute</span></span>

<span data-ttu-id="a94ee-105">L’attribut **\[ proxy \]** empêche l’inscription de l’Automation en tant que gestionnaire proxy/stub pour une interface double.</span><span class="sxs-lookup"><span data-stu-id="a94ee-105">The **\[proxy\]** attribute prevents Automation from registering as a proxy/stub handler for a dual interface.</span></span>

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="a94ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a94ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94ee-107">*chaîne-UUID*</span><span class="sxs-lookup"><span data-stu-id="a94ee-107">*string-uuid*</span></span> 
</dt> <dd>

<span data-ttu-id="a94ee-108">Spécifie une chaîne composée de 8 chiffres hexadécimaux suivis d’un trait d’Union, puis trois groupes de 4 chiffres hexadécimaux chacun suivi d’un trait d’Union, puis 12 chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="a94ee-108">Specifies a string consisting of 8 hexadecimal digits followed by a hyphen, then three groups of 4 hexadecimal digits each followed by a hyphen, then 12 hexadecimal digits.</span></span> <span data-ttu-id="a94ee-109">Vous pouvez placer la chaîne UUID entre guillemets, sauf si vous utilisez le commutateur de compilateur MIDL [**/OSF**](-osf.md).</span><span class="sxs-lookup"><span data-stu-id="a94ee-109">You can enclose the UUID string in quotes, except when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

</dd> <dt>

<span data-ttu-id="a94ee-110">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="a94ee-110">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a94ee-111">Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a94ee-111">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="a94ee-112">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="a94ee-112">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="a94ee-113">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="a94ee-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a94ee-114">Nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a94ee-114">Name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a94ee-115">*interface de base*</span><span class="sxs-lookup"><span data-stu-id="a94ee-115">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="a94ee-116">Spécifie le nom d’une interface à partir de laquelle cette interface dérivée hérite des fonctions membres, des codes d’État et des attributs d’interface.</span><span class="sxs-lookup"><span data-stu-id="a94ee-116">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="a94ee-117">L’interface dérivée n’hérite pas des définitions de type.</span><span class="sxs-lookup"><span data-stu-id="a94ee-117">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="a94ee-118">Pour ce faire, utilisez le mot clé [**Import**](import.md) pour importer le fichier IDL de l’interface de base.</span><span class="sxs-lookup"><span data-stu-id="a94ee-118">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a94ee-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a94ee-119">Remarks</span></span>

<span data-ttu-id="a94ee-120">L’utilisation \[  \] de l’attribut proxy pour une interface double empêche le TLB de prendre en charge des stubs générés.</span><span class="sxs-lookup"><span data-stu-id="a94ee-120">Using the \[ **proxy**\] attribute for a dual interface prevents the TLB from taking over generated stubs.</span></span> <span data-ttu-id="a94ee-121">Si cet attribut est spécifié, le proxy de TypeLib ne doit pas être désinscrit lorsque la TypeLib est désinscrite.</span><span class="sxs-lookup"><span data-stu-id="a94ee-121">If this attribute is specified, the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

### <a name="flags"></a><span data-ttu-id="a94ee-122">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="a94ee-122">Flags</span></span>

<dl> <dt>

<span data-ttu-id="a94ee-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>\_proxy TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="a94ee-123"><span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="a94ee-124">Les interfaces peuvent être marquées avec l' \_ indicateur de proxy TYPEFLAG pour indiquer qu’elles utiliseront une bibliothèque de liens dynamiques proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="a94ee-124">Interfaces can be marked with the TYPEFLAG\_PROXY flag to indicate they will be using a proxy/stub dynamic link library.</span></span> <span data-ttu-id="a94ee-125">Cet indicateur spécifie que le proxy de TypeLib ne doit pas être désinscrit lorsque la TypeLib est désinscrite.</span><span class="sxs-lookup"><span data-stu-id="a94ee-125">This flag specifies the typelib proxy should not be unregistered when the typelib is unregistered.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a94ee-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a94ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94ee-127">**Génération d’une bibliothèque de types avec MIDL**</span><span class="sxs-lookup"><span data-stu-id="a94ee-127">**Generating a Type Library with MIDL**</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="a94ee-128">**double**</span><span class="sxs-lookup"><span data-stu-id="a94ee-128">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="a94ee-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a94ee-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 