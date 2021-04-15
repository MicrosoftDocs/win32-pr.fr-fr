---
description: Le tableau ODBCDriver répertorie les pilotes ODBC appartenant à l’installation.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Table ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257f3eec5b60191df727d156572293489aa1956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525780"
---
# <a name="odbcdriver-table"></a><span data-ttu-id="f66ec-103">Table ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="f66ec-103">ODBCDriver Table</span></span>

<span data-ttu-id="f66ec-104">Le tableau ODBCDriver répertorie les pilotes ODBC appartenant à l’installation.</span><span class="sxs-lookup"><span data-stu-id="f66ec-104">The ODBCDriver table lists the ODBC drivers belonging to the installation.</span></span>

<span data-ttu-id="f66ec-105">La table ODBCDriver contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f66ec-105">The ODBCDriver table has the following columns.</span></span>



| <span data-ttu-id="f66ec-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="f66ec-106">Column</span></span>      | <span data-ttu-id="f66ec-107">Type</span><span class="sxs-lookup"><span data-stu-id="f66ec-107">Type</span></span>                         | <span data-ttu-id="f66ec-108">Clé</span><span class="sxs-lookup"><span data-stu-id="f66ec-108">Key</span></span> | <span data-ttu-id="f66ec-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f66ec-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="f66ec-110">Pilote</span><span class="sxs-lookup"><span data-stu-id="f66ec-110">Driver</span></span>      | [<span data-ttu-id="f66ec-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f66ec-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f66ec-112">O</span><span class="sxs-lookup"><span data-stu-id="f66ec-112">Y</span></span>   | <span data-ttu-id="f66ec-113">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-113">N</span></span>        |
| <span data-ttu-id="f66ec-114">-\_</span><span class="sxs-lookup"><span data-stu-id="f66ec-114">Component\_</span></span> | [<span data-ttu-id="f66ec-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f66ec-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f66ec-116">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-116">N</span></span>   | <span data-ttu-id="f66ec-117">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-117">N</span></span>        |
| <span data-ttu-id="f66ec-118">Description</span><span class="sxs-lookup"><span data-stu-id="f66ec-118">Description</span></span> | [<span data-ttu-id="f66ec-119">Text</span><span class="sxs-lookup"><span data-stu-id="f66ec-119">Text</span></span>](text.md)             | <span data-ttu-id="f66ec-120">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-120">N</span></span>   | <span data-ttu-id="f66ec-121">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-121">N</span></span>        |
| <span data-ttu-id="f66ec-122">fichier\_</span><span class="sxs-lookup"><span data-stu-id="f66ec-122">File\_</span></span>      | [<span data-ttu-id="f66ec-123">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f66ec-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="f66ec-124">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-124">N</span></span>   | <span data-ttu-id="f66ec-125">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-125">N</span></span>        |
| <span data-ttu-id="f66ec-126">Configuration des fichiers \_</span><span class="sxs-lookup"><span data-stu-id="f66ec-126">File\_Setup</span></span> | [<span data-ttu-id="f66ec-127">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f66ec-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="f66ec-128">N</span><span class="sxs-lookup"><span data-stu-id="f66ec-128">N</span></span>   | <span data-ttu-id="f66ec-129">O</span><span class="sxs-lookup"><span data-stu-id="f66ec-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f66ec-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f66ec-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f66ec-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Pilote</span><span class="sxs-lookup"><span data-stu-id="f66ec-131"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Driver</span></span>
</dt> <dd>

<span data-ttu-id="f66ec-132">Nom du jeton interne pour le pilote.</span><span class="sxs-lookup"><span data-stu-id="f66ec-132">Internal token name for driver.</span></span> <span data-ttu-id="f66ec-133">Une clé primaire pour la table</span><span class="sxs-lookup"><span data-stu-id="f66ec-133">A primary key for the table</span></span>

</dd> <dt>

<span data-ttu-id="f66ec-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="f66ec-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f66ec-135">Clé externe dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="f66ec-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="f66ec-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="f66ec-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="f66ec-137">Description inscrite pour ce pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="f66ec-137">The description registered for this ODBC driver.</span></span> <span data-ttu-id="f66ec-138">Cette valeur ne peut pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="f66ec-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="f66ec-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="f66ec-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="f66ec-140">Fichier DLL pour les pilotes figurant dans la colonne Driver.</span><span class="sxs-lookup"><span data-stu-id="f66ec-140">The DLL file for drivers listed in the Driver column.</span></span> <span data-ttu-id="f66ec-141">La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f66ec-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="f66ec-142">Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short.</span><span class="sxs-lookup"><span data-stu-id="f66ec-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="f66ec-143">La \| syntaxe SFN LFN ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f66ec-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="f66ec-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuration des fichiers \_</span><span class="sxs-lookup"><span data-stu-id="f66ec-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="f66ec-145">Fichier DLL d’installation du pilote, s’il est différent de celui du pilote.</span><span class="sxs-lookup"><span data-stu-id="f66ec-145">The setup DLL file for the driver if it is different than from Driver.</span></span> <span data-ttu-id="f66ec-146">La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f66ec-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="f66ec-147">Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short.</span><span class="sxs-lookup"><span data-stu-id="f66ec-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="f66ec-148">La \| syntaxe SFN LFN ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f66ec-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f66ec-149">Notes</span><span class="sxs-lookup"><span data-stu-id="f66ec-149">Remarks</span></span>

<span data-ttu-id="f66ec-150">Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="f66ec-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f66ec-151">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f66ec-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f66ec-152">Validation</span><span class="sxs-lookup"><span data-stu-id="f66ec-152">Validation</span></span>

<dl>

[<span data-ttu-id="f66ec-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="f66ec-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f66ec-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="f66ec-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f66ec-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="f66ec-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



