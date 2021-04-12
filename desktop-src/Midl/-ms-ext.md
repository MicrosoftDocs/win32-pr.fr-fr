---
title: commutateur/ms_ext
description: Efficace avec MIDL version 3,0, les fonctionnalités activées par le \_ commutateur MS ext sont à présent le mode par défaut pour le compilateur MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /commutateur ms_ext MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031096"
---
# <a name="ms_ext-switch"></a><span data-ttu-id="25cf3-104">\_commutateur/ms. ext</span><span class="sxs-lookup"><span data-stu-id="25cf3-104">/ms\_ext switch</span></span>

<span data-ttu-id="25cf3-105">Efficace avec MIDL version 3,0, les fonctionnalités activées par le commutateur **MS \_ ext** sont à présent le mode par défaut pour le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="25cf3-105">Effective with MIDL version 3.0, the features enabled by the **ms\_ext** switch are now the default mode for the MIDL compiler.</span></span>

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a><span data-ttu-id="25cf3-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="25cf3-106">Switch Options</span></span>

<span data-ttu-id="25cf3-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="25cf3-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="25cf3-108">Notes</span><span class="sxs-lookup"><span data-stu-id="25cf3-108">Remarks</span></span>

<span data-ttu-id="25cf3-109">L’utilisation du commutateur ne génère pas d’erreur du compilateur. vous n’avez donc pas besoin de supprimer les références à **/ms. \_ ext** ou [**/c \_ ext**](-c-ext.md) d’un Makefile existant.</span><span class="sxs-lookup"><span data-stu-id="25cf3-109">Using the switch will not generate a compiler error, so you do not have to remove references to **/ms\_ext** or [**/c\_ext**](-c-ext.md) from an existing makefile.</span></span>

<span data-ttu-id="25cf3-110">Les extensions Microsoft suivantes à l’ETCD OSF sont désormais disponibles par défaut :</span><span class="sxs-lookup"><span data-stu-id="25cf3-110">The following Microsoft extensions to OSF DCE are now available by default:</span></span>

-   <span data-ttu-id="25cf3-111">Définitions d’interface pour les objets OLE.</span><span class="sxs-lookup"><span data-stu-id="25cf3-111">Interface definitions for OLE objects.</span></span> <span data-ttu-id="25cf3-112">Pour plus d’informations sur les fichiers générés pour les interfaces OLE, consultez [fichiers générés pour une interface com](files-generated-for-a-com-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="25cf3-112">For more information on the files generated for OLE interfaces, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md)</span></span>
-   <span data-ttu-id="25cf3-113">Attribut de [**\[ rappel \]**](callback.md) spécifiant une fonction de rappel statique sur le client</span><span class="sxs-lookup"><span data-stu-id="25cf3-113">A [**\[callback\]**](callback.md) attribute specifying a static callback function on the client</span></span>
-   <span data-ttu-id="25cf3-114">[**\_ DEM quote**](cpp-quote.md)(*\_ chaîne entre guillemets*) et [**\# pragma MIDL \_ echo**](pragma.md)</span><span class="sxs-lookup"><span data-stu-id="25cf3-114">[**cpp\_quote**](cpp-quote.md)(*quoted\_string*) and [**\#pragma midl\_echo**](pragma.md)</span></span>
-   <span data-ttu-id="25cf3-115">types de caractères larges de [**WCHAR \_ t**](wchar-t.md) , constantes et chaînes</span><span class="sxs-lookup"><span data-stu-id="25cf3-115">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings</span></span>
-   <span data-ttu-id="25cf3-116">[**initialisation d’enum**](enum.md) (énumérateurs épars)</span><span class="sxs-lookup"><span data-stu-id="25cf3-116">[**enum initialization**](enum.md) (sparse enumerators)</span></span>
-   <span data-ttu-id="25cf3-117">Expressions telles que la taille et les spécificateurs de discriminateur</span><span class="sxs-lookup"><span data-stu-id="25cf3-117">Expressions as size and discriminator specifiers</span></span>
-   [<span data-ttu-id="25cf3-118">Gérer les extensions</span><span class="sxs-lookup"><span data-stu-id="25cf3-118">Handle extensions</span></span>](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [<span data-ttu-id="25cf3-119">Héritage de type d’attribut de pointeur</span><span class="sxs-lookup"><span data-stu-id="25cf3-119">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [<span data-ttu-id="25cf3-120">Plusieurs interfaces</span><span class="sxs-lookup"><span data-stu-id="25cf3-120">Multiple interfaces</span></span>](/windows/desktop/Rpc/registering-interfaces)
-   <span data-ttu-id="25cf3-121">Définitions en dehors du bloc d’interface</span><span class="sxs-lookup"><span data-stu-id="25cf3-121">Definitions outside of the interface block</span></span>
-   <span data-ttu-id="25cf3-122">Vous pouvez omettre les [attributs directionnels](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**dans**](in.md), [**out**](out-idl.md)\]</span><span class="sxs-lookup"><span data-stu-id="25cf3-122">You can omit [directional attributes](/windows/desktop/Rpc/directional-parameter-attributes) \[[**in**](in.md), [**out**](out-idl.md)\]</span></span>

## <a name="see-also"></a><span data-ttu-id="25cf3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25cf3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25cf3-124">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="25cf3-124">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="25cf3-125">Héritage de type d’attribut de pointeur</span><span class="sxs-lookup"><span data-stu-id="25cf3-125">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[<span data-ttu-id="25cf3-126">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="25cf3-126">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="25cf3-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="25cf3-127">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 