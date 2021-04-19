---
title: commutateur/c_ext
description: Ce commutateur est obsolète à partir de la version 3,0 du compilateur MIDL. Toutefois, l’utilisation du \_ commutateur c ext ne génère pas d’erreur du compilateur. vous n’avez donc pas besoin de supprimer les références à/ms. \_ ext ou/c \_ ext d’un Makefile existant.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /commutateur c_ext MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106538587"
---
# <a name="c_ext-switch"></a><span data-ttu-id="801ed-105">\_commutateur/c ext</span><span class="sxs-lookup"><span data-stu-id="801ed-105">/c\_ext switch</span></span>

<span data-ttu-id="801ed-106">Ce commutateur est obsolète à partir de la version 3,0 du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="801ed-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="801ed-107">Toutefois, l’utilisation du commutateur **c \_ ext** ne génère pas d’erreur du compilateur. vous n’avez donc pas besoin de supprimer les références à [**/ms. \_ ext**](-ms-ext.md) ou **/c \_ ext** d’un Makefile existant.</span><span class="sxs-lookup"><span data-stu-id="801ed-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="801ed-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="801ed-108">Switch Options</span></span>

<span data-ttu-id="801ed-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="801ed-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="801ed-110">Notes</span><span class="sxs-lookup"><span data-stu-id="801ed-110">Remarks</span></span>

<span data-ttu-id="801ed-111">Les fonctionnalités suivantes sont désormais disponibles par défaut :</span><span class="sxs-lookup"><span data-stu-id="801ed-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="801ed-112">De nombreux fichiers d’en-tête existants définissent des types avec des qualificateurs, tels que **Far** et **StdCall**, qui ne font pas partie de l’IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="801ed-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="801ed-113">Ces compilateurs (et le compilateur MIDL dans le mode de compatibilité DCE) génèrent des erreurs lorsqu’ils tentent de traiter ces qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="801ed-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="801ed-114">Le compilateur MIDL vous permet de compiler des fichiers IDL qui contiennent ces qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="801ed-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="801ed-115">Les qualificateurs de type n’affectent pas la manière dont les données sont transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="801ed-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="801ed-116">Vous pouvez omettre des attributs directionnels comme [**\[ in \]**](in.md) ou [**\[ out \]**](out-idl.md).</span><span class="sxs-lookup"><span data-stu-id="801ed-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="801ed-117">Les extensions de langage C suivantes sont prises en charge en mode par défaut :</span><span class="sxs-lookup"><span data-stu-id="801ed-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="801ed-118">Champs de bits dans les structures et les unions</span><span class="sxs-lookup"><span data-stu-id="801ed-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="801ed-119">Commentaires commençant par deux barres obliques (//)</span><span class="sxs-lookup"><span data-stu-id="801ed-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="801ed-120">Déclarations externes</span><span class="sxs-lookup"><span data-stu-id="801ed-120">External declarations</span></span>
-   <span data-ttu-id="801ed-121">Procédures avec des points de suspension dans la liste de paramètres (...)</span><span class="sxs-lookup"><span data-stu-id="801ed-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="801ed-122">Sur les plateformes 32 bits, [**int**](int.md) est un type de base 32 bits natif ; sur les plateformes 16 bits, **int** est reconnu, mais n’est pas un type accessible à distance</span><span class="sxs-lookup"><span data-stu-id="801ed-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="801ed-123">Tapez [**void \***](void.md) qui n’est pas utilisé dans les opérations distantes</span><span class="sxs-lookup"><span data-stu-id="801ed-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="801ed-124">Les qualificateurs de type (y compris le formulaire avec le préfixe conforme à la norme ANSI) contiennent deux caractères de soulignement : **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Exporter**, **\_ \_ Exporter**, **Far**, **\_ \_ Far**, **loadds**, **\_ \_ loadds**, **pres**, **\_ \_ near**, **Pascal**, **\_ \_ Pascal**, **StdCall**, **\_ \_ StdCall**, **volatile** et **\_ \_ volatile**.</span><span class="sxs-lookup"><span data-stu-id="801ed-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="801ed-125">Pour plus d’informations sur les qualificateurs de déclaration, consultez la documentation de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="801ed-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="801ed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="801ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801ed-127">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="801ed-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="801ed-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="801ed-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="801ed-129">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="801ed-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




