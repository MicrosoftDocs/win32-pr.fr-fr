---
description: L’action InstallODBC installe les pilotes, les traducteurs et les sources de données dans la table ODBCDriver, la table ODBCTranslator et la table ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Action InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521953"
---
# <a name="installodbc-action"></a><span data-ttu-id="fcc72-103">Action InstallODBC</span><span class="sxs-lookup"><span data-stu-id="fcc72-103">InstallODBC Action</span></span>

<span data-ttu-id="fcc72-104">L’action InstallODBC installe les pilotes, les traducteurs et les sources de données dans la table [ODBCDriver](odbcdriver-table.md), la table [ODBCTranslator](odbctranslator-table.md)et la [table ODBCDataSource](odbcdatasource-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcc72-104">The InstallODBC action installs the drivers, translators, and data sources in the [ODBCDriver Table](odbcdriver-table.md), [ODBCTranslator Table](odbctranslator-table.md), and [ODBCDataSource Table](odbcdatasource-table.md).</span></span> <span data-ttu-id="fcc72-105">S’il existe déjà un pilote ou un convertisseur, l’action InstallODBC effectue les appels SQL nécessaires à l’installation.</span><span class="sxs-lookup"><span data-stu-id="fcc72-105">If a driver or translator already exists, the InstallODBC action makes SQL calls necessary for the installation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fcc72-106">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="fcc72-106">Sequence Restrictions</span></span>

<span data-ttu-id="fcc72-107">L’action InstallODBC ne copie pas et ne supprime pas les fichiers, et doit se trouver après les actions qui copient ou suppriment des fichiers.</span><span class="sxs-lookup"><span data-stu-id="fcc72-107">The InstallODBC action does not copy or remove files, and must be after actions that copy or remove files.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fcc72-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="fcc72-108">ActionData Messages</span></span>

<span data-ttu-id="fcc72-109">Le tableau suivant identifie les messages ActionData pour chaque pilote installé.</span><span class="sxs-lookup"><span data-stu-id="fcc72-109">The following table identifies the ActionData messages for each installed driver.</span></span>



| <span data-ttu-id="fcc72-110">Champ</span><span class="sxs-lookup"><span data-stu-id="fcc72-110">Field</span></span>       | <span data-ttu-id="fcc72-111">Description</span><span class="sxs-lookup"><span data-stu-id="fcc72-111">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="fcc72-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-112">\[1\]</span></span>       | <span data-ttu-id="fcc72-113">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="fcc72-113">Driver description.</span></span> <span data-ttu-id="fcc72-114">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="fcc72-114">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="fcc72-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-115">\[2\]</span></span>       | <span data-ttu-id="fcc72-116">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="fcc72-116">ComponentId.</span></span>                                                             |
| <span data-ttu-id="fcc72-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-117">\[3\]</span></span>       | <span data-ttu-id="fcc72-118">Dossier.</span><span class="sxs-lookup"><span data-stu-id="fcc72-118">Folder.</span></span>                                                                  |
| <span data-ttu-id="fcc72-119">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-119">\[4, 5, …\]</span></span> | <span data-ttu-id="fcc72-120">Paires attribut/valeur de [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcc72-120">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="fcc72-121">Le tableau suivant identifie les messages ActionData pour chaque traducteur installé.</span><span class="sxs-lookup"><span data-stu-id="fcc72-121">The following table identifies the ActionData messages for each installed translator.</span></span>



| <span data-ttu-id="fcc72-122">Champ</span><span class="sxs-lookup"><span data-stu-id="fcc72-122">Field</span></span>       | <span data-ttu-id="fcc72-123">Description</span><span class="sxs-lookup"><span data-stu-id="fcc72-123">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="fcc72-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-124">\[1\]</span></span>       | <span data-ttu-id="fcc72-125">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="fcc72-125">Driver description.</span></span> <span data-ttu-id="fcc72-126">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="fcc72-126">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="fcc72-127">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-127">\[2\]</span></span>       | <span data-ttu-id="fcc72-128">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="fcc72-128">ComponentId.</span></span>                                                             |
| <span data-ttu-id="fcc72-129">\[3\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-129">\[3\]</span></span>       | <span data-ttu-id="fcc72-130">Dossier.</span><span class="sxs-lookup"><span data-stu-id="fcc72-130">Folder.</span></span>                                                                  |
| <span data-ttu-id="fcc72-131">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-131">\[4, 5, …\]</span></span> | <span data-ttu-id="fcc72-132">Paires attribut/valeur de [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcc72-132">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

<span data-ttu-id="fcc72-133">Le tableau suivant identifie les messages ActionData pour chaque source de données installée.</span><span class="sxs-lookup"><span data-stu-id="fcc72-133">The following table identifies the ActionData messages for each installed data source.</span></span>



| <span data-ttu-id="fcc72-134">Champ</span><span class="sxs-lookup"><span data-stu-id="fcc72-134">Field</span></span>       | <span data-ttu-id="fcc72-135">Description</span><span class="sxs-lookup"><span data-stu-id="fcc72-135">Description</span></span>                                                              |
|-------------|--------------------------------------------------------------------------|
| <span data-ttu-id="fcc72-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-136">\[1\]</span></span>       | <span data-ttu-id="fcc72-137">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="fcc72-137">Driver description.</span></span> <span data-ttu-id="fcc72-138">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="fcc72-138">The ODBC driver key.</span></span>                                 |
| <span data-ttu-id="fcc72-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-139">\[2\]</span></span>       | <span data-ttu-id="fcc72-140">ComponentID.</span><span class="sxs-lookup"><span data-stu-id="fcc72-140">ComponentId.</span></span>                                                             |
| <span data-ttu-id="fcc72-141">\[3\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-141">\[3\]</span></span>       | <span data-ttu-id="fcc72-142">Inscription : ODBC \_ Add \_ DSN ou ODBC \_ Add \_ sys \_ DSN.</span><span class="sxs-lookup"><span data-stu-id="fcc72-142">Registration: ODBC\_ADD\_DSN or ODBC\_ADD\_SYS\_DSN.</span></span>                     |
| <span data-ttu-id="fcc72-143">\[4, 5,...\]</span><span class="sxs-lookup"><span data-stu-id="fcc72-143">\[4, 5, …\]</span></span> | <span data-ttu-id="fcc72-144">Paires attribut/valeur de [ODBCAttribute](odbcattribute-table.md).</span><span class="sxs-lookup"><span data-stu-id="fcc72-144">Attribute and value pairs from [ODBCAttribute](odbcattribute-table.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fcc72-145">Notes</span><span class="sxs-lookup"><span data-stu-id="fcc72-145">Remarks</span></span>

<span data-ttu-id="fcc72-146">Le gestionnaire de pilotes ODBC doit être créé dans le package Microsoft installer et un composant nommé ODBCDriverManager doit être inclus.</span><span class="sxs-lookup"><span data-stu-id="fcc72-146">The ODBC Driver Manager must be authored in the Microsoft Installer package and a component named ODBCDriverManager must be included.</span></span> <span data-ttu-id="fcc72-147">Le gestionnaire est installé si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fcc72-147">The manager is installed if necessary.</span></span>

<span data-ttu-id="fcc72-148">Pour renommer le composant, définissez une propriété nommée ODBCDriverManager sur le nouveau nom du composant.</span><span class="sxs-lookup"><span data-stu-id="fcc72-148">To rename the component, set a property named ODBCDriverManager to the new name of the component.</span></span> <span data-ttu-id="fcc72-149">Si un gestionnaire de pilotes ODBC 64 bits doit être installé, le composant qui le contient doit être nommé ODBCDriverManager64.</span><span class="sxs-lookup"><span data-stu-id="fcc72-149">If a 64-bit ODBC Driver Manager is to be installed, the component that carries it should be named ODBCDriverManager64.</span></span>

-   <span data-ttu-id="fcc72-150">L’action InstallODBC interroge la [table ODBCDataSource](odbcdatasource-table.md) et la [table ODBCSourceAttribute](odbcsourceattribute-table.md) pour chaque source de données à installer, ainsi que les attributs de la source de données.</span><span class="sxs-lookup"><span data-stu-id="fcc72-150">The InstallODBC action queries the [ODBCDataSource Table](odbcdatasource-table.md) and the [ODBCSourceAttribute Table](odbcsourceattribute-table.md) for each data source to be installed, and the attributes of the data source.</span></span>
-   <span data-ttu-id="fcc72-151">L’action InstallODBC interroge la [table ODBCDriver](odbcdriver-table.md) et la [table ODBCTranslator](odbctranslator-table.md) pour chaque pilote et traducteur sélectionné pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="fcc72-151">The InstallODBC action queries the [ODBCDriver Table](odbcdriver-table.md) and the [ODBCTranslator Table](odbctranslator-table.md) for each driver and translator that is selected for installation.</span></span>
-   <span data-ttu-id="fcc72-152">L’action InstallODBC interroge la [table ODBCAttribute](odbcattribute-table.md) pour obtenir les attributs des pilotes et des traducteurs.</span><span class="sxs-lookup"><span data-stu-id="fcc72-152">The InstallODBC action queries the [ODBCAttribute Table](odbcattribute-table.md) for the attributes of the drivers and translators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcc72-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcc72-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcc72-154">Exemples de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fcc72-154">Windows Installer Examples</span></span>](windows-installer-examples.md)
</dt> </dl>

 

 



