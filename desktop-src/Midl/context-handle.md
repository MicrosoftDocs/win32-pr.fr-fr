---
title: attribut context_handle
description: L’attribut \ Context \_ handle \ identifie un handle de liaison qui gère le contexte, ou les informations d’État, sur le serveur entre les appels de procédure distante.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724957"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="ec157-104">attribut de handle de contexte \_</span><span class="sxs-lookup"><span data-stu-id="ec157-104">context\_handle attribute</span></span>

<span data-ttu-id="ec157-105">L’attribut de **\[ \_ handle \] de contexte** identifie un handle de liaison qui gère le contexte, ou les informations d’État, sur le serveur entre les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="ec157-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="ec157-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec157-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec157-107">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="ec157-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-108">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="ec157-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="ec157-109">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="ec157-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-110">Spécifie un type pointeur ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="ec157-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="ec157-111">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="ec157-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="ec157-112">*déclarateur et déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="ec157-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-113">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="ec157-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="ec157-114">Le déclarateur d’un handle de contexte doit inclure au moins un déclarateur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="ec157-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="ec157-115">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="ec157-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="ec157-116">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ec157-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="ec157-117">L’identificateur de nom de paramètre dans le déclarateur de fonction est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ec157-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="ec157-118">*function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="ec157-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-119">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="ec157-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="ec157-120">Les attributs de fonction valides sont **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[ \_ handle \] de contexte**.</span><span class="sxs-lookup"><span data-stu-id="ec157-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="ec157-121">*pointeur-decl*</span><span class="sxs-lookup"><span data-stu-id="ec157-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-122">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="ec157-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="ec157-123">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' **\*** indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="ec157-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec157-124">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="ec157-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-125">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="ec157-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ec157-126">*Parameter-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ec157-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-127">Spécifie zéro, un ou plusieurs attributs directionnels, attributs de champ, attributs d’utilisation et attributs de pointeur appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="ec157-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="ec157-128">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ec157-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="ec157-129">*Context-handle-type*</span><span class="sxs-lookup"><span data-stu-id="ec157-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ec157-130">Spécifie l’identificateur qui spécifie le type de handle de contexte tel que défini dans une déclaration [**typedef**](typedef.md) qui prend l’attribut de **\[ \_ handle \] de contexte** .</span><span class="sxs-lookup"><span data-stu-id="ec157-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="ec157-131">La routine d’arrêt est facultative.</span><span class="sxs-lookup"><span data-stu-id="ec157-131">The rundown routine is optional.</span></span>

<span data-ttu-id="ec157-132">**Windows ServerÂ 2003 et WINDOWSÂ XP :** Une interface unique peut prendre en charge des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé).</span><span class="sxs-lookup"><span data-stu-id="ec157-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="ec157-133">Ces fonctionnalités d’accès sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs).</span><span class="sxs-lookup"><span data-stu-id="ec157-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="ec157-134">Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées.</span><span class="sxs-lookup"><span data-stu-id="ec157-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="ec157-135">Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées.</span><span class="sxs-lookup"><span data-stu-id="ec157-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="ec157-136">Notez que les méthodes de création sont implicitement sérialisées.</span><span class="sxs-lookup"><span data-stu-id="ec157-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec157-137">Notes</span><span class="sxs-lookup"><span data-stu-id="ec157-137">Remarks</span></span>

