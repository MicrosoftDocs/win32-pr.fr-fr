---
title: commutateur/OSF
description: Le commutateur/OSF force une compatibilité stricte avec l’ETCD OSF.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- MIDL du commutateur/OSF
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031125"
---
# <a name="osf-switch"></a><span data-ttu-id="76871-104">commutateur/OSF</span><span class="sxs-lookup"><span data-stu-id="76871-104">/osf switch</span></span>

<span data-ttu-id="76871-105">Le commutateur **/OSF** force une compatibilité stricte avec l’ETCD OSF.</span><span class="sxs-lookup"><span data-stu-id="76871-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="76871-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="76871-106">Switch Options</span></span>

<span data-ttu-id="76871-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="76871-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="76871-108">Notes</span><span class="sxs-lookup"><span data-stu-id="76871-108">Remarks</span></span>

<span data-ttu-id="76871-109">Utilisez ce commutateur si votre application requiert une compatibilité stricte avec l’ETCD OSF pour des raisons de portabilité.</span><span class="sxs-lookup"><span data-stu-id="76871-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="76871-110">En mode **/OSF** , le package RPCSS est activé automatiquement lorsque vous utilisez des pointeurs complets, les arguments nécessitent une allocation de mémoire ou lorsque vous utilisez l’attribut [**Enable \_ allocate**](enable-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="76871-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="76871-111">Cela signifie que vous n’avez pas besoin de fournir à l’utilisateur MIDL les fonctions d' [**\_ \_ allocation**](/windows/desktop/Rpc/the-midl-user-allocate-function) et de [**\_ \_ libération d’utilisateur MIDL**](/windows/desktop/Rpc/the-midl-user-free-function) dans votre application cliente et serveur.</span><span class="sxs-lookup"><span data-stu-id="76871-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="76871-112">Les fonctionnalités étendues Microsoft suivantes ne sont pas disponibles quand vous compilez avec le commutateur **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="76871-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="76871-113">Déclarateurs abstraits (paramètres sans nom) dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="76871-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="76871-114">Définitions d’interface pour les objets COM.</span><span class="sxs-lookup"><span data-stu-id="76871-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="76871-115">Noms d’interface avec plus de 17 caractères.</span><span class="sxs-lookup"><span data-stu-id="76871-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="76871-116">Attributs MIDL uniquement, tels que le [**\_ marshaling de câble**](wire-marshal.md), le [**\_ Marshal d’utilisateur**](user-marshal.md)et les extensions de TypeLib (ODL).</span><span class="sxs-lookup"><span data-stu-id="76871-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="76871-117">Utilisation de mots clés ACF dans un fichier IDL (option de **\_ configuration MIDL/App** ).</span><span class="sxs-lookup"><span data-stu-id="76871-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="76871-118">Fonctions de rappel statiques sur le client.</span><span class="sxs-lookup"><span data-stu-id="76871-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="76871-119">Attribut [**Async**](async.md) .</span><span class="sxs-lookup"><span data-stu-id="76871-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="76871-120">echo [**RPC \_ quote**](cpp-quote.md) et **\# pragma MIDL \_ echo**.</span><span class="sxs-lookup"><span data-stu-id="76871-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="76871-121">types de caractères étendus [**WCHAR \_ t**](wchar-t.md) , constantes et chaînes.</span><span class="sxs-lookup"><span data-stu-id="76871-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="76871-122">initialisation d' [**enum**](enum.md) (énumérateurs épars).</span><span class="sxs-lookup"><span data-stu-id="76871-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="76871-123">spécification de taille en [**sortie**](out-idl.md)seule.</span><span class="sxs-lookup"><span data-stu-id="76871-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="76871-124">Tableaux de tailles et de pointeurs mixtes.</span><span class="sxs-lookup"><span data-stu-id="76871-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="76871-125">Expressions utilisées pour les spécificateurs de taille et de discriminateur.</span><span class="sxs-lookup"><span data-stu-id="76871-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="76871-126">Paramètres de handle explicites dans n’importe quelle position dans la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="76871-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="76871-127">En mode **/OSF** , le compilateur MIDL recherche un handle de liaison explicite comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="76871-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="76871-128">Lorsque le premier paramètre n’est pas un handle de liaison et qu’un ou plusieurs descripteurs de contexte sont spécifiés, le descripteur de contexte le plus à gauche est utilisé comme handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="76871-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="76871-129">Lorsque le premier paramètre n’est pas un handle et qu’il n’existe aucun descripteur de contexte, la procédure utilise une liaison implicite à l’aide du handle [**implicite \_**](implicit-handle.md) de l’attribut ACF ou du [**\_ handle automatique**](auto-handle.md).</span><span class="sxs-lookup"><span data-stu-id="76871-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="76871-130">Héritage de type pointeur-Attribute.</span><span class="sxs-lookup"><span data-stu-id="76871-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="76871-131">Le DCE OSF n’autorise pas les pointeurs non attributs.</span><span class="sxs-lookup"><span data-stu-id="76871-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="76871-132">Par conséquent, en mode **/OSF** , chaque fichier IDL doit définir des attributs pour ses pointeurs.</span><span class="sxs-lookup"><span data-stu-id="76871-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="76871-133">Si un pointeur n’a pas d’attribut explicite, le fichier IDL doit avoir une spécification de [**pointeur \_ par défaut**](pointer-default.md) pour définir le type de pointeur.</span><span class="sxs-lookup"><span data-stu-id="76871-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="76871-134">Plusieurs interfaces dans un fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="76871-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="76871-135">Définitions en dehors du bloc d’interface.</span><span class="sxs-lookup"><span data-stu-id="76871-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="76871-136">Qualificateurs de type tels que **Far** et **StdCall**.</span><span class="sxs-lookup"><span data-stu-id="76871-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="76871-137">Omission des attributs directionnels.</span><span class="sxs-lookup"><span data-stu-id="76871-137">Omitting directional attributes.</span></span>

