---
description: Obtenez une base de données de module de fusion vide. Vous pouvez utiliser le fichier Schema. msm fourni avec le kit de développement logiciel (SDK) Windows Installer en tant que base de données de départ pour votre module de fusion. Pour plus d’informations, consultez SDK Windows Components for Windows Installer Developers.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Obtention de bases de données de module de fusion vides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531687"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="291e7-105">Obtention de bases de données de module de fusion vides</span><span class="sxs-lookup"><span data-stu-id="291e7-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="291e7-106">Obtenez une base de données de module de fusion vide.</span><span class="sxs-lookup"><span data-stu-id="291e7-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="291e7-107">Vous pouvez utiliser le fichier Schema. msm fourni avec le kit de développement logiciel (SDK) Windows Installer en tant que base de données de départ pour votre module de fusion.</span><span class="sxs-lookup"><span data-stu-id="291e7-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="291e7-108">Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="291e7-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="291e7-109">Les développeurs doivent créer des modules de fusion à l’aide du schéma de base de données le plus simple qui installe leurs composants.</span><span class="sxs-lookup"><span data-stu-id="291e7-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="291e7-110">L’utilisation d’un schéma simple garantit la plus grande compatibilité pour le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="291e7-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="291e7-111">La fusion d’un module de fusion dans un package d’installation avec un schéma de base de données différent entraîne généralement des conflits de fusion.</span><span class="sxs-lookup"><span data-stu-id="291e7-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="291e7-112">Pour obtenir la liste complète de toutes les tables obligatoires et facultatives dans les modules de fusion, consultez [tables de base de données de module de fusion](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="291e7-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



