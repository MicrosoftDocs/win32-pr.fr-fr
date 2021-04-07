---
title: attribut context_handle_noserialize
description: L’attribut \ de handle de contexte \_ \_ noserialize \ ACF garantit qu’un handle de contexte ne sera jamais sérialisé, quel que soit le comportement par défaut de l’application.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize MIDL de l’attribut
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724964"
---
# <a name="context_handle_noserialize-attribute"></a><span data-ttu-id="5663a-104">\_attribut noserialize de handle de contexte \_</span><span class="sxs-lookup"><span data-stu-id="5663a-104">context\_handle\_noserialize attribute</span></span>

<span data-ttu-id="5663a-105">L’attribut de **\[ Gestionnaire de contexte \_ \_ noserialize \]** , qui garantit qu’un handle de contexte ne sera jamais sérialisé, quel que soit le comportement par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="5663a-105">The **\[context\_handle\_noserialize\]** ACF attribute guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="5663a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5663a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5663a-107">*type-ACF-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5663a-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5663a-108">Tous les autres attributs ACF qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="5663a-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="5663a-109">*Context-handle-type*</span><span class="sxs-lookup"><span data-stu-id="5663a-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5663a-110">Identificateur qui spécifie le type de handle de contexte, tel que défini dans une déclaration [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="5663a-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="5663a-111">Il s’agit du type qui reçoit l’attribut de [**\[ \_ handle \] de contexte**](context-handle.md) dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5663a-111">This is the type that receives the [**\[context\_handle\]**](context-handle.md) attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="5663a-112">*function-ACF-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5663a-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5663a-113">Tous les attributs ACF supplémentaires qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="5663a-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="5663a-114">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="5663a-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5663a-115">Nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5663a-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="5663a-116">*Parameter-ACF-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="5663a-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5663a-117">Tous les autres attributs ACF qui s’appliquent au paramètre.</span><span class="sxs-lookup"><span data-stu-id="5663a-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5663a-118">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="5663a-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5663a-119">Nom du paramètre tel que défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5663a-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5663a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5663a-120">Remarks</span></span>

<span data-ttu-id="5663a-121">L’attribut de [**\[ \_ handle \] de contexte**](context-handle.md) identifie un handle de liaison qui gère le contexte, ou les informations d’État, sur le serveur entre les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="5663a-121">The [**\[context\_handle\]**](context-handle.md) attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span> <span data-ttu-id="5663a-122">L’attribut peut apparaître en tant qu’attribut de type [**typedef**](typedef.md) IDL, en tant qu’attribut de type de retour de fonction ou en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="5663a-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="5663a-123">Par défaut, les appels sur les handles de contexte sont sérialisés.</span><span class="sxs-lookup"><span data-stu-id="5663a-123">By default, calls on context handles are serialized.</span></span> <span data-ttu-id="5663a-124">Une application peut appeler [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) pour remplacer ce comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="5663a-124">An application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="5663a-125">L’utilisation de l’attribut [**\[ \_ handle \] de contexte**](context-handle.md) dans un fichier ACF garantit que les appels sur ce handle de contexte particulier ne seront pas sérialisés, quel que soit le comportement de l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="5663a-125">Using the [**\[context\_handle\]**](context-handle.md) attribute in an ACF file guarantees that calls on this particular context handle will not be serialized, regardless of the calling application's behavior.</span></span> <span data-ttu-id="5663a-126">La fourniture d’une routine d’arrêt de contexte est facultative.</span><span class="sxs-lookup"><span data-stu-id="5663a-126">Providing a context rundown routine is optional.</span></span>

<span data-ttu-id="5663a-127">Cet attribut est disponible dans MIDL version 5,0.</span><span class="sxs-lookup"><span data-stu-id="5663a-127">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="5663a-128">**Windows ServerÂ 2003 et WINDOWSÂ XP ou version ultérieure :** Une interface unique peut prendre en charge des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé).</span><span class="sxs-lookup"><span data-stu-id="5663a-128">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="5663a-129">Ces fonctionnalités d’accès sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs).</span><span class="sxs-lookup"><span data-stu-id="5663a-129">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="5663a-130">Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées.</span><span class="sxs-lookup"><span data-stu-id="5663a-130">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="5663a-131">Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées.</span><span class="sxs-lookup"><span data-stu-id="5663a-131">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="5663a-132">Notez que les méthodes de création sont implicitement sérialisées.</span><span class="sxs-lookup"><span data-stu-id="5663a-132">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="5663a-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="5663a-133">Examples</span></span>

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="5663a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5663a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5663a-135">Attributs ACF</span><span class="sxs-lookup"><span data-stu-id="5663a-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="5663a-136">**\_sérialisation du handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="5663a-136">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="5663a-137">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="5663a-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="5663a-138">Handles de contexte</span><span class="sxs-lookup"><span data-stu-id="5663a-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="5663a-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="5663a-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="5663a-140">Routine d’exécution du contexte de serveur</span><span class="sxs-lookup"><span data-stu-id="5663a-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="5663a-141">Clients multithread et handles de contexte</span><span class="sxs-lookup"><span data-stu-id="5663a-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="5663a-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="5663a-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 