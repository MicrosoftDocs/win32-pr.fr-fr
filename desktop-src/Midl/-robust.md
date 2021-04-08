---
title: commutateur/Robust
description: Le commutateur/Robust indique au compilateur MIDL de générer des informations supplémentaires de vérification des erreurs, que le moteur de NDR utilise pour effectuer des vérifications d’intégrité au moment de l’exécution.
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- MIDL du commutateur/Robust
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841122"
---
# <a name="robust-switch"></a><span data-ttu-id="19248-104">commutateur/Robust</span><span class="sxs-lookup"><span data-stu-id="19248-104">/robust switch</span></span>

<span data-ttu-id="19248-105">Le commutateur **/Robust** indique au compilateur MIDL de générer des informations supplémentaires de vérification des erreurs, que le moteur de NDR utilise pour effectuer des vérifications d’intégrité au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="19248-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="19248-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="19248-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="19248-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="19248-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="19248-108">*/OIF*</span><span class="sxs-lookup"><span data-stu-id="19248-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="19248-109">Ces commutateurs sont identiques dans leurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="19248-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="19248-110">Ils spécifient la méthode de proxy en mode Code du marshaling et utilisent des chaînes de format rapide pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="19248-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="19248-111">Voir/ [**OI**](-oi.md).</span><span class="sxs-lookup"><span data-stu-id="19248-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19248-112">Notes</span><span class="sxs-lookup"><span data-stu-id="19248-112">Remarks</span></span>

<span data-ttu-id="19248-113">L’utilisation du commutateur **/Robust** génère des informations supplémentaires qui permettent au moteur de représentation de données réseau d’effectuer une vérification des erreurs au moment de l’exécution sur des arguments corrélés dans des tableaux dynamiques, des unions et des pointeurs d’interface [**out**](out-idl.md) dans des applications DCOM.</span><span class="sxs-lookup"><span data-stu-id="19248-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="19248-114">Le commutateur **/Robust** est disponible uniquement sous WindowsÂ 2000 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="19248-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="19248-115">Un argument corrélé est un argument qui utilise l’un des attributs qui permettent de déterminer la taille d’un objet de données au moment de l’exécution : la [**taille \_ est**](size-is.md), la [**longueur \_ est**](length-is.md), le premier est, le [**dernier \_ est**](last-is.md), le [**nombre maximal \_**](max-is.md), le [**commutateur \_**](switch-is.md)et [**IID la \_ valeur**](iid-is.md). [**\_**](first-is.md)</span><span class="sxs-lookup"><span data-stu-id="19248-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="19248-116">Conformément à la spécification OSF-DCE pour la représentation filaire, cet argument corrélé apparaît à deux emplacements différents.</span><span class="sxs-lookup"><span data-stu-id="19248-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="19248-117">Par exemple, considérons une utilisation classique de la taille : attribute : **\_**</span><span class="sxs-lookup"><span data-stu-id="19248-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="19248-118">Dans cet exemple, le client passe une valeur long qui spécifie la taille d’un bloc de types de barres \_ (en termes de nombre d' \_ éléments de type barre) et un pointeur vers le bloc de types de barres réel \_ .</span><span class="sxs-lookup"><span data-stu-id="19248-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="19248-119">L’argument Size est corrélé avec l’argument pBarType.</span><span class="sxs-lookup"><span data-stu-id="19248-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="19248-120">Conformément à la spécification OSF-DCE, l’argument de taille est représenté deux fois sur le câble, d’abord comme lui-même, puis avec le tableau d’éléments de type de barre \_ qui représentent l’argument pBarType.</span><span class="sxs-lookup"><span data-stu-id="19248-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="19248-121">Chaque argument est démarshalé indépendamment, en fonction de sa propre représentation filaire.</span><span class="sxs-lookup"><span data-stu-id="19248-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="19248-122">Normalement, l’argument de taille et sa copie, qui est utilisée pour représenter une partie de l’autre argument, ont les mêmes valeurs.</span><span class="sxs-lookup"><span data-stu-id="19248-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="19248-123">Toutefois, si l’argument de taille est endommagé (par exemple, lorsque le bloc de types de barres \_ est plus grand que ce qui a été alloué), l’application serveur peut cesser de répondre, car elle utilise la valeur de l’argument size pour mesurer les données entrantes.</span><span class="sxs-lookup"><span data-stu-id="19248-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="19248-124">Le commutateur **/Robust** est requis pour implémenter une vérification de plage valide avec l’attribut de [**plage**](range.md) .</span><span class="sxs-lookup"><span data-stu-id="19248-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="19248-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="19248-125">Examples</span></span>

<span data-ttu-id="19248-126">**MIDL/Robust/Oicf NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="19248-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="19248-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19248-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19248-128">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="19248-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="19248-129">**/OI**</span><span class="sxs-lookup"><span data-stu-id="19248-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="19248-130">**vont**</span><span class="sxs-lookup"><span data-stu-id="19248-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




