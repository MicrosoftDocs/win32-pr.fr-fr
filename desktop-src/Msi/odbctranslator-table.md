---
description: Le tableau ODBCTranslator répertorie les convertisseurs ODBC appartenant à l’installation.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Table ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535042"
---
# <a name="odbctranslator-table"></a><span data-ttu-id="ecbac-103">Table ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="ecbac-103">ODBCTranslator Table</span></span>

<span data-ttu-id="ecbac-104">Le tableau ODBCTranslator répertorie les convertisseurs ODBC appartenant à l’installation.</span><span class="sxs-lookup"><span data-stu-id="ecbac-104">The ODBCTranslator table lists the ODBC translators belonging to the installation.</span></span>

<span data-ttu-id="ecbac-105">La table ODBCTranslator contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ecbac-105">The ODBCTranslator table has the following columns.</span></span>



| <span data-ttu-id="ecbac-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="ecbac-106">Column</span></span>      | <span data-ttu-id="ecbac-107">Type</span><span class="sxs-lookup"><span data-stu-id="ecbac-107">Type</span></span>                         | <span data-ttu-id="ecbac-108">Clé</span><span class="sxs-lookup"><span data-stu-id="ecbac-108">Key</span></span> | <span data-ttu-id="ecbac-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="ecbac-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="ecbac-110">Convertisseur</span><span class="sxs-lookup"><span data-stu-id="ecbac-110">Translator</span></span>  | [<span data-ttu-id="ecbac-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ecbac-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="ecbac-112">O</span><span class="sxs-lookup"><span data-stu-id="ecbac-112">Y</span></span>   | <span data-ttu-id="ecbac-113">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-113">N</span></span>        |
| <span data-ttu-id="ecbac-114">-\_</span><span class="sxs-lookup"><span data-stu-id="ecbac-114">Component\_</span></span> | [<span data-ttu-id="ecbac-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ecbac-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="ecbac-116">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-116">N</span></span>   | <span data-ttu-id="ecbac-117">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-117">N</span></span>        |
| <span data-ttu-id="ecbac-118">Description</span><span class="sxs-lookup"><span data-stu-id="ecbac-118">Description</span></span> | [<span data-ttu-id="ecbac-119">Text</span><span class="sxs-lookup"><span data-stu-id="ecbac-119">Text</span></span>](text.md)             | <span data-ttu-id="ecbac-120">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-120">N</span></span>   | <span data-ttu-id="ecbac-121">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-121">N</span></span>        |
| <span data-ttu-id="ecbac-122">fichier\_</span><span class="sxs-lookup"><span data-stu-id="ecbac-122">File\_</span></span>      | [<span data-ttu-id="ecbac-123">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ecbac-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="ecbac-124">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-124">N</span></span>   | <span data-ttu-id="ecbac-125">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-125">N</span></span>        |
| <span data-ttu-id="ecbac-126">Configuration des fichiers \_</span><span class="sxs-lookup"><span data-stu-id="ecbac-126">File\_Setup</span></span> | [<span data-ttu-id="ecbac-127">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ecbac-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="ecbac-128">N</span><span class="sxs-lookup"><span data-stu-id="ecbac-128">N</span></span>   | <span data-ttu-id="ecbac-129">O</span><span class="sxs-lookup"><span data-stu-id="ecbac-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ecbac-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ecbac-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ecbac-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span><span class="sxs-lookup"><span data-stu-id="ecbac-131"><span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Translator</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-132">Nom de jeton interne pour le traducteur.</span><span class="sxs-lookup"><span data-stu-id="ecbac-132">Internal token name for translator.</span></span> <span data-ttu-id="ecbac-133">Clé primaire pour la table.</span><span class="sxs-lookup"><span data-stu-id="ecbac-133">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="ecbac-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="ecbac-134"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-135">Clé externe dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="ecbac-135">External key into the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="ecbac-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="ecbac-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-137">Description enregistrée pour ce convertisseur de pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="ecbac-137">The description registered for this ODBC driver translator.</span></span> <span data-ttu-id="ecbac-138">Cette valeur ne peut pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="ecbac-138">This value cannot be localized.</span></span>

</dd> <dt>

<span data-ttu-id="ecbac-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="ecbac-139"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-140">Fichier DLL pour le transfert listé dans la colonne traducteur.</span><span class="sxs-lookup"><span data-stu-id="ecbac-140">The DLL file for the transfer listed in the Translator column.</span></span> <span data-ttu-id="ecbac-141">La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecbac-141">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="ecbac-142">Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short.</span><span class="sxs-lookup"><span data-stu-id="ecbac-142">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="ecbac-143">La \| syntaxe SFN LFN ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="ecbac-143">The SFN\|LFN syntax cannot be used.</span></span>

</dd> <dt>

<span data-ttu-id="ecbac-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuration des fichiers \_</span><span class="sxs-lookup"><span data-stu-id="ecbac-144"><span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>File\_Setup</span></span>
</dt> <dd>

<span data-ttu-id="ecbac-145">Fichier DLL d’installation pour le convertisseur, s’il est différent de la colonne translator.</span><span class="sxs-lookup"><span data-stu-id="ecbac-145">The setup DLL file for the translator if it is different from the Translator column.</span></span> <span data-ttu-id="ecbac-146">La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecbac-146">The File\_ column is an external key into the [File table](file-table.md).</span></span> <span data-ttu-id="ecbac-147">Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short.</span><span class="sxs-lookup"><span data-stu-id="ecbac-147">The filename entered in the Filename column of that File table record must be in the short filename format.</span></span> <span data-ttu-id="ecbac-148">La \| syntaxe SFN LFN ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="ecbac-148">The SFN\|LFN syntax cannot be used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecbac-149">Notes</span><span class="sxs-lookup"><span data-stu-id="ecbac-149">Remarks</span></span>

<span data-ttu-id="ecbac-150">Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ecbac-150">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="ecbac-151">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecbac-151">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="ecbac-152">Validation</span><span class="sxs-lookup"><span data-stu-id="ecbac-152">Validation</span></span>

<dl>

[<span data-ttu-id="ecbac-153">ICE03</span><span class="sxs-lookup"><span data-stu-id="ecbac-153">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ecbac-154">ICE06</span><span class="sxs-lookup"><span data-stu-id="ecbac-154">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ecbac-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="ecbac-155">ICE32</span></span>](ice32.md)  
</dl>

 

 



