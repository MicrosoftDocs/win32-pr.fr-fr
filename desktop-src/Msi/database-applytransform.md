---
description: La méthode ApplyTransform de l’objet de base de données applique la transformation à cette base de données.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. ApplyTransform, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 81eda2f2c868b4ccd637ec117850c2beea14eef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544110"
---
# <a name="databaseapplytransform-method"></a><span data-ttu-id="97aa5-103">Database. ApplyTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="97aa5-103">Database.ApplyTransform method</span></span>

<span data-ttu-id="97aa5-104">La méthode **ApplyTransform** de l’objet [**de base de données**](database-object.md) applique la transformation à cette base de données.</span><span class="sxs-lookup"><span data-stu-id="97aa5-104">The **ApplyTransform** method of the [**Database**](database-object.md) object applies the transform to this database.</span></span>

## <a name="syntax"></a><span data-ttu-id="97aa5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97aa5-105">Syntax</span></span>


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a><span data-ttu-id="97aa5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97aa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97aa5-107">*storage*</span><span class="sxs-lookup"><span data-stu-id="97aa5-107">*storage*</span></span> 
</dt> <dd>

<span data-ttu-id="97aa5-108">Chemin d’accès au fichier de transformation en cours d’application.</span><span class="sxs-lookup"><span data-stu-id="97aa5-108">Path to the transform file being applied.</span></span> <span data-ttu-id="97aa5-109">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="97aa5-109">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="97aa5-110">*errorConditions*</span><span class="sxs-lookup"><span data-stu-id="97aa5-110">*errorConditions*</span></span> 
</dt> <dd>

<span data-ttu-id="97aa5-111">Spécifie les conditions d’erreur qui doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="97aa5-111">Specifies the error conditions that are to be suppressed.</span></span> <span data-ttu-id="97aa5-112">Spécifiez en tant que combinaison des valeurs entières suivantes.</span><span class="sxs-lookup"><span data-stu-id="97aa5-112">Specify as a combination of the following integer values.</span></span>



| <span data-ttu-id="97aa5-113">État d’erreur</span><span class="sxs-lookup"><span data-stu-id="97aa5-113">Error condition</span></span>                                                                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="97aa5-114">Signification</span><span class="sxs-lookup"><span data-stu-id="97aa5-114">Meaning</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <span data-ttu-id="97aa5-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-115"><dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt></span></span> </dl>                                 | <span data-ttu-id="97aa5-116">Ajoute une ligne qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="97aa5-116">Adds a row that already exists.</span></span><br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <span data-ttu-id="97aa5-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-117"><dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="97aa5-118">Supprime une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="97aa5-118">Deletes a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <span data-ttu-id="97aa5-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-119"><dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt></span></span> </dl>                         | <span data-ttu-id="97aa5-120">Ajoute une table qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="97aa5-120">Adds a table that already exists.</span></span><br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <span data-ttu-id="97aa5-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-121"><dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="97aa5-122">Supprime une table qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="97aa5-122">Deletes a table that does not exist.</span></span><br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <span data-ttu-id="97aa5-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-123"><dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt></span></span> </dl>         | <span data-ttu-id="97aa5-124">Met à jour une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="97aa5-124">Updates a row that does not exist.</span></span><br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <span data-ttu-id="97aa5-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-125"><dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt></span></span> </dl>                                 | <span data-ttu-id="97aa5-126">Les pages de codes de transformation et de base de données ne correspondent pas et n’ont aucune page de codes neutre.</span><span class="sxs-lookup"><span data-stu-id="97aa5-126">Transform and database code pages do not match and neither has a neutral code page.</span></span><br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <span data-ttu-id="97aa5-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-127"><dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt></span></span> </dl>                                     | <span data-ttu-id="97aa5-128">Crée la [ \_ table TransformView](-transformview-table.md)temporaire.</span><span class="sxs-lookup"><span data-stu-id="97aa5-128">Creates the temporary [\_TransformView table](-transformview-table.md).</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97aa5-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97aa5-129">Return value</span></span>

<span data-ttu-id="97aa5-130">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="97aa5-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97aa5-131">Notes</span><span class="sxs-lookup"><span data-stu-id="97aa5-131">Remarks</span></span>

<span data-ttu-id="97aa5-132">La méthode **ApplyTransform** retarde la transformation des tables jusqu’au dernier moment possible.</span><span class="sxs-lookup"><span data-stu-id="97aa5-132">The **ApplyTransform** method delays transforming tables until the last possible moment.</span></span> <span data-ttu-id="97aa5-133">Les étapes effectuées dans **ApplyTransform** sont de transformer immédiatement les catalogues de tables et de colonnes pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="97aa5-133">The steps taken in **ApplyTransform** are to immediately transform the table and column catalogs for the database.</span></span> <span data-ttu-id="97aa5-134">Les catalogues de tables et de colonnes sont mis à jour en fonction de la table qui est ajoutée ou supprimée et de la colonne ajoutée (aucune suppression de colonnes n’est autorisée).</span><span class="sxs-lookup"><span data-stu-id="97aa5-134">The table and column catalogs are updated according to which table is added or deleted and which column is added (no deletion of columns is allowed).</span></span> <span data-ttu-id="97aa5-135">Si une table est actuellement chargée en mémoire et doit être transformée, elle est transformée.</span><span class="sxs-lookup"><span data-stu-id="97aa5-135">If a table is currently loaded in memory and needs to be transformed, it is transformed.</span></span> <span data-ttu-id="97aa5-136">Dans le cas contraire, l’état de la table a la valeur, ce qui nécessite une transformation, de sorte que lorsque la table est chargée, ou lorsque la base de données est validée, la transformation est appliquée.</span><span class="sxs-lookup"><span data-stu-id="97aa5-136">Otherwise, the table state is set to that requiring a transform so that when the table is loaded, or when the database is committed, the transform is applied.</span></span> <span data-ttu-id="97aa5-137">La transformation dans cette instance signifie que les données (ligne) réelles de la table sont ajoutées, supprimées ou mises à jour.</span><span class="sxs-lookup"><span data-stu-id="97aa5-137">Transform in this instance means that the actual (row) data of the table is added, deleted, or updated.</span></span>

<span data-ttu-id="97aa5-138">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="97aa5-138">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="97aa5-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97aa5-139">Requirements</span></span>



| <span data-ttu-id="97aa5-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97aa5-140">Requirement</span></span> | <span data-ttu-id="97aa5-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="97aa5-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97aa5-142">Version</span><span class="sxs-lookup"><span data-stu-id="97aa5-142">Version</span></span><br/> | <span data-ttu-id="97aa5-143">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97aa5-143">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97aa5-144">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="97aa5-144">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97aa5-145">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="97aa5-145">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="97aa5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="97aa5-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="97aa5-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97aa5-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="97aa5-148">IID</span><span class="sxs-lookup"><span data-stu-id="97aa5-148">IID</span></span><br/>     | <span data-ttu-id="97aa5-149">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="97aa5-149">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="97aa5-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97aa5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97aa5-151">**Base de données**</span><span class="sxs-lookup"><span data-stu-id="97aa5-151">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="97aa5-152">Transformations de base de données</span><span class="sxs-lookup"><span data-stu-id="97aa5-152">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




