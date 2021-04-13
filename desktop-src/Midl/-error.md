---
title: /Error (commutateur)
description: Le commutateur/Error détermine les types de vérification des erreurs que les stubs générés exécuteront au moment de l’exécution.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- MIDL du commutateur/Error
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380892"
---
# <a name="error-switch"></a><span data-ttu-id="af224-104">/Error (commutateur)</span><span class="sxs-lookup"><span data-stu-id="af224-104">/error switch</span></span>

<span data-ttu-id="af224-105">Le commutateur **/Error** détermine les types de vérification des erreurs que les stubs générés exécuteront au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="af224-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="af224-106">Cette fonctionnalité est obsolète et n’est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="af224-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="af224-107">L’utilisation du commutateur [**/Robust**](-robust.md) est recommandée.</span><span class="sxs-lookup"><span data-stu-id="af224-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="af224-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="af224-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="af224-109"><span id="allocation"></span><span id="ALLOCATION"></span>allocation \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="af224-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="af224-110">Vérifie si [**l' \_ \_ allocation d’utilisateur MIDL**](midl-user-allocate-1.md) retourne une valeur **null** , indiquant une erreur de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="af224-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="af224-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\_données stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="af224-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="af224-112">Génère un stub qui intercepte les exceptions d’annulation de marshaling côté serveur et les propage au client.</span><span class="sxs-lookup"><span data-stu-id="af224-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="af224-113"><span id="ref"></span><span id="REF"></span>Ref \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="af224-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="af224-114">Génère du code qui exécute une vérification au moment de l’exécution pour s’assurer qu’aucun pointeur de référence **null** n’est passé aux stubs du client et déclenche une \_ \_ \_ exception de pointeur Ref null RPC X \_ s’il en trouve.</span><span class="sxs-lookup"><span data-stu-id="af224-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="af224-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>contrôle des limites \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="af224-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="af224-116">Vérifie la taille des tableaux variables et variables de conformité par rapport à la spécification de longueur de transmission.</span><span class="sxs-lookup"><span data-stu-id="af224-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="af224-117"><span id="none"></span><span id="NONE"></span>aucun \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="af224-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="af224-118">N’effectue aucune vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="af224-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="af224-119"><span id="all"></span><span id="ALL"></span>tous les \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="af224-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="af224-120">Effectue toutes les vérifications d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="af224-120">Performs all error checking.</span></span> <span data-ttu-id="af224-121">Efficace avec MIDL version 5,0, il s’agit d’un commutateur de compilateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="af224-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af224-122">Notes</span><span class="sxs-lookup"><span data-stu-id="af224-122">Remarks</span></span>

<span data-ttu-id="af224-123">Le commutateur **/Error** sélectionne le nombre de vérifications d’erreurs effectuées par les fichiers stub générés.</span><span class="sxs-lookup"><span data-stu-id="af224-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="af224-124">En vigueur avec MIDL version 5,0, le paramètre par défaut est **/Error All**.</span><span class="sxs-lookup"><span data-stu-id="af224-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="af224-125">Les erreurs d’énumération qui sont vérifiées (par défaut dans toutes les versions de MIDL) sont des erreurs de troncation provoquées lors de la conversion entre des types **enum longs** (entiers 32 bits) et des types **enum courts** (la représentation de données réseau de [**enum**](enum.md)) et le nombre d’identificateurs dans une énumération dépassant 32 767.</span><span class="sxs-lookup"><span data-stu-id="af224-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="af224-126">La vérification des erreurs d’accès à la mémoire (également par défaut dans toutes les versions de MIDL) concerne les pointeurs qui dépassent la fin de la mémoire tampon dans le code de marshaling et les tableaux conformes dont la taille est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="af224-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="af224-127">Utilisez l’indicateur de **\_ vérification de limites/Error** pour rechercher d’autres limites de tableau non valides.</span><span class="sxs-lookup"><span data-stu-id="af224-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="af224-128">Lorsque vous spécifiez l' **allocation de/Error**, les stubs incluent du code qui lève une exception lorsque l' [**\_ utilisateur MIDL \_ allocate**](midl-user-allocate-1.md) retourne 0.</span><span class="sxs-lookup"><span data-stu-id="af224-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="af224-129">L’option de **\_ données de stub/Error** empêche les données du client de se bloquer sur le serveur pendant le démarshaling, ce qui offre une méthode plus robuste pour gérer l’opération de démarshaling.</span><span class="sxs-lookup"><span data-stu-id="af224-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="af224-130">Efficace avec WindowsÂ 2000, le moteur de marshaling des NDR à l’exécution sous-jacent effectue la plupart de ces contrôles.</span><span class="sxs-lookup"><span data-stu-id="af224-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="af224-131">Cela signifie que si vous utilisez l’un des modes entièrement interprétés ([**/OI**](-oi.md), **/OIF**) de la génération du stub, le choix des options de vérification des erreurs différentes n’aura pas d’effet marqué sur les performances.</span><span class="sxs-lookup"><span data-stu-id="af224-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="af224-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="af224-132">Examples</span></span>

<span data-ttu-id="af224-133">**attribution de l’attribution de nom de fichier. idl MIDL**</span><span class="sxs-lookup"><span data-stu-id="af224-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="af224-134">**MIDL/Error None nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="af224-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="af224-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af224-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af224-136">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="af224-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="af224-137">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="af224-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




