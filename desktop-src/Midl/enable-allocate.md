---
title: attribut enable_allocate
description: L’attribut \ Enable \_ allocate \ ACF spécifie que le code stub du serveur doit activer l’environnement de gestion de la mémoire stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate MIDL de l’attribut
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101505"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="1884e-104">activer l' \_ attribut d’allocation</span><span class="sxs-lookup"><span data-stu-id="1884e-104">enable\_allocate attribute</span></span>

<span data-ttu-id="1884e-105">L’attribut **\[ Enable ACF \_ allocate \]** spécifie que le code stub du serveur doit activer l’environnement de gestion de la mémoire stub.</span><span class="sxs-lookup"><span data-stu-id="1884e-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="1884e-106">L’attribut **\[ Enable \_ allocate \]** est obsolète et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1884e-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="1884e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1884e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1884e-108">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="1884e-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1884e-109">Spécifie une liste de zéro ou plusieurs attributs MIDL supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1884e-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1884e-110">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="1884e-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="1884e-111">Nom de l’interface à laquelle l’attribut **\[ Enable \_ allcoate \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="1884e-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1884e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1884e-112">Remarks</span></span>

<span data-ttu-id="1884e-113">En mode par défaut, le stub serveur Active l’environnement de mémoire uniquement lorsque l’attribut **\[ Enable \_ allocate \]** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1884e-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="1884e-114">L’environnement de gestion de la mémoire doit être activé pour que la mémoire puisse être allouée à l’aide de [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span><span class="sxs-lookup"><span data-stu-id="1884e-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="1884e-115">En mode **OSF** (lorsque vous compilez à l’aide du commutateur [**/OSF**](-osf.md) ), le stub active automatiquement cet environnement, ou à la demande lorsque l’attribut **\[ Enable \_ allocate \]** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1884e-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="1884e-116">Le stub côté client peut être sensible à l’environnement de gestion de mémoire **RPCSS** .</span><span class="sxs-lookup"><span data-stu-id="1884e-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="1884e-117">Si un stub client sensible est exécuté lorsque le package **RPCSS** est désactivé, l’allocateur/annulateurs d’utilisateur par défaut est appelé (par exemple, l’utilisateur [MIDL \_ \_ alloue](/windows/desktop/Rpc/the-midl-user-allocate-function)l' /  [ \_ utilisateur MIDL \_ gratuitement](/windows/desktop/Rpc/the-midl-user-free-function)).</span><span class="sxs-lookup"><span data-stu-id="1884e-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="1884e-118">Lorsqu’il est activé, le package **RPCSS** utilise la paire Allocator/annulateur du package.</span><span class="sxs-lookup"><span data-stu-id="1884e-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="1884e-119">Dans le mode par défaut, le client est sensible uniquement lorsque l’attribut **\[ Enable \_ allocate \]** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1884e-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="1884e-120">En règle générale, le stub côté client s’exécute dans l’environnement désactivé.</span><span class="sxs-lookup"><span data-stu-id="1884e-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="1884e-121">En mode **OSF** (lorsque vous compilez à l’aide du commutateur [**/OSF**](-osf.md) ), le client est toujours sensible à l’environnement de gestion de mémoire **RPCSS** et, par conséquent, l’attribut **\[ Enable \_ allocate \]** n’affecte pas les stubs du client.</span><span class="sxs-lookup"><span data-stu-id="1884e-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="1884e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1884e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1884e-123">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="1884e-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="1884e-124">allouer un \_ utilisateur MIDL \_</span><span class="sxs-lookup"><span data-stu-id="1884e-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="1884e-125">\_utilisateur \_ gratuit MIDL</span><span class="sxs-lookup"><span data-stu-id="1884e-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="1884e-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="1884e-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="1884e-127">RpcSmDisableAllocate</span><span class="sxs-lookup"><span data-stu-id="1884e-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="1884e-128">RpcSmEnableAllocate</span><span class="sxs-lookup"><span data-stu-id="1884e-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="1884e-129">RpcSmFree</span><span class="sxs-lookup"><span data-stu-id="1884e-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 