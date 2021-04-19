---
title: requestedit (attribut)
description: L’attribut \ modification \ indique que la propriété prend en charge la notification OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- MIDL de l’attribut modification
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106536888"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="180ab-104">requestedit (attribut)</span><span class="sxs-lookup"><span data-stu-id="180ab-104">requestedit attribute</span></span>

<span data-ttu-id="180ab-105">L’attribut **\[ \] modification** indique que la propriété prend en charge la notification **OnRequestEdit** .</span><span class="sxs-lookup"><span data-stu-id="180ab-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="180ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="180ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="180ab-107">*attributs facultatifs*</span><span class="sxs-lookup"><span data-stu-id="180ab-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="180ab-108">Zéro, un ou plusieurs attributs MIDL.</span><span class="sxs-lookup"><span data-stu-id="180ab-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="180ab-109">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="180ab-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="180ab-110">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="180ab-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="180ab-111">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="180ab-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="180ab-112">Spécifie le nom de la fonction dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="180ab-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="180ab-113">*params*</span><span class="sxs-lookup"><span data-stu-id="180ab-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="180ab-114">Zéro, un ou plusieurs paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="180ab-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="180ab-115">Notes</span><span class="sxs-lookup"><span data-stu-id="180ab-115">Remarks</span></span>

<span data-ttu-id="180ab-116">La prise en charge de la notification **OnRequestEdit** signifie qu’avant qu’une modification soit apportée, l’objet envoie au client une demande d’autorisation de modification d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="180ab-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="180ab-117">Un objet peut prendre en charge la liaison de données mais ne pas avoir cet attribut.</span><span class="sxs-lookup"><span data-stu-id="180ab-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="180ab-118">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="180ab-118">Flags</span></span>

<span data-ttu-id="180ab-119">FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT</span><span class="sxs-lookup"><span data-stu-id="180ab-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="180ab-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="180ab-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="180ab-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="180ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180ab-122">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="180ab-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="180ab-123">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="180ab-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="180ab-124">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="180ab-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="180ab-125">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="180ab-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 