---
title: attribut DllName (STR)
description: L’attribut \ DllName \ définit le nom de la DLL qui contient les points d’entrée d’un module.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- attribut DllName (STR) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031225"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="493bb-104">attribut DllName (STR)</span><span class="sxs-lookup"><span data-stu-id="493bb-104">dllname(str) attribute</span></span>

<span data-ttu-id="493bb-105">L’attribut **\[ DllName \]** définit le nom de la dll qui contient les points d’entrée d’un module.</span><span class="sxs-lookup"><span data-stu-id="493bb-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="493bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="493bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="493bb-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="493bb-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="493bb-108">Spécifie un numéro d’identification unique universel pour le [**module**](module.md).</span><span class="sxs-lookup"><span data-stu-id="493bb-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="493bb-109">*extension*</span><span class="sxs-lookup"><span data-stu-id="493bb-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="493bb-110">Spécifie une chaîne terminée par le caractère NULL qui contient le chemin d’accès complet au fichier dll.</span><span class="sxs-lookup"><span data-stu-id="493bb-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="493bb-111">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="493bb-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="493bb-112">Spécifie une liste de zéro, un ou plusieurs attributs d’interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="493bb-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="493bb-113">*NomModule*</span><span class="sxs-lookup"><span data-stu-id="493bb-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="493bb-114">Spécifie le nom que d’autres composants logiciels peuvent utiliser pour faire référence au module.</span><span class="sxs-lookup"><span data-stu-id="493bb-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="493bb-115">*elementlist*</span><span class="sxs-lookup"><span data-stu-id="493bb-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="493bb-116">Spécifie une ou plusieurs instructions de définition d’élément de module.</span><span class="sxs-lookup"><span data-stu-id="493bb-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="493bb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="493bb-117">Remarks</span></span>

<span data-ttu-id="493bb-118">L’attribut **\[ DllName \]** est requis sur un module.</span><span class="sxs-lookup"><span data-stu-id="493bb-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="493bb-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="493bb-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="493bb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="493bb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493bb-121">**modules**</span><span class="sxs-lookup"><span data-stu-id="493bb-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="493bb-122">**mention**</span><span class="sxs-lookup"><span data-stu-id="493bb-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="493bb-123">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="493bb-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="493bb-124">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="493bb-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="493bb-125">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="493bb-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 