<span data-ttu-id="76871-138">Les extensions de langage C/C++ suivantes ne sont pas disponibles quand vous compilez avec le commutateur **/OSF** :</span><span class="sxs-lookup"><span data-stu-id="76871-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="76871-139">Champs de bits dans les structures et les unions.</span><span class="sxs-lookup"><span data-stu-id="76871-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="76871-140">Les commentaires sur une seule ligne sont séparés par deux barres obliques (//).</span><span class="sxs-lookup"><span data-stu-id="76871-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="76871-141">Déclarations externes.</span><span class="sxs-lookup"><span data-stu-id="76871-141">External declarations.</span></span>
-   <span data-ttu-id="76871-142">Procédures avec des ellipses dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="76871-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="76871-143">Tapez [**int**](int.md).</span><span class="sxs-lookup"><span data-stu-id="76871-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="76871-144">Tapez **void \*** (sauf avec l' [**attribut \_ handle de contexte**](context-handle.md) ).</span><span class="sxs-lookup"><span data-stu-id="76871-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="76871-145">Les qualificateurs de type, y compris le formulaire avec le préfixe conforme à la norme ANSI, contiennent deux caractères de soulignement : **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Exporter**, **Exporter**, **\_ \_ Far**, **Far**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **pres**, **\_ \_ Pascal**, **Pascal**, **\_ \_ StdCall**, **StdCall**, **\_ \_ volatile** et **volatile**.</span><span class="sxs-lookup"><span data-stu-id="76871-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="76871-146">Un \# Avertissement [**pragma**](pragma.md) ou un commentaire **\# pragma** .</span><span class="sxs-lookup"><span data-stu-id="76871-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="76871-147">Sérialisation de type.</span><span class="sxs-lookup"><span data-stu-id="76871-147">Type serialization.</span></span>
-   <span data-ttu-id="76871-148">Type de données [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="76871-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="76871-149">Le commutateur [**/Protocol**](-protocol.md) et la syntaxe de transfert ndr64.</span><span class="sxs-lookup"><span data-stu-id="76871-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="76871-150">Exemples</span><span class="sxs-lookup"><span data-stu-id="76871-150">Examples</span></span>

<span data-ttu-id="76871-151">**MIDL/OSF NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="76871-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="76871-152">**MIDL/OSF/App \_ config nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="76871-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="76871-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76871-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76871-154">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="76871-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="76871-155">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="76871-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="76871-156">**/ms. \_ ext**</span><span class="sxs-lookup"><span data-stu-id="76871-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="76871-157">Package de gestion de mémoire RPCSS</span><span class="sxs-lookup"><span data-stu-id="76871-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 