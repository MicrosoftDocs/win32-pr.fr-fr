---
title: attribut de rappel
description: L’attribut \ callback \ déclare une fonction de rappel statique qui existe du côté client de l’application distribuée. Les fonctions de rappel permettent au serveur d’exécuter du code sur le client.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- MIDL, attribut de rappel
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381892"
---
# <a name="callback-attribute"></a><span data-ttu-id="1a90d-105">attribut de rappel</span><span class="sxs-lookup"><span data-stu-id="1a90d-105">callback attribute</span></span>

<span data-ttu-id="1a90d-106">L’attribut **\[ callback \]** déclare une fonction de rappel statique qui existe du côté client de l’application distribuée.</span><span class="sxs-lookup"><span data-stu-id="1a90d-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="1a90d-107">Les fonctions de rappel permettent au serveur d’exécuter du code sur le client.</span><span class="sxs-lookup"><span data-stu-id="1a90d-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="1a90d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a90d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a90d-109">*function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="1a90d-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a90d-110">Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="1a90d-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="1a90d-111">Les attributs de fonction valides sont **\[** [**local**](local.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et les attributs d’utilisation **\[** [**chaîne**](string.md) **\]** , **\[** [**Ignorer**](ignore.md) **\]** et **\[** [**\_ handle de contexte**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1a90d-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="1a90d-112">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1a90d-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="1a90d-113">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="1a90d-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="1a90d-114">Spécifie [un \_ type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="1a90d-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="1a90d-115">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="1a90d-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="1a90d-116">*ptr-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="1a90d-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="1a90d-117">Spécifie zéro ou plusieurs déclarateurs de pointeur.</span><span class="sxs-lookup"><span data-stu-id="1a90d-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="1a90d-118">Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="1a90d-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a90d-119">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="1a90d-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1a90d-120">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="1a90d-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="1a90d-121">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="1a90d-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a90d-122">Spécifie zéro, un ou plusieurs attributs directionnels, attributs de champ, attributs d’utilisation et attributs de pointeur appropriés pour le type de paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a90d-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="1a90d-123">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="1a90d-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="1a90d-124">*declarator*</span><span class="sxs-lookup"><span data-stu-id="1a90d-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="1a90d-125">Spécifie un déclarateur C standard, comme des identificateurs, des déclarateurs de pointeurs et des déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="1a90d-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="1a90d-126">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="1a90d-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="1a90d-127">L’identificateur de nom de paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a90d-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a90d-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1a90d-128">Remarks</span></span>

<span data-ttu-id="1a90d-129">La fonction de **\[ rappel \]** est utile lorsque le serveur doit obtenir des informations à partir du client.</span><span class="sxs-lookup"><span data-stu-id="1a90d-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="1a90d-130">Si les applications serveur étaient prises en charge sur Windows 3. *x*, le serveur peut passer un appel à une procédure distante sur Windows 3. *x* Server pour obtenir les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="1a90d-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="1a90d-131">La fonction de rappel remplit la même fonction et permet au serveur d’interroger le client à la recherche d’informations dans le contexte de l’appel d’origine.</span><span class="sxs-lookup"><span data-stu-id="1a90d-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="1a90d-132">Les rappels sont des cas spéciaux d’appels distants qui s’exécutent dans le cadre d’un thread unique.</span><span class="sxs-lookup"><span data-stu-id="1a90d-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="1a90d-133">Un rappel est émis dans le contexte d’un appel distant.</span><span class="sxs-lookup"><span data-stu-id="1a90d-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="1a90d-134">Toute procédure distante définie dans le cadre de la même interface que la fonction de rappel statique peut appeler la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="1a90d-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="1a90d-135">Il est important de noter qu’il n' \[ est pas recommandé d’utiliser le rappel \] dans la programmation multithread.</span><span class="sxs-lookup"><span data-stu-id="1a90d-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="1a90d-136">En tant que fonction de programmation à thread unique, elle n’est pas conçue pour prendre en charge les demandes de sécurité fournies par un environnement multithread.</span><span class="sxs-lookup"><span data-stu-id="1a90d-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="1a90d-137">La fonction **RpcCancelThread** ne peut pas être utilisée pour annuler un appel qui peut distribuer un rappel statique.</span><span class="sxs-lookup"><span data-stu-id="1a90d-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="1a90d-138">Si un appel de procédure distante particulier n’entraîne jamais de rappel, il peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="1a90d-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="1a90d-139">Dans le cas contraire, un appel peut être annulé uniquement s’il peut être garanti qu’un rappel n’a pas été émis.</span><span class="sxs-lookup"><span data-stu-id="1a90d-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="1a90d-140">Seules les séquences orientées connexion et de protocole local prennent en charge l’attribut de rappel.</span><span class="sxs-lookup"><span data-stu-id="1a90d-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="1a90d-141">La taille des \[ données sortantes \] pour les rappels sur la séquence de protocole local est limitée à 150 octets.</span><span class="sxs-lookup"><span data-stu-id="1a90d-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="1a90d-142">Si une interface RPC utilise une séquence de protocole sans connexion (datagramme), les appels aux procédures avec l’attribut de rappel échouent.</span><span class="sxs-lookup"><span data-stu-id="1a90d-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="1a90d-143">Les handles ne peuvent pas être utilisés en tant que paramètres dans les fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="1a90d-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="1a90d-144">Étant donné que les rappels s’exécutent toujours dans le contexte d’un appel, le handle de liaison utilisé par le client pour effectuer l’appel au serveur est également utilisé comme handle de liaison du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="1a90d-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="1a90d-145">Les rappels peuvent être imbriqués à n’importe quelle profondeur.</span><span class="sxs-lookup"><span data-stu-id="1a90d-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="1a90d-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="1a90d-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="1a90d-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a90d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a90d-148">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="1a90d-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="1a90d-149">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="1a90d-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="1a90d-150">**const**</span><span class="sxs-lookup"><span data-stu-id="1a90d-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="1a90d-151">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="1a90d-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="1a90d-152">**variables**</span><span class="sxs-lookup"><span data-stu-id="1a90d-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="1a90d-153">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="1a90d-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1a90d-154">**tenir**</span><span class="sxs-lookup"><span data-stu-id="1a90d-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="1a90d-155">**localisé**</span><span class="sxs-lookup"><span data-stu-id="1a90d-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="1a90d-156">**/osf**</span><span class="sxs-lookup"><span data-stu-id="1a90d-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="1a90d-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="1a90d-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="1a90d-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="1a90d-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="1a90d-159">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="1a90d-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="1a90d-160">**modélis**</span><span class="sxs-lookup"><span data-stu-id="1a90d-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="1a90d-161">**UE**</span><span class="sxs-lookup"><span data-stu-id="1a90d-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="1a90d-162">**unique**</span><span class="sxs-lookup"><span data-stu-id="1a90d-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="1a90d-163">**RpcCancelThread**</span><span class="sxs-lookup"><span data-stu-id="1a90d-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 