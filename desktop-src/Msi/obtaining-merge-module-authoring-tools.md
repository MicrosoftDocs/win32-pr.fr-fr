---
description: Pour générer un module de fusion, vous devez obtenir un outil logiciel permettant de modifier un fichier. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtention d’outils de création de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516948"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="f500d-103">Obtention d’outils de création de module de fusion</span><span class="sxs-lookup"><span data-stu-id="f500d-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="f500d-104">Pour générer un module de fusion, vous devez obtenir un outil logiciel permettant de modifier un fichier. msm.</span><span class="sxs-lookup"><span data-stu-id="f500d-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="f500d-105">Étant donné qu’un fichier. msm est fondamentalement un fichier. msi simplifié, vous pourrez peut-être utiliser les mêmes outils que ceux utilisés pour créer une base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="f500d-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="f500d-106">Par exemple, l’application Orca.exe fournie avec le kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f500d-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="f500d-107">Une alternative consiste à acheter l’un des outils d’empaquetage du programme d’installation à la disposition des éditeurs de logiciels indépendants.</span><span class="sxs-lookup"><span data-stu-id="f500d-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="f500d-108">Plusieurs outils tiers en cours de développement peuvent être utilisés pour produire des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="f500d-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="f500d-109">Si vous choisissez d’utiliser un outil tiers, vous devez vérifier qu’il génère des modules de fusion qui sont cohérents avec la norme décrite dans ce document.</span><span class="sxs-lookup"><span data-stu-id="f500d-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="f500d-110">En particulier, vous devez déterminer que les outils d’édition n’ont pas effectué les opérations suivantes dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="f500d-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="f500d-111">Ajout de tables superflues au module de fusion qui ne sont pas référencées dans la [table ModuleIgnoreTable](moduleignoretable-table.md).</span><span class="sxs-lookup"><span data-stu-id="f500d-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="f500d-112">Supprimez ces tables ou ajoutez-les à la table ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="f500d-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="f500d-113">Ajout d’une [table](textstyle-table.md) de style TextStyle inutile au module de fusion.</span><span class="sxs-lookup"><span data-stu-id="f500d-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="f500d-114">Si votre module de fusion n’a pas d’interface utilisateur (et cela ne doit généralement pas), vous pouvez supprimer cette table en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="f500d-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="f500d-115">Ajout d’entrées inutiles à la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f500d-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="f500d-116">Supprimez les entrées inutiles de la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="f500d-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="f500d-117">Informations de gauche dans le tableau de validation du module de fusion \_ .</span><span class="sxs-lookup"><span data-stu-id="f500d-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="f500d-118">Cela empêche la validation du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="f500d-118">This prevents merge module validation.</span></span> <span data-ttu-id="f500d-119">Ajoutez une \_ table de validation complète.</span><span class="sxs-lookup"><span data-stu-id="f500d-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f500d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f500d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f500d-121">Création d’interfaces utilisateur dans les modules de fusion</span><span class="sxs-lookup"><span data-stu-id="f500d-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="f500d-122">Création de tables de répertoires de module de fusion</span><span class="sxs-lookup"><span data-stu-id="f500d-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="f500d-123">Validation des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="f500d-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



