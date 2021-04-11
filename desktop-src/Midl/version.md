---
title: version (attribut)
description: L’attribut \ version \ de l’interface identifie une version particulière parmi plusieurs versions d’une interface RPC. Avec l’attribut version, vous vous assurez que seules les versions compatibles du logiciel client et serveur sont autorisées à se lier.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- MIDL, attribut de version
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030262"
---
# <a name="version-attribute"></a><span data-ttu-id="53cff-105">version (attribut)</span><span class="sxs-lookup"><span data-stu-id="53cff-105">version attribute</span></span>

<span data-ttu-id="53cff-106">L’attribut d’interface de **\[ version \]** identifie une version particulière parmi plusieurs versions d’une interface RPC.</span><span class="sxs-lookup"><span data-stu-id="53cff-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="53cff-107">Avec l’attribut version, vous vous assurez que seules les versions compatibles du logiciel client et serveur sont autorisées à se lier.</span><span class="sxs-lookup"><span data-stu-id="53cff-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="53cff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53cff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53cff-109">*valeur Major*</span><span class="sxs-lookup"><span data-stu-id="53cff-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="53cff-110">Spécifie un entier non signé Short compris entre zéro et 65 535 inclus, qui représente le numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="53cff-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="53cff-111">*valeur mineure*</span><span class="sxs-lookup"><span data-stu-id="53cff-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="53cff-112">Spécifie un entier non signé Short compris entre zéro et 65 535 inclus, qui représente le numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="53cff-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="53cff-113">La valeur de la version mineure est facultative.</span><span class="sxs-lookup"><span data-stu-id="53cff-113">The minor version value is optional.</span></span> <span data-ttu-id="53cff-114">Si elle est présente, la valeur de la version mineure est séparée du numéro de version principale par un point (.).</span><span class="sxs-lookup"><span data-stu-id="53cff-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="53cff-115">S’il n’est pas spécifié, la valeur de la version mineure est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="53cff-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53cff-116">Notes</span><span class="sxs-lookup"><span data-stu-id="53cff-116">Remarks</span></span>