<span data-ttu-id="ec157-138">L’attribut de **\[ \_ handle \] de contexte** peut apparaître en tant qu’attribut de type [**typedef**](typedef.md) IDL, en tant qu’attribut de type de retour de fonction ou en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="ec157-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="ec157-139">Quand vous appliquez l’attribut de **\[ \_ handle \] de contexte** à une définition de type, vous devez également fournir une routine d’arrêt de contexte.</span><span class="sxs-lookup"><span data-stu-id="ec157-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="ec157-140">Pour plus d’informations, consultez [routine de fonctionnement du contexte de serveur](/windows/desktop/Rpc/server-context-run-down-routine) .</span><span class="sxs-lookup"><span data-stu-id="ec157-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="ec157-141">Quand vous utilisez le compilateur MIDL en mode par défaut ([**/ms. \_ ext**](-ms-ext.md)), un descripteur de contexte peut être n’importe quel type pointeur sélectionné par l’utilisateur, à condition qu’il soit conforme aux exigences des handles de contexte décrits ici.</span><span class="sxs-lookup"><span data-stu-id="ec157-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="ec157-142">Les données associées à ce type de descripteur de contexte ne sont pas transmises sur le réseau et ne doivent être manipulées que par l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="ec157-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="ec157-143">Les compilateurs IDL DCE restreignent les handles de contexte aux pointeurs de type [**void**](void.md) **\*** .</span><span class="sxs-lookup"><span data-stu-id="ec157-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="ec157-144">Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur [**/OSF**](-osf.md) du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="ec157-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="ec157-145">Comme avec d’autres types de handles, le handle de contexte est opaque pour l’application cliente, et toutes les données qui lui sont associées ne sont pas transmises.</span><span class="sxs-lookup"><span data-stu-id="ec157-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="ec157-146">Sur le serveur, le handle de contexte sert de handle sur le contexte actif, et toutes les données associées au type de descripteur de contexte sont accessibles.</span><span class="sxs-lookup"><span data-stu-id="ec157-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="ec157-147">Pour créer un handle de contexte, le client passe au serveur un **\[** [](out-idl.md) **\]** **\[** [](ref.md) **\]** pointeur Ref vers un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="ec157-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="ec157-148">(Le handle de contexte lui-même peut avoir une valeur **null** ou non **null** , à condition que sa valeur soit cohérente avec ses attributs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="ec157-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="ec157-149">Par exemple, quand l’attribut ref est appliqué au type de handle de contexte **\[** [](ref.md) **\]** , il ne peut pas avoir de valeur **null** .) Un autre handle de liaison doit être fourni pour accomplir la liaison jusqu’à ce que le handle de contexte soit créé.</span><span class="sxs-lookup"><span data-stu-id="ec157-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="ec157-150">Quand aucun handle explicite n’est spécifié, la liaison implicite est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ec157-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="ec157-151">Lorsqu’aucun **\[** attribut de [**\_ handle implicite**](implicit-handle.md) **\]** n’est présent, un handle automatique est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ec157-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="ec157-152">La procédure distante sur le serveur crée un handle de contexte actif.</span><span class="sxs-lookup"><span data-stu-id="ec157-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="ec157-153">Le client doit utiliser ce handle de contexte en tant que **\[** [](in.md) **\]** paramètre in ou **\[ in**, **out dans les \]** appels suivants.</span><span class="sxs-lookup"><span data-stu-id="ec157-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="ec157-154">Un handle **\[ de contexte \] en** uniquement peut être utilisé comme handle de liaison, donc il doit avoir une valeur non **null** .</span><span class="sxs-lookup"><span data-stu-id="ec157-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="ec157-155">Un handle **\[ de contexte en \]** uniquement ne reflète pas les modifications d’État sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ec157-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="ec157-156">Sur le serveur, la procédure appelée peut interpréter le descripteur de contexte en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="ec157-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="ec157-157">Par exemple, la procédure appelée peut allouer le stockage du tas et utiliser le handle de contexte comme pointeur vers ce stockage.</span><span class="sxs-lookup"><span data-stu-id="ec157-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="ec157-158">Pour fermer un handle de contexte, le client passe le handle de contexte en tant qu' **\[** argument [**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ec157-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="ec157-159">Le serveur doit retourner un handle de contexte **null** lorsqu’il ne gère plus le contexte pour le compte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="ec157-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="ec157-160">Par exemple, si le handle de contexte représente un fichier ouvert et que l’appel ferme le fichier, le serveur doit définir le handle de contexte sur la **valeur null** et le renvoyer au client.</span><span class="sxs-lookup"><span data-stu-id="ec157-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="ec157-161">Une valeur **null** n’est pas valide en tant que handle de liaison lors des appels suivants.</span><span class="sxs-lookup"><span data-stu-id="ec157-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="ec157-162">Un descripteur de contexte n’est valide que pour un seul serveur.</span><span class="sxs-lookup"><span data-stu-id="ec157-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="ec157-163">Lorsqu’une fonction a deux paramètres de handle et que le handle de contexte n’a pas la **valeur null**, les handles de liaison doivent faire référence au même espace d’adressage.</span><span class="sxs-lookup"><span data-stu-id="ec157-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="ec157-164">Quand une fonction possède un **\[** handle [**de contexte in**](in.md) **\]** ou **\[ in**, **out \]** , son handle de contexte peut être utilisé comme handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="ec157-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="ec157-165">Dans ce cas, la liaison implicite n’est pas utilisée et le **\[** [**\_ handle implicite**](implicit-handle.md) **\]** ou l’attribut de **\[** [**\_ handle automatique**](auto-handle.md) **\]** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ec157-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="ec157-166">Les restrictions suivantes s’appliquent aux handles de contexte :</span><span class="sxs-lookup"><span data-stu-id="ec157-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="ec157-167">Les handles de contexte ne peuvent pas être des éléments de tableau, des membres de structure ou des membres d’Union.</span><span class="sxs-lookup"><span data-stu-id="ec157-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="ec157-168">Ils peuvent uniquement être des paramètres.</span><span class="sxs-lookup"><span data-stu-id="ec157-168">They can only be parameters.</span></span>
-   <span data-ttu-id="ec157-169">Les handles de contexte ne peuvent pas avoir l' **\[** attribut [**transmit \_ As**](transmit-as.md) **\]** ou **\[** [**dereprésente \_ As**](represent-as.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ec157-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="ec157-170">Les paramètres qui sont des pointeurs vers **\[** [**des**](out-idl.md) **\]** Handles de contexte doivent être des **\[** [](ref.md) **\]** pointeurs Ref.</span><span class="sxs-lookup"><span data-stu-id="ec157-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="ec157-171">Un **\[** handle [**de contexte in**](in.md) **\]** peut être utilisé comme handle de liaison et ne peut pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ec157-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="ec157-172">Un handle **\[ de contexte in**, [**out**](out-idl.md) peut avoir la **valeur null** en entrée, mais uniquement si la procédure a un autre paramètre de handle explicite.</span><span class="sxs-lookup"><span data-stu-id="ec157-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="ec157-173">S’il n’existe aucun autre paramètre explicite **\[ de handle de** contexte non **null** , le handle de contexte **out \]** ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="ec157-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="ec157-174">Un descripteur de contexte ne peut pas être utilisé avec les rappels.</span><span class="sxs-lookup"><span data-stu-id="ec157-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="ec157-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="ec157-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="ec157-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec157-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec157-177">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="ec157-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="ec157-178">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="ec157-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="ec157-179">**rappel**</span><span class="sxs-lookup"><span data-stu-id="ec157-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="ec157-180">Réinitialisation du contexte client</span><span class="sxs-lookup"><span data-stu-id="ec157-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="ec157-181">**const**</span><span class="sxs-lookup"><span data-stu-id="ec157-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="ec157-182">Handles de contexte</span><span class="sxs-lookup"><span data-stu-id="ec157-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="ec157-183">**traitée**</span><span class="sxs-lookup"><span data-stu-id="ec157-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="ec157-184">Liaison et Handles</span><span class="sxs-lookup"><span data-stu-id="ec157-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="ec157-185">**tenir**</span><span class="sxs-lookup"><span data-stu-id="ec157-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="ec157-186">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="ec157-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="ec157-187">**in**</span><span class="sxs-lookup"><span data-stu-id="ec157-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="ec157-188">**localisé**</span><span class="sxs-lookup"><span data-stu-id="ec157-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="ec157-189">Clients multithread et handles de contexte</span><span class="sxs-lookup"><span data-stu-id="ec157-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="ec157-190">**/ms. \_ ext**</span><span class="sxs-lookup"><span data-stu-id="ec157-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="ec157-191">**à**</span><span class="sxs-lookup"><span data-stu-id="ec157-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="ec157-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="ec157-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="ec157-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="ec157-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="ec157-194">**représenter \_ comme**</span><span class="sxs-lookup"><span data-stu-id="ec157-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="ec157-195">**RpcSsDestroyClientContext**</span><span class="sxs-lookup"><span data-stu-id="ec157-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="ec157-196">Routine d’exécution du contexte de serveur</span><span class="sxs-lookup"><span data-stu-id="ec157-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="ec157-197">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="ec157-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="ec157-198">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="ec157-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="ec157-199">**typedef**</span><span class="sxs-lookup"><span data-stu-id="ec157-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="ec157-200">**unique**</span><span class="sxs-lookup"><span data-stu-id="ec157-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="ec157-201">**void**</span><span class="sxs-lookup"><span data-stu-id="ec157-201">**void**</span></span>](void.md)
</dt> </dl>

 

 