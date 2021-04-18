---
title: attribut context_handle_serialize
description: L’attribut \ Context \_ handle \_ Serialize \ ACF garantit qu’un handle de contexte sera toujours sérialisé, quel que soit le comportement par défaut de l’application.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize MIDL de l’attribut
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106543046"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="18564-104">attribut de sérialisation du \_ handle de contexte \_</span><span class="sxs-lookup"><span data-stu-id="18564-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="18564-105">L’attribut de **\[ handle de contexte de \_ \_ sérialisation \] de contexte** garantit qu’un handle de contexte sera toujours sérialisé, quel que soit le comportement par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="18564-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="18564-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18564-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18564-107">*type-ACF-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="18564-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18564-108">Tous les autres attributs ACF qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="18564-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="18564-109">*Context-handle-type*</span><span class="sxs-lookup"><span data-stu-id="18564-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="18564-110">Identificateur qui spécifie le type de handle de contexte, tel que défini dans une déclaration [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="18564-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="18564-111">Il s’agit du type qui reçoit l’attribut de **\[ \_ \_ sérialisation \] du handle de contexte** dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="18564-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="18564-112">*function-ACF-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="18564-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18564-113">Tous les attributs ACF supplémentaires qui s’appliquent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="18564-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="18564-114">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="18564-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="18564-115">Nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="18564-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="18564-116">*Parameter-ACF-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="18564-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18564-117">Tous les autres attributs ACF qui s’appliquent au paramètre.</span><span class="sxs-lookup"><span data-stu-id="18564-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18564-118">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="18564-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="18564-119">Nom du paramètre tel que défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="18564-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18564-120">Notes</span><span class="sxs-lookup"><span data-stu-id="18564-120">Remarks</span></span>

<span data-ttu-id="18564-121">L’attribut de **\[ \_ \_ sérialisation \] du handle de contexte** identifie un handle de liaison qui gère les informations de contexte ou d’État sur le serveur entre les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="18564-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="18564-122">L’attribut peut apparaître en tant qu’attribut de type [**typedef**](typedef.md) IDL, en tant qu’attribut de type de retour de fonction ou en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="18564-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="18564-123">Par défaut, les appels sur les handles de contexte sont sérialisés, mais une application peut appeler [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) pour remplacer ce comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="18564-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="18564-124">L’utilisation de l’attribut de **\[ \_ \_ sérialisation \] du handle de contexte** dans un fichier ACF garantit que les appels sur ce handle de contexte particulier seront sérialisés, même si l’application appelante a remplacé la sérialisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="18564-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="18564-125">Une routine d’arrêt de contexte est facultative.</span><span class="sxs-lookup"><span data-stu-id="18564-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="18564-126">Cet attribut est disponible dans MIDL version 5,0.</span><span class="sxs-lookup"><span data-stu-id="18564-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="18564-127">**Windows ServerÂ 2003 et WINDOWSÂ XP ou version ultérieure :** Une interface unique peut prendre en charge des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé).</span><span class="sxs-lookup"><span data-stu-id="18564-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="18564-128">Ces fonctionnalités d’accès sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs).</span><span class="sxs-lookup"><span data-stu-id="18564-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="18564-129">Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées.</span><span class="sxs-lookup"><span data-stu-id="18564-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="18564-130">Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées.</span><span class="sxs-lookup"><span data-stu-id="18564-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="18564-131">Notez que les méthodes de création sont implicitement sérialisées.</span><span class="sxs-lookup"><span data-stu-id="18564-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="18564-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="18564-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="18564-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18564-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18564-134">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="18564-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="18564-135">Attributs ACF</span><span class="sxs-lookup"><span data-stu-id="18564-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="18564-136">**handle de contexte \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="18564-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="18564-137">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="18564-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="18564-138">Handles de contexte</span><span class="sxs-lookup"><span data-stu-id="18564-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="18564-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="18564-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="18564-140">Routine d’exécution du contexte de serveur</span><span class="sxs-lookup"><span data-stu-id="18564-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="18564-141">Clients multithread et handles de contexte</span><span class="sxs-lookup"><span data-stu-id="18564-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="18564-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="18564-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 