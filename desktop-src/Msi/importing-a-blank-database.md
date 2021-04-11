---
description: Pour reproduire l’exemple que vous devez copier ou créer à l’aide d’un outil logiciel, Windows Installer fichier de base de données.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importation d’une base de données vide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203776"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="934f7-103">Importation d’une base de données vide</span><span class="sxs-lookup"><span data-stu-id="934f7-103">Importing a Blank Database</span></span>

<span data-ttu-id="934f7-104">Pour reproduire l’exemple que vous devez copier ou créer à l’aide d’un outil logiciel, Windows Installer fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="934f7-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="934f7-105">Une base de données d’installation entièrement vierge, Schema.msi, est fournie avec les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="934f7-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="934f7-106">Le kit de développement logiciel (SDK) fournit également une base de données partiellement vide, uisample.msi, qui contient les tables et les données de séquence suggérées requises pour une interface utilisateur simple.</span><span class="sxs-lookup"><span data-stu-id="934f7-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="934f7-107">Effectuez une copie de uisample.msi et déplacez-le vers le même répertoire contenant le dossier du bloc-notes que vous avez créé lors de [la planification de l’installation](planning-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="934f7-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="934f7-108">Renommez le fichier MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="934f7-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="934f7-109">Le fichier de base de données d’installation et les fichiers sources doivent être situés à la racine du même répertoire.</span><span class="sxs-lookup"><span data-stu-id="934f7-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="934f7-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="934f7-110">For example:</span></span>

<span data-ttu-id="934f7-111">C : \\ exemple de \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="934f7-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="934f7-112">C : \\ exemple de \\ bloc-notes</span><span class="sxs-lookup"><span data-stu-id="934f7-112">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="934f7-113">Si vous n’utilisez pas Uisample.msi, vous devez obtenir une base de données vide, telle que Schema.msi, et entrer des informations pour l’installation à l’aide d’un outil d’édition de base de données tel que Orca, qui est fourni avec le kit de développement logiciel (SDK) ou un autre éditeur de base de données.</span><span class="sxs-lookup"><span data-stu-id="934f7-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="934f7-114">Continuer</span><span class="sxs-lookup"><span data-stu-id="934f7-114">Continue</span></span>](specifying-directory-structure.md)

 

 



