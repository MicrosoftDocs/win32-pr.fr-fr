---
description: Le tableau ODBCDataSource répertorie les sources de données appartenant à l’installation.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Table ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519349"
---
# <a name="odbcdatasource-table"></a><span data-ttu-id="f4b41-103">Table ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="f4b41-103">ODBCDataSource Table</span></span>

<span data-ttu-id="f4b41-104">Le tableau ODBCDataSource répertorie les sources de données appartenant à l’installation.</span><span class="sxs-lookup"><span data-stu-id="f4b41-104">The ODBCDataSource table lists the data sources belonging to the installation.</span></span>

<span data-ttu-id="f4b41-105">La table ODBCDataSource contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4b41-105">The ODBCDataSource table has the following columns.</span></span>



| <span data-ttu-id="f4b41-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="f4b41-106">Column</span></span>            | <span data-ttu-id="f4b41-107">Type</span><span class="sxs-lookup"><span data-stu-id="f4b41-107">Type</span></span>                         | <span data-ttu-id="f4b41-108">Clé</span><span class="sxs-lookup"><span data-stu-id="f4b41-108">Key</span></span> | <span data-ttu-id="f4b41-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f4b41-109">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="f4b41-110">DataSource</span><span class="sxs-lookup"><span data-stu-id="f4b41-110">DataSource</span></span>        | [<span data-ttu-id="f4b41-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f4b41-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f4b41-112">O</span><span class="sxs-lookup"><span data-stu-id="f4b41-112">Y</span></span>   | <span data-ttu-id="f4b41-113">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-113">N</span></span>        |
| <span data-ttu-id="f4b41-114">-\_</span><span class="sxs-lookup"><span data-stu-id="f4b41-114">Component\_</span></span>       | [<span data-ttu-id="f4b41-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f4b41-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f4b41-116">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-116">N</span></span>   | <span data-ttu-id="f4b41-117">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-117">N</span></span>        |
| <span data-ttu-id="f4b41-118">Description</span><span class="sxs-lookup"><span data-stu-id="f4b41-118">Description</span></span>       | [<span data-ttu-id="f4b41-119">Text</span><span class="sxs-lookup"><span data-stu-id="f4b41-119">Text</span></span>](text.md)             | <span data-ttu-id="f4b41-120">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-120">N</span></span>   | <span data-ttu-id="f4b41-121">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-121">N</span></span>        |
| <span data-ttu-id="f4b41-122">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="f4b41-122">DriverDescription</span></span> | [<span data-ttu-id="f4b41-123">Text</span><span class="sxs-lookup"><span data-stu-id="f4b41-123">Text</span></span>](text.md)             | <span data-ttu-id="f4b41-124">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-124">N</span></span>   | <span data-ttu-id="f4b41-125">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-125">N</span></span>        |
| <span data-ttu-id="f4b41-126">Inscription</span><span class="sxs-lookup"><span data-stu-id="f4b41-126">Registration</span></span>      | [<span data-ttu-id="f4b41-127">Integer</span><span class="sxs-lookup"><span data-stu-id="f4b41-127">Integer</span></span>](integer.md)       | <span data-ttu-id="f4b41-128">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-128">N</span></span>   | <span data-ttu-id="f4b41-129">N</span><span class="sxs-lookup"><span data-stu-id="f4b41-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f4b41-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f4b41-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f4b41-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>Mustek</span><span class="sxs-lookup"><span data-stu-id="f4b41-131"><span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource</span></span>
</dt> <dd>

<span data-ttu-id="f4b41-132">Nom de jeton interne de la source de données.</span><span class="sxs-lookup"><span data-stu-id="f4b41-132">Internal token name for data source.</span></span> <span data-ttu-id="f4b41-133">Clé primaire pour la table.</span><span class="sxs-lookup"><span data-stu-id="f4b41-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="f4b41-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="f4b41-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f4b41-135">Clé externe dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4b41-135">External key into the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4b41-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="f4b41-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="f4b41-137">Description inscrite pour cette source de données.</span><span class="sxs-lookup"><span data-stu-id="f4b41-137">The description registered for this data source.</span></span> <span data-ttu-id="f4b41-138">Cette valeur ne peut pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="f4b41-138">This value cannot be localized.</span></span> <span data-ttu-id="f4b41-139">Les descriptions de source de données ODBC ne peuvent pas dépasser la \_ longueur maximale de \_ DSN SQL \_ .</span><span class="sxs-lookup"><span data-stu-id="f4b41-139">ODBC data source descriptions cannot exceed SQL\_MAX\_DSN\_LENGTH.</span></span>

</dd> <dt>

<span data-ttu-id="f4b41-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span><span class="sxs-lookup"><span data-stu-id="f4b41-140"><span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription</span></span>
</dt> <dd>

<span data-ttu-id="f4b41-141">Pilote associé qui peut être préexistant.</span><span class="sxs-lookup"><span data-stu-id="f4b41-141">Associated driver which may be pre-existing.</span></span> <span data-ttu-id="f4b41-142">Cette valeur ne peut pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="f4b41-142">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="f4b41-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Abonnement</span><span class="sxs-lookup"><span data-stu-id="f4b41-143"><span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registration</span></span>
</dt> <dd>

<span data-ttu-id="f4b41-144">Ce champ spécifie le type d’inscription de la source de données.</span><span class="sxs-lookup"><span data-stu-id="f4b41-144">This field specifies the type of registration for the data source.</span></span>



| <span data-ttu-id="f4b41-145">Constante</span><span class="sxs-lookup"><span data-stu-id="f4b41-145">Constant</span></span>                                      | <span data-ttu-id="f4b41-146">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="f4b41-146">Hexadecimal</span></span> | <span data-ttu-id="f4b41-147">Decimal</span><span class="sxs-lookup"><span data-stu-id="f4b41-147">Decimal</span></span> | <span data-ttu-id="f4b41-148">Description</span><span class="sxs-lookup"><span data-stu-id="f4b41-148">Description</span></span>                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| <span data-ttu-id="f4b41-149">**msidbODBCDataSourceRegistrationPerMachine**</span><span class="sxs-lookup"><span data-stu-id="f4b41-149">**msidbODBCDataSourceRegistrationPerMachine**</span></span> | <span data-ttu-id="f4b41-150">0x000</span><span class="sxs-lookup"><span data-stu-id="f4b41-150">0x000</span></span>       | <span data-ttu-id="f4b41-151">0</span><span class="sxs-lookup"><span data-stu-id="f4b41-151">0</span></span>       | <span data-ttu-id="f4b41-152">La source de données est inscrite par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f4b41-152">Data source is registered per machine.</span></span> |
| <span data-ttu-id="f4b41-153">**msidbODBCDataSourceRegistrationPerUser**</span><span class="sxs-lookup"><span data-stu-id="f4b41-153">**msidbODBCDataSourceRegistrationPerUser**</span></span>    | <span data-ttu-id="f4b41-154">0x001</span><span class="sxs-lookup"><span data-stu-id="f4b41-154">0x001</span></span>       | <span data-ttu-id="f4b41-155">1</span><span class="sxs-lookup"><span data-stu-id="f4b41-155">1</span></span>       | <span data-ttu-id="f4b41-156">La source de données est inscrite par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4b41-156">Data source is registered per user.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4b41-157">Notes</span><span class="sxs-lookup"><span data-stu-id="f4b41-157">Remarks</span></span>

<span data-ttu-id="f4b41-158">Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="f4b41-158">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f4b41-159">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4b41-159">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f4b41-160">Validation</span><span class="sxs-lookup"><span data-stu-id="f4b41-160">Validation</span></span>

<dl>

[<span data-ttu-id="f4b41-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="f4b41-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f4b41-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="f4b41-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f4b41-163">ICE32</span><span class="sxs-lookup"><span data-stu-id="f4b41-163">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f4b41-164">ICE45</span><span class="sxs-lookup"><span data-stu-id="f4b41-164">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="f4b41-165">ICE98</span><span class="sxs-lookup"><span data-stu-id="f4b41-165">ICE98</span></span>](ice98.md)  
</dl>

 

 



