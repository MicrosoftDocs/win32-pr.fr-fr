---
title: Ciblage des stubs pour des plateformes 32 bits ou 64 bits spécifiques
description: Certaines des fonctionnalités de Microsoft RPC et des compilateurs MIDL 3,0 et versions ultérieures sont spécifiques à la plateforme.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL de plateformes 32 bits
- MIDL de plateformes 64 bits
- stubs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310730"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="7c5c3-106">Ciblage des stubs pour des plateformes 32 bits ou 64 bits spécifiques</span><span class="sxs-lookup"><span data-stu-id="7c5c3-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="7c5c3-107">Certaines des fonctionnalités de Microsoft RPC et des compilateurs MIDL 3,0 et versions ultérieures sont spécifiques à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="7c5c3-108">Par précaution, les compilateurs MIDL 3,0 et versions ultérieures génèrent des gardes qui facilitent la vérification de la compatibilité pendant la phase de compilation C.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="7c5c3-109">MIDL génère deux types de protecteurs : une protection dépendante de la plateforme (32 bits par rapport à 64 bits) et une protection dépendante de la version (dépendance de l’ensemble de fonctionnalités).</span><span class="sxs-lookup"><span data-stu-id="7c5c3-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="7c5c3-110">Par exemple, MIDL génère la protection suivante pour empêcher la compilation en C d’un stub 32 bits pour d’autres plateformes :</span><span class="sxs-lookup"><span data-stu-id="7c5c3-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="7c5c3-111">La protection dépendante de la mise en version est déclenchée par un ensemble de fonctionnalités figurant dans le ou les fichiers IDL traités et par le commutateur [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5c3-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="7c5c3-112">Par exemple, si l’interface utilise des fonctionnalités prises en charge uniquement sur WindowsÂ 2000 ou une version ultérieure, MIDL génère une protection avec la cible \_ \_ NT50 \_ ou une \_ macro ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="7c5c3-113">Les macros Guard, définies dans Rpcndr. h, dépendent de la valeur de WINVER et \_ de \_ winnt Win32 et sont évaluées par le compilateur C/C++.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="7c5c3-114">Si, au moment de la compilation, vous recevez un message d’erreur indiquant que vous avez besoin d’une plateforme spécifique pour exécuter un stub, commencez par vérifier que vous n’avez pas utilisé une fonctionnalité qui n’est pas disponible sur cette plateforme.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="7c5c3-115">Les fonctionnalités déclenchant une protection particulière sont répertoriées dans le corps de la protection.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="7c5c3-116">Dans l’exemple précédent, le commutateur-Oicf a déclenché la protection.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="7c5c3-117">Les fonctionnalités notables de ce type incluent le commutateur [**/Robust**](-robust.md) et l' \[ attribut [**async**](async.md) \] disponible sur WindowsÂ 2000 et versions ultérieures, le constructeur de type [**pipe**](pipe.md) , l’option de compilateur/OIF et les \[ attributs [**\_ Marshal d’utilisateur**](user-marshal.md) \] et \[ [**\_ marshaling de câble**](wire-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="7c5c3-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="7c5c3-118">Les stubs utilisant ces fonctionnalités ne seront pas exécutés sur les systèmes antérieurs.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="7c5c3-119">Si vous savez que votre plateforme cible est correcte pour les fonctionnalités que vous utilisez et que vous recevez toujours une erreur, vous devrez peut-être définir les variables d’environnement de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="7c5c3-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="7c5c3-120">**Pour générer des mises en production pour WindowsÂ 2000 ou versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="7c5c3-121">Ajoutez cette ligne à votre Makefile :</span><span class="sxs-lookup"><span data-stu-id="7c5c3-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="7c5c3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c5c3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c5c3-123">**/Target**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-124">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-125">**async**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-126">**\_UUID asynchrone**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-127">**/OI**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-128">**canal**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-129">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-130">**Marshal d’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="7c5c3-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="7c5c3-131">Marshaling des types de données OLE</span><span class="sxs-lookup"><span data-stu-id="7c5c3-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




