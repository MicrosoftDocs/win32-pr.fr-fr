---
description: Les propriétés de résumé des packages d’installation, des transformations et des correctifs sont décrites dans les tableaux suivants.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descriptions des propriétés de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537074"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="03ee2-103">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="03ee2-103">Summary Property Descriptions</span></span>

<span data-ttu-id="03ee2-104">Les propriétés de résumé des packages d’installation, des transformations et des correctifs sont décrites dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="03ee2-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="03ee2-105">Notez que la signification d’une propriété de résumé particulière peut être différente selon que la base de données appartient à un package d’installation, à une transformation ou à un package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="03ee2-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="03ee2-106">Pour plus d’informations sur les ID de propriété, les PID et les types, consultez [jeu de propriétés de flux d’informations de synthèse](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="03ee2-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="03ee2-107">Packages d’installation</span><span class="sxs-lookup"><span data-stu-id="03ee2-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03ee2-108">Summary, propriété</span><span class="sxs-lookup"><span data-stu-id="03ee2-108">Summary property</span></span></th>
<th><span data-ttu-id="03ee2-109">Signification de cette propriété dans une base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="03ee2-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03ee2-110"><a href="title-summary.md"><strong>Intitulé</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-111">Description de ce fichier sous la forme d’un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-111">A description of this file as an installation package.</span></span> <span data-ttu-id="03ee2-112">La description doit inclure la &quot; <a href="about-the-installer-database.md">base de données d’installation de</a>l’expression.&quot;</span><span class="sxs-lookup"><span data-stu-id="03ee2-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-113"><a href="subject-summary.md"><strong>Objet</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-114">Nom du produit installé par ce package.</span><span class="sxs-lookup"><span data-stu-id="03ee2-114">The name of the product installed by this package.</span></span> <span data-ttu-id="03ee2-115">Il doit s’agir du même nom que dans la propriété <a href="productname.md"><strong>ProductName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="03ee2-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-116"><a href="author-summary.md"><strong>Auteur</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-117">Nom du fabricant de ce produit.</span><span class="sxs-lookup"><span data-stu-id="03ee2-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="03ee2-118">Il doit s’agir du même nom que dans la propriété <a href="manufacturer.md"><strong>Manufacturer</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="03ee2-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-119"><a href="keywords-summary.md"><strong>Mots clés</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-120">Liste de mots clés qui peuvent être utilisés par les navigateurs de fichiers pour effectuer des recherches dans les mots clés d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="03ee2-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="03ee2-121">Les mots clés doivent inclure le &quot; programme d’installation &quot; et les mots clés spécifiques au produit.</span><span class="sxs-lookup"><span data-stu-id="03ee2-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-122"><a href="comments-summary.md"><strong>Commentaires</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-123">Contient l’expression : &quot; cette base de données du programme d’installation contient la logique et les données requises pour installer <<em>nom du produit</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="03ee2-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-124"><a href="template-summary.md"><strong>Modèle</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-125">La plateforme et les langages compatibles avec ce package d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="03ee2-126">Consultez <a href="template-summary.md"><strong>template</strong></a> pour la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="03ee2-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-127"><a href="last-saved-by-summary.md"><strong>Dernier enregistrement par</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-128">Les développeurs d’outils d’édition de base de données peuvent utiliser cette propriété pendant le processus de développement pour suivre la dernière personne à modifier la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="03ee2-129">Cette propriété doit avoir la valeur null dans une base de données d’expédition finale.</span><span class="sxs-lookup"><span data-stu-id="03ee2-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="03ee2-130">Le programme d’installation définit cette propriété sur la valeur de la propriété <a href="logonuser.md"><strong>LogonUser</strong></a> au cours d’une <a href="administrative-installation.md"><strong>installation d’administration</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="03ee2-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="03ee2-131">Le programme d’installation n’utilise jamais cette propriété et un utilisateur n’a jamais besoin de le modifier.</span><span class="sxs-lookup"><span data-stu-id="03ee2-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-132"><a href="revision-number-summary.md"><strong>Numéro de révision</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-133">Contient le <a href="package-codes.md">Code du package</a> du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-134"><a href="last-printed-summary.md"><strong>Dernière impression</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-135">Peut être défini sur la date et l’heure d’une <a href="administrative-installation.md">installation d’administration</a> à enregistrer lors de la création de l’image administrative.</span><span class="sxs-lookup"><span data-stu-id="03ee2-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-136"><a href="create-time-date-summary.md"><strong>Créer une date/heure</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-137">Heure et date de création de la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-138"><a href="last-saved-time-date-summary.md"><strong>Heure/date du dernier enregistrement</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-139">Date et heure système actuelles au moment de la dernière sauvegarde de la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="03ee2-140">Initialement null.</span><span class="sxs-lookup"><span data-stu-id="03ee2-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-141"><a href="page-count-summary.md"><strong>Nombre de pages</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-142">Contient une valeur utilisée pour identifier la version minimale du programme d’installation requise par ce package d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="03ee2-143">Par exemple, si le package requiert au minimum la version 2,0 du programme d’installation, cette propriété doit être définie sur un entier de 200.</span><span class="sxs-lookup"><span data-stu-id="03ee2-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="03ee2-144">La valeur de cette propriété doit être supérieure ou égale à 200 avec des <a href="64-bit-windows-installer-packages.md">packages de Windows Installer 64 bits</a>.</span><span class="sxs-lookup"><span data-stu-id="03ee2-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-145"><a href="word-count-summary.md"><strong>Nombre de mots</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-146">Type de l’image du fichier source.</span><span class="sxs-lookup"><span data-stu-id="03ee2-146">The type of the source file image.</span></span> <span data-ttu-id="03ee2-147">Stocké à la place de la propriété nombre standard.</span><span class="sxs-lookup"><span data-stu-id="03ee2-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="03ee2-148">Cette propriété est un champ de bits.</span><span class="sxs-lookup"><span data-stu-id="03ee2-148">This property is a bit field.</span></span> <span data-ttu-id="03ee2-149">Consultez la rubrique <a href="word-count-summary.md"><strong>nombre de mots</strong></a> pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="03ee2-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="03ee2-150">À partir de Windows Installer version 4,0 sur Windows Vista, cette propriété comprend des bits pour spécifier si des privilèges élevés sont requis.</span><span class="sxs-lookup"><span data-stu-id="03ee2-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-151"><a href="character-count-summary.md"><strong>Nombre de caractères</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-152">Null</span><span class="sxs-lookup"><span data-stu-id="03ee2-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-153"><a href="creating-application-summary.md"><strong>Création de l’application</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-154">Contient le nom du logiciel utilisé pour créer cette base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-155"><a href="security-summary.md"><strong>Sécurité</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-156">La valeur de cette propriété doit être 2-recommandée en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03ee2-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-157"><a href="codepage-summary.md"><strong>Courante</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-158">Valeur numérique de la page de codes ANSI utilisée pour afficher les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="03ee2-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="03ee2-159">Cette propriété doit être définie avant que toutes les propriétés de chaîne ne soient définies dans les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="03ee2-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="03ee2-160">Transformations</span><span class="sxs-lookup"><span data-stu-id="03ee2-160">Transforms</span></span>



| <span data-ttu-id="03ee2-161">Summary, propriété</span><span class="sxs-lookup"><span data-stu-id="03ee2-161">Summary property</span></span>                                              | <span data-ttu-id="03ee2-162">Signification de cette propriété dans une transformation</span><span class="sxs-lookup"><span data-stu-id="03ee2-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03ee2-163">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="03ee2-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="03ee2-164">Description de ce fichier en tant que transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-164">A description of this file as a transform.</span></span> <span data-ttu-id="03ee2-165">La description doit inclure la phrase suivante : «[transformer](database-transforms.md)».</span><span class="sxs-lookup"><span data-stu-id="03ee2-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="03ee2-166">**Objet**</span><span class="sxs-lookup"><span data-stu-id="03ee2-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="03ee2-167">Nom du produit installé par le package d’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="03ee2-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="03ee2-168">Il doit s’agir de la même valeur que la propriété Résumé de l' [**objet**](subject-summary.md) dans le package d’installation d’origine.</span><span class="sxs-lookup"><span data-stu-id="03ee2-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="03ee2-169">**Auteur**</span><span class="sxs-lookup"><span data-stu-id="03ee2-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="03ee2-170">Nom du fabricant de cette transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="03ee2-171">**Mots clés**</span><span class="sxs-lookup"><span data-stu-id="03ee2-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="03ee2-172">Liste de mots clés qui peuvent être utilisés par les navigateurs de fichiers pour effectuer des recherches dans les mots clés d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="03ee2-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="03ee2-173">Les mots clés doivent inclure « programme d’installation », ainsi que des mots clés spécifiques au produit.</span><span class="sxs-lookup"><span data-stu-id="03ee2-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="03ee2-174">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="03ee2-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="03ee2-175">Contient l’expression : « cette transformation contient la logique et les données requises pour installer <*nom de produit*> ».</span><span class="sxs-lookup"><span data-stu-id="03ee2-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="03ee2-176">[**Modèle**](template-summary.md) (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="03ee2-177">Les versions de plateforme et de langage compatibles avec cette transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="03ee2-178">Cette valeur peut être laissée vide s’il n’existe aucune restriction.</span><span class="sxs-lookup"><span data-stu-id="03ee2-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="03ee2-179">Vous ne pouvez spécifier qu’un seul langage pour une transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="03ee2-180">Pour plus d’informations sur la syntaxe, consultez [**modèle**](template-summary.md).</span><span class="sxs-lookup"><span data-stu-id="03ee2-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="03ee2-181">**Dernier enregistrement par**</span><span class="sxs-lookup"><span data-stu-id="03ee2-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="03ee2-182">ID de la plateforme et de la langue que la base de données a après avoir été transformée.</span><span class="sxs-lookup"><span data-stu-id="03ee2-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="03ee2-183">La propriété [**Résumé du modèle**](template-summary.md) de la nouvelle base de données doit être définie sur les mêmes valeurs.</span><span class="sxs-lookup"><span data-stu-id="03ee2-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="03ee2-184">[**Numéro de révision**](revision-number-summary.md) (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="03ee2-185">Liste des GUID de code de produit et de la version des produits nouveaux et originaux et du GUID du code de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="03ee2-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="03ee2-186">La liste est séparée par des points-virgules, comme suit.</span><span class="sxs-lookup"><span data-stu-id="03ee2-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="03ee2-187">*Original : code* du produit original-version du produit ; *New-Product Code New-Product-version*; *Mettre à niveau le code*</span><span class="sxs-lookup"><span data-stu-id="03ee2-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="03ee2-188">**Dernière impression**</span><span class="sxs-lookup"><span data-stu-id="03ee2-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="03ee2-189">Null</span><span class="sxs-lookup"><span data-stu-id="03ee2-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="03ee2-190">**Créer une date/heure**</span><span class="sxs-lookup"><span data-stu-id="03ee2-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="03ee2-191">Date et heure de création de la transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="03ee2-192">**Heure/date du dernier enregistrement**</span><span class="sxs-lookup"><span data-stu-id="03ee2-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="03ee2-193">Date et heure système actuelles au moment où la transformation a été enregistrée.</span><span class="sxs-lookup"><span data-stu-id="03ee2-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="03ee2-194">Initialement null.</span><span class="sxs-lookup"><span data-stu-id="03ee2-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="03ee2-195">[**Nombre de pages**](page-count-summary.md) (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="03ee2-196">Valeur utilisée pour indiquer la version minimale du programme d’installation requise pour traiter la transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="03ee2-197">La valeur doit être définie sur la plus grande des deux valeurs de propriété du [**nombre de pages**](page-count-summary.md) qui appartiennent aux bases de données utilisées pour générer la transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="03ee2-198">[**Nombre de mots**](word-count-summary.md) (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="03ee2-199">Null</span><span class="sxs-lookup"><span data-stu-id="03ee2-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="03ee2-200">**Nombre de caractères**</span><span class="sxs-lookup"><span data-stu-id="03ee2-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="03ee2-201">Cette partie du flux d’informations de résumé est divisée en mots de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="03ee2-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="03ee2-202">Le mot supérieur contient des [*indicateurs de validation de transformation*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="03ee2-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="03ee2-203">Le mot inférieur contient des [*indicateurs de condition d’erreur de transformation*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="03ee2-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="03ee2-204">**Création de l’application**</span><span class="sxs-lookup"><span data-stu-id="03ee2-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="03ee2-205">Contient le nom du logiciel utilisé pour créer cette transformation.</span><span class="sxs-lookup"><span data-stu-id="03ee2-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="03ee2-206">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="03ee2-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="03ee2-207">La valeur de cette propriété doit être en lecture seule appliquée à 4.</span><span class="sxs-lookup"><span data-stu-id="03ee2-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="03ee2-208">**Courante**</span><span class="sxs-lookup"><span data-stu-id="03ee2-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="03ee2-209">Valeur numérique de la page de codes ANSI utilisée pour afficher les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="03ee2-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="03ee2-210">Cette propriété doit être définie avant de pouvoir définir des propriétés de chaîne dans les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="03ee2-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="03ee2-211">Packages de correctifs</span><span class="sxs-lookup"><span data-stu-id="03ee2-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03ee2-212">Summary, propriété</span><span class="sxs-lookup"><span data-stu-id="03ee2-212">Summary property</span></span></th>
<th><span data-ttu-id="03ee2-213">Signification de cette propriété dans un package correctif</span><span class="sxs-lookup"><span data-stu-id="03ee2-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03ee2-214"><a href="title-summary.md"><strong>Intitulé</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-215">Description de ce fichier en tant que package correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-215">A description of this file as a patch package.</span></span> <span data-ttu-id="03ee2-216">La description doit inclure l’expression : &quot; <a href="patch-packages.md">patch</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="03ee2-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-217"><a href="subject-summary.md"><strong>Objet</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-218">Description du correctif qui comprend le nom du produit.</span><span class="sxs-lookup"><span data-stu-id="03ee2-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-219"><a href="author-summary.md"><strong>Auteur</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-220">Nom du fabricant du package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="03ee2-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-221"><a href="keywords-summary.md"><strong>Mots clés</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-222">Liste délimitée par des points-virgules des sources du correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-223"><a href="comments-summary.md"><strong>Commentaires</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-224">Contient l’expression : &quot; ce correctif contient la logique et les données requises pour installer <<em>nom de produit</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="03ee2-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-225"><a href="template-summary.md"><strong>Modèle</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-226">Liste délimitée par des points-virgules des codes de produit pouvant accepter ce correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-227"><a href="last-saved-by-summary.md"><strong>Dernier enregistrement par</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-228">Liste délimitée par des points-virgules de noms de transformations de transformation dans l’ordre dans lequel ils sont appliqués par ce correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-229"><a href="revision-number-summary.md"><strong>Numéro de révision</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-230">Contient le code de correctif GUID pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="03ee2-231">Elle peut être suivie d’une liste de GUID de code correctif pour les correctifs supprimés lorsque ce correctif est appliqué.</span><span class="sxs-lookup"><span data-stu-id="03ee2-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="03ee2-232">Les codes de correctif sont concaténés, sans délimiteur, en séparant les GUID dans la liste.</span><span class="sxs-lookup"><span data-stu-id="03ee2-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="03ee2-233">Si le package de correctifs contient une table <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , le correctif ne supprime pas les correctifs figurant après le GUID du correctif actuel.</span><span class="sxs-lookup"><span data-stu-id="03ee2-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-234"><a href="last-printed-summary.md"><strong>Dernière impression</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-235">Null</span><span class="sxs-lookup"><span data-stu-id="03ee2-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-236"><a href="create-time-date-summary.md"><strong>Créer une date/heure</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-237">Date et heure de création du fichier correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-238"><a href="last-saved-time-date-summary.md"><strong>Heure/date du dernier enregistrement</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-239">Date et heure système actuelles au moment où le package de correctifs a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="03ee2-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="03ee2-240">Cette valeur est initialement null.</span><span class="sxs-lookup"><span data-stu-id="03ee2-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-241"><a href="page-count-summary.md"><strong>Nombre de pages</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-242">Null</span><span class="sxs-lookup"><span data-stu-id="03ee2-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-243"><a href="word-count-summary.md"><strong>Nombre de mots</strong></a> (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="03ee2-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="03ee2-244">Contient une valeur qui indique la version minimale de Windows Installer requise pour installer le correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="03ee2-245">Un correctif avec une valeur de nombre de mots de 4 requiert Windows Installer version 3,0 ou ultérieure pour appliquer le correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="03ee2-246">La valeur 3 indique que Windows Installer version 2,0 ou ultérieure est requise.</span><span class="sxs-lookup"><span data-stu-id="03ee2-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="03ee2-247">La valeur 2 indique que Windows Installer version 1,2 ou ultérieure est requise.</span><span class="sxs-lookup"><span data-stu-id="03ee2-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="03ee2-248">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="03ee2-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-249"><a href="character-count-summary.md"><strong>Nombre de caractères</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-250">Null</span><span class="sxs-lookup"><span data-stu-id="03ee2-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-251"><a href="creating-application-summary.md"><strong>Création de l’application</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-252">Nom du logiciel utilisé pour créer le correctif.</span><span class="sxs-lookup"><span data-stu-id="03ee2-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ee2-253"><a href="security-summary.md"><strong>Sécurité</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-254">La valeur de cette propriété doit être en lecture seule appliquée à 4.</span><span class="sxs-lookup"><span data-stu-id="03ee2-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ee2-255"><a href="codepage-summary.md"><strong>Courante</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ee2-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="03ee2-256">Valeur numérique de la page de codes ANSI utilisée pour afficher les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="03ee2-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="03ee2-257">Cette propriété doit être définie avant que toutes les propriétés de chaîne ne soient définies dans les informations de résumé.</span><span class="sxs-lookup"><span data-stu-id="03ee2-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




