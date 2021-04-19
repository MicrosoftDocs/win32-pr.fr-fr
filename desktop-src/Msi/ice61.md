---
description: ICE61 valide la table de mise à niveau d’une base de données Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519410"
---
# <a name="ice61"></a><span data-ttu-id="1a965-103">ICE61</span><span class="sxs-lookup"><span data-stu-id="1a965-103">ICE61</span></span>

<span data-ttu-id="1a965-104">ICE61 vérifie la table de mise à niveau pour s’assurer que les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="1a965-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="1a965-105">Toutes les propriétés ActionProperty ne sont pas pré-créées dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1a965-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="1a965-106">Toutes les propriétés ActionProperty sont des propriétés publiques.</span><span class="sxs-lookup"><span data-stu-id="1a965-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="1a965-107">Toutes les propriétés ActionProperty sont incluses dans la propriété [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="1a965-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="1a965-108">Toutes les propriétés ActionProperty sont uniques à chaque enregistrement dans la table de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="1a965-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="1a965-109">Toutes les valeurs VersionMax ne sont pas inférieures aux valeurs VersionMin correspondantes.</span><span class="sxs-lookup"><span data-stu-id="1a965-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="1a965-110">Les valeurs VersionMin et VersionMax sont des versions de produit valides.</span><span class="sxs-lookup"><span data-stu-id="1a965-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="1a965-111">Consultez la propriété [**ProductVersion**](productversion.md) pour le format de version de produit valide.</span><span class="sxs-lookup"><span data-stu-id="1a965-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="1a965-112">Aucune tentative n’est faite pour supprimer une version plus récente ou égale du produit actuel.</span><span class="sxs-lookup"><span data-stu-id="1a965-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="1a965-113">Si vous ne corrigez pas un avertissement ou une erreur signalée par ICE61, les problèmes liés à la mise à niveau de votre application sont généralement problématiques.</span><span class="sxs-lookup"><span data-stu-id="1a965-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="1a965-114">En fonction de l’erreur exacte, il peut y avoir n’importe quoi, en laissant les fichiers de l’ancienne version en arrière-plan, en supprimant les fichiers de l’ancienne version, même s’ils sont requis par la nouvelle application, ou en cas de défaillance complète de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="1a965-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="1a965-115">Résultats</span><span class="sxs-lookup"><span data-stu-id="1a965-115">Result</span></span>

<span data-ttu-id="1a965-116">ICE61 publie un avertissement ou une erreur si l’une des conditions ci-dessus n’est pas remplie.</span><span class="sxs-lookup"><span data-stu-id="1a965-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="1a965-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a965-117">Example</span></span>

<span data-ttu-id="1a965-118">ICE61 signale les erreurs et avertissements suivants pour les exemples indiqués.</span><span class="sxs-lookup"><span data-stu-id="1a965-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="1a965-119">Dans ce cas, la première ligne essaiera de supprimer un produit de la même version.</span><span class="sxs-lookup"><span data-stu-id="1a965-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="1a965-120">(La colonne VersionMax est égale à la version du produit dans la table de propriétés).</span><span class="sxs-lookup"><span data-stu-id="1a965-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="1a965-121">Pour corriger cette erreur, utilisez une version de la colonne VersionMax inférieure à la version actuelle spécifiée dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1a965-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="1a965-122">Supprimez le bit **msidbUpgradeAttributesVersionMaxInclusive** de la colonne attributs si le VersionMax est égal à la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="1a965-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="1a965-123">Si l’objectif est uniquement de détecter le produit et de ne pas le supprimer, l’ajout du bit **msidbUpgradeAttributesOnlyDetect** à la colonne attributs corrigera également cette erreur.</span><span class="sxs-lookup"><span data-stu-id="1a965-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="1a965-124">À moins que la propriété ne soit listée dans la propriété [**SecureCustomProperties**](securecustomproperties.md) , la propriété n’est pas transmise au côté serveur de l’installation lorsque la propriété est trouvée.</span><span class="sxs-lookup"><span data-stu-id="1a965-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="1a965-125">Pour corriger cette erreur, ajoutez la propriété à [**SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="1a965-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="1a965-126">Les propriétés de mise à niveau doivent être des propriétés publiques pour que le résultat soit transmis au côté serveur de l’installation.</span><span class="sxs-lookup"><span data-stu-id="1a965-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="1a965-127">Pour corriger cette erreur, utilisez toutes les lettres majuscules dans le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1a965-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="1a965-128">Une propriété ne peut être utilisée que sur une seule ligne de la table de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="1a965-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="1a965-129">Pour corriger cette erreur, utilisez une autre propriété pour la deuxième ligne.</span><span class="sxs-lookup"><span data-stu-id="1a965-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="1a965-130">La version minimale doit être inférieure à la version maximale.</span><span class="sxs-lookup"><span data-stu-id="1a965-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="1a965-131">Pour corriger cette erreur, vérifiez que les numéros de version ne sont pas corrects.</span><span class="sxs-lookup"><span data-stu-id="1a965-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="1a965-132">S’ils sont corrects et que vous souhaitez utiliser la plage entre les deux versions, changez-les afin que VersionMin soit inférieur à VersionMax.</span><span class="sxs-lookup"><span data-stu-id="1a965-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="1a965-133">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="1a965-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="1a965-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="1a965-134">Property</span></span>                                                 | <span data-ttu-id="1a965-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a965-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="1a965-136">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="1a965-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="1a965-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="1a965-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="1a965-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="1a965-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="1a965-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="1a965-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="1a965-140">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="1a965-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="1a965-141">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1a965-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="1a965-142">Mettre à niveau la table</span><span class="sxs-lookup"><span data-stu-id="1a965-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="1a965-143">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="1a965-143">UpgradeCode</span></span>                            | <span data-ttu-id="1a965-144">VersionMin</span><span class="sxs-lookup"><span data-stu-id="1a965-144">VersionMin</span></span> | <span data-ttu-id="1a965-145">VersionMax</span><span class="sxs-lookup"><span data-stu-id="1a965-145">VersionMax</span></span> | <span data-ttu-id="1a965-146">Language</span><span class="sxs-lookup"><span data-stu-id="1a965-146">Language</span></span> | <span data-ttu-id="1a965-147">Attributs</span><span class="sxs-lookup"><span data-stu-id="1a965-147">Attributes</span></span> | <span data-ttu-id="1a965-148">Supprimer</span><span class="sxs-lookup"><span data-stu-id="1a965-148">Remove</span></span>                | <span data-ttu-id="1a965-149">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="1a965-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="1a965-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="1a965-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="1a965-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="1a965-151">2.01.0000</span></span>  |          | <span data-ttu-id="1a965-152">513</span><span class="sxs-lookup"><span data-stu-id="1a965-152">513</span></span>        |                       | <span data-ttu-id="1a965-153">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1a965-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="1a965-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="1a965-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="1a965-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="1a965-155">2.01.0001</span></span>  | <span data-ttu-id="1a965-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="1a965-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="1a965-157">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1a965-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="1a965-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="1a965-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="1a965-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="1a965-159">1.00.0000</span></span>  | <span data-ttu-id="1a965-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="1a965-160">2.00.0000</span></span>  | <span data-ttu-id="1a965-161">1033</span><span class="sxs-lookup"><span data-stu-id="1a965-161">1033</span></span>     |            | <span data-ttu-id="1a965-162">\[AppFeatureEnglish\]</span><span class="sxs-lookup"><span data-stu-id="1a965-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="1a965-163">EnglishAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="1a965-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1a965-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a965-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a965-165">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="1a965-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



