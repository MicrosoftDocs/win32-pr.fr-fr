---
description: La méthode CreateTransformSummaryInfo de l’objet de base de données crée et remplit le flux d’informations de synthèse d’un fichier de transformation existant. Cette méthode remplit les propriétés avec les ProductCode et ProductVersion de base et de référence.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. CreateTransformSummaryInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541059"
---
# <a name="databasecreatetransformsummaryinfo-method"></a><span data-ttu-id="4b09b-104">Database. CreateTransformSummaryInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="4b09b-104">Database.CreateTransformSummaryInfo method</span></span>

<span data-ttu-id="4b09b-105">La méthode **CreateTransformSummaryInfo** de l’objet [**de base de données**](database-object.md) crée et remplit le flux d’informations de synthèse d’un fichier de transformation existant.</span><span class="sxs-lookup"><span data-stu-id="4b09b-105">The **CreateTransformSummaryInfo** method of the [**Database**](database-object.md) object creates and populates the summary information stream of an existing transform file.</span></span> <span data-ttu-id="4b09b-106">Cette méthode remplit les propriétés avec les [**ProductCode**](productcode.md) et [**ProductVersion**](productversion.md)de base et de référence.</span><span class="sxs-lookup"><span data-stu-id="4b09b-106">This method fills in the properties with the base and reference [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b09b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b09b-107">Syntax</span></span>


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a><span data-ttu-id="4b09b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b09b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b09b-109">*reference*</span><span class="sxs-lookup"><span data-stu-id="4b09b-109">*reference*</span></span> 
</dt> <dd>

<span data-ttu-id="4b09b-110">Base de données requise qui n’inclut pas les modifications.</span><span class="sxs-lookup"><span data-stu-id="4b09b-110">Required database that does not include the changes.</span></span>

</dd> <dt>

<span data-ttu-id="4b09b-111">*storage*</span><span class="sxs-lookup"><span data-stu-id="4b09b-111">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="4b09b-112">Nom du fichier de transformation généré.</span><span class="sxs-lookup"><span data-stu-id="4b09b-112">The name of the generated transform file.</span></span> <span data-ttu-id="4b09b-113">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="4b09b-113">This is optional.</span></span>

</dd> <dt>

<span data-ttu-id="4b09b-114">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="4b09b-114">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="4b09b-115">Conditions d’erreur requises qui doivent être supprimées lors de l’application de la transformation.</span><span class="sxs-lookup"><span data-stu-id="4b09b-115">Required error conditions that should be suppressed when the transform is applied.</span></span> <span data-ttu-id="4b09b-116">Combinez une ou plusieurs des valeurs de condition d’erreur suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b09b-116">Combine one or more of the following error condition values.</span></span>



| <span data-ttu-id="4b09b-117">Nom de la condition d’erreur</span><span class="sxs-lookup"><span data-stu-id="4b09b-117">Error condition name</span></span>                                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="4b09b-118">Signification</span><span class="sxs-lookup"><span data-stu-id="4b09b-118">Meaning</span></span>                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <span data-ttu-id="4b09b-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-119"><dt>**msiTransformErrorNone**</dt> <dt>0</dt></span></span> </dl>                                                                         | <span data-ttu-id="4b09b-120">Aucune des conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b09b-120">None of the following conditions.</span></span><br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="4b09b-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-121"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt></span></span> </dl>                                 | <span data-ttu-id="4b09b-122">Ajoute une ligne qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4b09b-122">Adds a row that already exists.</span></span><br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="4b09b-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-123"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="4b09b-124">Supprime une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4b09b-124">Deletes a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="4b09b-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-125"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="4b09b-126">Ajoute une table qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4b09b-126">Adds a table that already exists.</span></span><br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="4b09b-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-127"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="4b09b-128">Supprime une table qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4b09b-128">Deletes a table that does not exist.</span></span><br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="4b09b-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-129"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt></span></span> </dl>        | <span data-ttu-id="4b09b-130">Met à jour une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4b09b-130">Updates a row that does not exist.</span></span><br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="4b09b-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-131"><dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt></span></span> </dl>                                | <span data-ttu-id="4b09b-132">Les pages de codes de transformation et de base de données ne correspondent pas et aucune page de codes n’est neutre.</span><span class="sxs-lookup"><span data-stu-id="4b09b-132">Transform and database code pages do not match and neither code page is neutral.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4b09b-133">*validation*</span><span class="sxs-lookup"><span data-stu-id="4b09b-133">*validation*</span></span> 
</dt> <dd>

<span data-ttu-id="4b09b-134">Obligatoire lorsque la transformation est appliquée à une base de données ; indique les propriétés qui doivent être validées pour vérifier que cette transformation peut être appliquée à la base de données.</span><span class="sxs-lookup"><span data-stu-id="4b09b-134">Required when the transform is applied to a database; shows which properties should be validated to verify that this transform can be applied to the database.</span></span> <span data-ttu-id="4b09b-135">Les propriétés sont toutes contenues dans le [jeu de propriétés de flux d’informations de synthèse](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="4b09b-135">The properties are all contained in the [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="4b09b-136">Combinez une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b09b-136">Combine one or more of the following values.</span></span>



| <span data-ttu-id="4b09b-137">Indicateur de validation</span><span class="sxs-lookup"><span data-stu-id="4b09b-137">Validation flag</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="4b09b-138">Signification</span><span class="sxs-lookup"><span data-stu-id="4b09b-138">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <span data-ttu-id="4b09b-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-139"><dt>**msiTransformValidationNone**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="4b09b-140">Aucune validation n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="4b09b-140">No validation done.</span></span><br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <span data-ttu-id="4b09b-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-141"><dt>**msiTransformValidationLanguage**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="4b09b-142">La langue par défaut doit correspondre à la base de données de base.</span><span class="sxs-lookup"><span data-stu-id="4b09b-142">Default language must match base database.</span></span><br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <span data-ttu-id="4b09b-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-143"><dt>**msiTransformValidationProduct**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="4b09b-144">Le produit doit correspondre à la base de données de base.</span><span class="sxs-lookup"><span data-stu-id="4b09b-144">Product must match base database.</span></span><br/>          |



 

<span data-ttu-id="4b09b-145">Pour valider la version du produit, commencez par choisir un ou plusieurs de ces trois indicateurs pour indiquer la quantité de la version à vérifier.</span><span class="sxs-lookup"><span data-stu-id="4b09b-145">To validate product version, first choose one or more of these three flags to indicate how much of the version is to be verified.</span></span>



| <span data-ttu-id="4b09b-146">Indicateur de validation</span><span class="sxs-lookup"><span data-stu-id="4b09b-146">Validation flag</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="4b09b-147">Signification</span><span class="sxs-lookup"><span data-stu-id="4b09b-147">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <span data-ttu-id="4b09b-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-148"><dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt></span></span> </dl>      | <span data-ttu-id="4b09b-149">Vérifie uniquement la version principale.</span><span class="sxs-lookup"><span data-stu-id="4b09b-149">Checks major version only.</span></span><br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <span data-ttu-id="4b09b-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-150"><dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt></span></span> </dl>     | <span data-ttu-id="4b09b-151">Vérifie uniquement la version majeure et la version mineure.</span><span class="sxs-lookup"><span data-stu-id="4b09b-151">Checks major and minor version only.</span></span><br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <span data-ttu-id="4b09b-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-152"><dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt></span></span> </dl> | <span data-ttu-id="4b09b-153">Vérifie les versions majeures, mineures et mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4b09b-153">Checks major, minor, and update versions.</span></span><br/> |



 

<span data-ttu-id="4b09b-154">Choisissez ensuite l’une des options suivantes pour indiquer la relation requise entre la version du produit de la base de données à laquelle la transformation est appliquée et celle de la base de données de base.</span><span class="sxs-lookup"><span data-stu-id="4b09b-154">Then choose one of the following to indicate the required relationship between the product version of the database the transform is being applied to and that of the base database.</span></span>



| <span data-ttu-id="4b09b-155">Indicateur de validation</span><span class="sxs-lookup"><span data-stu-id="4b09b-155">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="4b09b-156">Signification</span><span class="sxs-lookup"><span data-stu-id="4b09b-156">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <span data-ttu-id="4b09b-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-157"><dt>**msiTransformValidationLess**</dt> <dt>64</dt></span></span> </dl>                                          | <span data-ttu-id="4b09b-158">Version appliquée < version de base</span><span class="sxs-lookup"><span data-stu-id="4b09b-158">Applied version < base version</span></span><br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <span data-ttu-id="4b09b-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-159"><dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt></span></span> </dl>             | <span data-ttu-id="4b09b-160">Version appliquée <= version de base</span><span class="sxs-lookup"><span data-stu-id="4b09b-160">Applied version <= base version</span></span><br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <span data-ttu-id="4b09b-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-161"><dt>**msiTransformValidationEqual**</dt> <dt>256</dt></span></span> </dl>                                     | <span data-ttu-id="4b09b-162">Version appliquée = version de base</span><span class="sxs-lookup"><span data-stu-id="4b09b-162">Applied version = base version</span></span><br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <span data-ttu-id="4b09b-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-163"><dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt></span></span> </dl> | <span data-ttu-id="4b09b-164">Version appliquée >= version de base</span><span class="sxs-lookup"><span data-stu-id="4b09b-164">Applied version >= base version</span></span><br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <span data-ttu-id="4b09b-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-165"><dt>**msiTransformValidationGreater**</dt> <dt>1024</dt></span></span> </dl>                            | <span data-ttu-id="4b09b-166">Version appliquée > version de base</span><span class="sxs-lookup"><span data-stu-id="4b09b-166">Applied version > base version</span></span><br/>  |



 

<span data-ttu-id="4b09b-167">Pour valider l’application de la transformation à un package ayant la [**UpgradeCode**](upgradecode.md)appropriée, définissez l’indicateur suivant.</span><span class="sxs-lookup"><span data-stu-id="4b09b-167">To validate that the transform is being applied to a package having the appropriate [**UpgradeCode**](upgradecode.md), set the following flag.</span></span>



| <span data-ttu-id="4b09b-168">Indicateur de validation</span><span class="sxs-lookup"><span data-stu-id="4b09b-168">Validation flag</span></span>                                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="4b09b-169">Signification</span><span class="sxs-lookup"><span data-stu-id="4b09b-169">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <span data-ttu-id="4b09b-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-170"><dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="4b09b-171">Valide le fait que la transformation soit la [**UpgradeCode**](upgradecode.md)appropriée.</span><span class="sxs-lookup"><span data-stu-id="4b09b-171">Validates that the transform is the appropriate [**UpgradeCode**](upgradecode.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b09b-172">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b09b-172">Return value</span></span>

<span data-ttu-id="4b09b-173">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4b09b-173">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b09b-174">Notes</span><span class="sxs-lookup"><span data-stu-id="4b09b-174">Remarks</span></span>

<span data-ttu-id="4b09b-175">Pour créer un flux d’informations de synthèse pour une transformation, les propriétés [**ProductCode**](productcode.md) et [**ProductVersion**](productversion.md) doivent être définies dans les tables de [Propriétés](property-table.md) des bases de données de base et de référence.</span><span class="sxs-lookup"><span data-stu-id="4b09b-175">To create a summary information stream for a transform, the [**ProductCode**](productcode.md) and [**ProductVersion**](productversion.md) properties must be defined in the [Property](property-table.md) tables of both the base and reference databases.</span></span> <span data-ttu-id="4b09b-176">Si msiTransformValidationUpgradeCode est utilisé, la propriété [**UpgradeCode**](upgradecode.md) doit être définie dans les deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="4b09b-176">If msiTransformValidationUpgradeCode is used, the [**UpgradeCode**](upgradecode.md) property must be defined in both databases.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b09b-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b09b-177">Requirements</span></span>



| <span data-ttu-id="4b09b-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b09b-178">Requirement</span></span> | <span data-ttu-id="4b09b-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b09b-179">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b09b-180">Version</span><span class="sxs-lookup"><span data-stu-id="4b09b-180">Version</span></span><br/> | <span data-ttu-id="4b09b-181">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b09b-181">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4b09b-182">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4b09b-182">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4b09b-183">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b09b-183">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="4b09b-184">DLL</span><span class="sxs-lookup"><span data-stu-id="4b09b-184">DLL</span></span><br/>     | <dl> <span data-ttu-id="4b09b-185"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b09b-185"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="4b09b-186">IID</span><span class="sxs-lookup"><span data-stu-id="4b09b-186">IID</span></span><br/>     | <span data-ttu-id="4b09b-187">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4b09b-187">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="4b09b-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b09b-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b09b-189">Transformations de base de données</span><span class="sxs-lookup"><span data-stu-id="4b09b-189">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