<span data-ttu-id="53cff-117">Le compilateur MIDL ne prend pas en charge plusieurs versions d’une interface COM.</span><span class="sxs-lookup"><span data-stu-id="53cff-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="53cff-118">Par conséquent, une liste d’attributs d’interface qui inclut l’attribut d' **\[** [**objet**](object.md) **\]** ne peut pas inclure l’attribut de **\[ version \]** .</span><span class="sxs-lookup"><span data-stu-id="53cff-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="53cff-119">Pour créer une nouvelle version d’une interface COM existante, utilisez l’héritage de l’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="53cff-120">Une interface COM dérivée possède un UUID différent, mais hérite des fonctions membres d’interface, des codes d’État et des attributs d’interface de l’interface de base.</span><span class="sxs-lookup"><span data-stu-id="53cff-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="53cff-121">En association avec la **\[** [](uuid.md) **\]** valeur UUID, la valeur de **\[ version \]** identifie de manière unique l’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="53cff-122">La bibliothèque Runtime transmet la **\[ version \]** et les valeurs **\[ UUID \]** au serveur lorsque le client appelle une fonction distante.</span><span class="sxs-lookup"><span data-stu-id="53cff-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="53cff-123">Un client peut effectuer une liaison à un serveur pour une interface donnée dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="53cff-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="53cff-124">La valeur **\[ UUID \]** est la même.</span><span class="sxs-lookup"><span data-stu-id="53cff-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="53cff-125">Le numéro de version principale est le même.</span><span class="sxs-lookup"><span data-stu-id="53cff-125">The major version number is the same.</span></span>
-   <span data-ttu-id="53cff-126">Le numéro de version mineure du client est inférieur ou égal au numéro de version secondaire du serveur.</span><span class="sxs-lookup"><span data-stu-id="53cff-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="53cff-127">C’est à votre avantage et à l’avantage de permettre à vos utilisateurs de conserver une compatibilité ascendante entre les versionsÂ, c’est-à-dire de modifier l’interface afin que seul le numéro de version mineure soit modifié.</span><span class="sxs-lookup"><span data-stu-id="53cff-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="53cff-128">Vous pouvez conserver une compatibilité ascendante lorsque vous ajoutez de nouveaux types de données qui ne sont pas utilisés par les fonctions existantes et lorsque vous ajoutez de nouvelles fonctions sans modifier la spécification d’interface pour les fonctions existantes.</span><span class="sxs-lookup"><span data-stu-id="53cff-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="53cff-129">Modifiez le numéro de version principale si l’une des conditions suivantes s’applique :</span><span class="sxs-lookup"><span data-stu-id="53cff-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="53cff-130">Si vous modifiez un type de données utilisé par une fonction existante.</span><span class="sxs-lookup"><span data-stu-id="53cff-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="53cff-131">Si vous modifiez la spécification d’interface d’une fonction existante (telle que l’ajout ou la suppression d’un paramètre).</span><span class="sxs-lookup"><span data-stu-id="53cff-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="53cff-132">Si vous ajoutez des rappels qui sont appelés par des fonctions existantes.</span><span class="sxs-lookup"><span data-stu-id="53cff-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="53cff-133">Modifiez le numéro de version mineure si toutes les conditions suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="53cff-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="53cff-134">Si vous ajoutez des définitions ou des constantes de type qui ne sont pas utilisées par des fonctions ou des rappels existants.</span><span class="sxs-lookup"><span data-stu-id="53cff-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="53cff-135">Si vous ne modifiez pas les fonctions existantes et que vous ajoutez de nouvelles fonctions à l’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="53cff-136">Si vous ajoutez des rappels qui ne sont pas appelés par des fonctions existantes et que les nouveaux rappels suivent les fonctions existantes.</span><span class="sxs-lookup"><span data-stu-id="53cff-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="53cff-137">Si vos modifications qualifient comme une modification à compatibilité descendante de l’interface, utilisez la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="53cff-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="53cff-138">**Pour modifier le fichier d’interface (IDL)**</span><span class="sxs-lookup"><span data-stu-id="53cff-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="53cff-139">Ajoutez de nouvelles définitions de constantes et de types au fichier d’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="53cff-140">Ajoutez des fonctions de rappel à la fin du fichier d’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="53cff-141">Ajoutez de nouvelles fonctions à la fin du fichier d’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="53cff-142">L’attribut **\[ version \]** peut se produire au plus une fois dans l’en-tête de l’interface.</span><span class="sxs-lookup"><span data-stu-id="53cff-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="53cff-143">Lorsque l’attribut version n’est pas présent, l’interface a une version par défaut de 0,0.</span><span class="sxs-lookup"><span data-stu-id="53cff-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="53cff-144">Le point entre les nombres principaux et secondaires est un délimiteur et ne représente pas une virgule décimale.</span><span class="sxs-lookup"><span data-stu-id="53cff-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="53cff-145">Le nombre mineur est traité comme un entier.</span><span class="sxs-lookup"><span data-stu-id="53cff-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="53cff-146">Les zéros non significatifs ne sont pas significatifs.</span><span class="sxs-lookup"><span data-stu-id="53cff-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="53cff-147">Les zéros de fin sont significatifs.</span><span class="sxs-lookup"><span data-stu-id="53cff-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="53cff-148">Par exemple, le paramètre de version 1,11 représente une valeur majeure d’un et une valeur mineure de onze.</span><span class="sxs-lookup"><span data-stu-id="53cff-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="53cff-149">La version 1,11 ne représente pas une valeur comprise entre 1,1 et 1,2.</span><span class="sxs-lookup"><span data-stu-id="53cff-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="53cff-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53cff-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cff-151">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="53cff-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="53cff-152">**interface**</span><span class="sxs-lookup"><span data-stu-id="53cff-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="53cff-153">**object**</span><span class="sxs-lookup"><span data-stu-id="53cff-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="53cff-154">**universel**</span><span class="sxs-lookup"><span data-stu-id="53cff-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




