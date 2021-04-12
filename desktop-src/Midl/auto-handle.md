---
title: attribut auto_handle
description: L’attribut \ auto \_ handle \ ACF indique au stub d’établir automatiquement la liaison pour une fonction qui n’a pas de paramètre de handle de liaison explicite. Remarque Cet attribut est obsolète et n’est plus pris en charge.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462542"
---
# <a name="auto_handle-attribute"></a><span data-ttu-id="5d618-104">\_attribut de descripteur automatique</span><span class="sxs-lookup"><span data-stu-id="5d618-104">auto\_handle attribute</span></span>

<span data-ttu-id="5d618-105">L’attribut **\[ auto \_ handle \]** ACF indique au stub d’établir automatiquement la liaison pour une fonction qui n’a pas de paramètre de handle de liaison explicite.</span><span class="sxs-lookup"><span data-stu-id="5d618-105">The **\[auto\_handle\]** ACF attribute directs the stub to automatically establish the binding for a function that does not have an explicit binding-handle parameter.</span></span>

> [!Note]  
> <span data-ttu-id="5d618-106">Cet attribut est obsolète et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5d618-106">This attribute is obsolete and no longer supported.</span></span> <span data-ttu-id="5d618-107">L’utilisation du commutateur [**/Robust**](-robust.md) est recommandée.</span><span class="sxs-lookup"><span data-stu-id="5d618-107">Use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="5d618-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d618-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d618-109">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="5d618-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5d618-110">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à l’interface dans son ensemble, par exemple [**code**](code.md) ou [**nocode**](nocode.md).</span><span class="sxs-lookup"><span data-stu-id="5d618-110">Specifies zero or more attributes that apply to the interface as a whole, such as [**code**](code.md) or [**nocode**](nocode.md).</span></span> <span data-ttu-id="5d618-111">Séparez les attributs d’interface par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5d618-111">Separate interface attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="5d618-112">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="5d618-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5d618-113">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="5d618-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="5d618-114">*définition d’interface*</span><span class="sxs-lookup"><span data-stu-id="5d618-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="5d618-115">Spécifie les instructions IDL qui forment la définition de l’interface.</span><span class="sxs-lookup"><span data-stu-id="5d618-115">Specifies IDL statements that form the definition of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d618-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5d618-116">Remarks</span></span>

<span data-ttu-id="5d618-117">L’attribut **\[ \_ handle \] automatique** s’affiche dans l’en-tête d’interface du CCP.</span><span class="sxs-lookup"><span data-stu-id="5d618-117">The **\[auto\_handle\]** attribute appears in the interface header of the ACF.</span></span> <span data-ttu-id="5d618-118">Elle apparaît également dans l’en-tête d’interface du fichier IDL lorsque vous spécifiez le commutateur de compilateur MIDL [**/app \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="5d618-118">It also appears in the interface header of the IDL file when you specify the MIDL compiler switch [**/app\_config**](-app-config.md).</span></span>

<span data-ttu-id="5d618-119">Lorsque le client appelle une fonction qui utilise la liaison automatique et qu’il n’existe aucune liaison à un serveur, le stub établit automatiquement la liaison.</span><span class="sxs-lookup"><span data-stu-id="5d618-119">When the client calls a function that uses automatic binding and no binding to a server exists, the stub automatically establishes the binding.</span></span> <span data-ttu-id="5d618-120">La liaison est réutilisée pour les appels suivants à d’autres fonctions dans l’interface qui utilisent la liaison automatique.</span><span class="sxs-lookup"><span data-stu-id="5d618-120">The binding is reused for subsequent calls to other functions in the interface that use automatic binding.</span></span> <span data-ttu-id="5d618-121">Le programme d’application cliente n’a pas besoin de déclarer ou d’effectuer un traitement relatif au handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="5d618-121">The client application program does not have to declare or perform any processing relating to the binding handle.</span></span>

<span data-ttu-id="5d618-122">Lorsque le ACF n’est pas présent ou n’inclut pas l’attribut de [**\[ \_ handle \] implicite**](implicit-handle.md) , le compilateur MIDL utilise le **\[ \_ handle \] automatique** et émet un message d’information.</span><span class="sxs-lookup"><span data-stu-id="5d618-122">When the ACF is not present or does not include the [**\[implicit\_handle\]**](implicit-handle.md) attribute, the MIDL compiler uses **\[auto\_handle\]** and issues an informational message.</span></span> <span data-ttu-id="5d618-123">Le compilateur MIDL utilise également le **\[ \_ handle \] automatique**, si nécessaire, pour établir la liaison initiale pour un [**\[ \_ handle \] de contexte**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="5d618-123">The MIDL compiler also uses **\[auto\_handle\]**, if needed, to establish the initial binding for a [**\[context\_handle\]**](context-handle.md).</span></span>

<span data-ttu-id="5d618-124">L’attribut de **\[ \_ handle \] automatique** peut se produire uniquement si le [**\[ \_ handle \] implicite**](implicit-handle.md) ou l’attribut de [**\[ \_ handle \] explicite**](explicit-handle.md) ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="5d618-124">The **\[auto\_handle\]** attribute can occur only if the [**\[implicit\_handle\]**](implicit-handle.md) or [**\[explicit\_handle\]**](explicit-handle.md) attribute does not occur.</span></span> <span data-ttu-id="5d618-125">L’attribut de **\[ \_ handle \] automatique** peut se produire dans l’en-tête de l’interface ACF ou IDL au plus une fois.</span><span class="sxs-lookup"><span data-stu-id="5d618-125">The **\[auto\_handle\]** attribute can occur in the ACF or IDL interface header at most once.</span></span>

> [!Note]  
> <span data-ttu-id="5d618-126">Vous ne pouvez pas utiliser la liaison automatique (avec l’attribut **\[ \_ handle \] automatique** ou par défaut) si vous traitez des données par le biais de canaux.</span><span class="sxs-lookup"><span data-stu-id="5d618-126">You cannot use automatic binding (either with the **\[auto\_handle\]** attribute, or by default) if you are processing data through pipes.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5d618-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="5d618-127">Examples</span></span>

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a><span data-ttu-id="5d618-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d618-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d618-129">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="5d618-129">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="5d618-130">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="5d618-130">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="5d618-131">**code**</span><span class="sxs-lookup"><span data-stu-id="5d618-131">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="5d618-132">**\_handle explicite**</span><span class="sxs-lookup"><span data-stu-id="5d618-132">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="5d618-133">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="5d618-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="5d618-134">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="5d618-134">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="5d618-135">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="5d618-135">**nocode**</span></span>](nocode.md)
</dt> </dl>

 

 




