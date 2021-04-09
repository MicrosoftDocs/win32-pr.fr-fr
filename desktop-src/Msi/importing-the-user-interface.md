---
description: Outre les informations abordées dans les sections précédentes, uisample.msi contient également des données pour un exemple d’interface utilisateur.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importation de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863038"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="8e98b-103">Importation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="8e98b-103">Importing the User Interface</span></span>

<span data-ttu-id="8e98b-104">Outre les informations abordées dans les sections précédentes, uisample.msi contient également des données pour un exemple d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8e98b-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="8e98b-105">Si vous avez fusionné uisample.msi dans MNP2000.msi dans la section [importation d’une base de données vide](importing-a-blank-database.md), ces informations sont également présentes dans MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="8e98b-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="8e98b-106">Les informations de l’exemple d’interface utilisateur se trouvent dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="8e98b-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="8e98b-107">Table ActionText</span><span class="sxs-lookup"><span data-stu-id="8e98b-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="8e98b-108">Table binaire</span><span class="sxs-lookup"><span data-stu-id="8e98b-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="8e98b-109">Table de contrôle</span><span class="sxs-lookup"><span data-stu-id="8e98b-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="8e98b-110">Table ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8e98b-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="8e98b-111">Table de boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="8e98b-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="8e98b-112">Table des erreurs</span><span class="sxs-lookup"><span data-stu-id="8e98b-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="8e98b-113">Table EventMapping</span><span class="sxs-lookup"><span data-stu-id="8e98b-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="8e98b-114">Table RadioButton</span><span class="sxs-lookup"><span data-stu-id="8e98b-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="8e98b-115">Table TextStyle</span><span class="sxs-lookup"><span data-stu-id="8e98b-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="8e98b-116">Table UIText</span><span class="sxs-lookup"><span data-stu-id="8e98b-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="8e98b-117">L’éditeur de base de données Orca fourni avec le programme d’installation comprend une option d’aperçu de boîte de dialogue que vous pouvez utiliser pour afficher un aperçu des dialogues de l’interface utilisateur spécifiés par les données dans les tables ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="8e98b-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="8e98b-118">L’exemple de package d’installation MNP2000.msi est maintenant prêt pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="8e98b-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="8e98b-119">Exécutez toujours la validation sur un nouveau package avant d’essayer d’installer le package pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="8e98b-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="8e98b-120">Cela est décrit dans validation de l’exemple d’installation.</span><span class="sxs-lookup"><span data-stu-id="8e98b-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="8e98b-121">Si vous ne souhaitez pas inclure l’interface utilisateur dans l’exemple de package, omettez ou supprimez toutes les informations figurant dans les tableaux ci-dessus, à l’exception de la [table TextStyle](textstyle-table.md) (qui est nécessaire pour définir la propriété [**DefaultUIFont**](defaultuifont.md) ).</span><span class="sxs-lookup"><span data-stu-id="8e98b-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="8e98b-122">Vous devez également supprimer les propriétés de l’interface utilisateur de la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e98b-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="8e98b-123">Un exemple de table de propriétés pour l’exemple Notepad, sans interface utilisateur, est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8e98b-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="8e98b-124">Ne réutilisez pas les GUID indiqués dans le tableau si vous copiez cet exemple.</span><span class="sxs-lookup"><span data-stu-id="8e98b-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="8e98b-125">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="8e98b-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="8e98b-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="8e98b-126">Property</span></span>                                   | <span data-ttu-id="8e98b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e98b-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="8e98b-128">**DefaultUIFont**</span><span class="sxs-lookup"><span data-stu-id="8e98b-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="8e98b-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="8e98b-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="8e98b-130">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="8e98b-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="8e98b-131">3</span><span class="sxs-lookup"><span data-stu-id="8e98b-131">3</span></span>                                      |
| [<span data-ttu-id="8e98b-132">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="8e98b-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="8e98b-133">1</span><span class="sxs-lookup"><span data-stu-id="8e98b-133">1</span></span>                                      |
| [<span data-ttu-id="8e98b-134">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="8e98b-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="8e98b-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="8e98b-135">Microsoft</span></span>                              |
| [<span data-ttu-id="8e98b-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="8e98b-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="8e98b-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="8e98b-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="8e98b-138">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="8e98b-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="8e98b-139">1033</span><span class="sxs-lookup"><span data-stu-id="8e98b-139">1033</span></span>                                   |
| [<span data-ttu-id="8e98b-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="8e98b-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="8e98b-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="8e98b-141">MNP2000</span></span>                                |
| [<span data-ttu-id="8e98b-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="8e98b-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="8e98b-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="8e98b-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="8e98b-144">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="8e98b-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="8e98b-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="8e98b-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="8e98b-146">Un package sans interface utilisateur peut être installé à partir de la ligne de commande ou d’un programme.</span><span class="sxs-lookup"><span data-stu-id="8e98b-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="8e98b-147">Pour installer un package à partir de la ligne de commande, utilisez les méthodes décrites dans [options de ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="8e98b-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="8e98b-148">Pour installer un package à partir d’un programme, utilisez les méthodes décrites dans [utilisation des fonctions de programme d’installation](using-installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8e98b-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="8e98b-149">Exécutez toujours la validation sur un nouveau package avant de tenter d’installer un nouveau package pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="8e98b-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="8e98b-150">Continuer</span><span class="sxs-lookup"><span data-stu-id="8e98b-150">Continue</span></span>](validating-an-installation-database.md)

 

 



