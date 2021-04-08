---
description: Une table de composants est requise dans chaque module de fusion.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Création de tables de composants de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034407"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="3f521-103">Création de tables de composants de module de fusion</span><span class="sxs-lookup"><span data-stu-id="3f521-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="3f521-104">Une [table de composants](component-table.md) est requise dans chaque module de fusion.</span><span class="sxs-lookup"><span data-stu-id="3f521-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="3f521-105">Cette table contient un enregistrement pour chaque composant remis par le module de fusion au fichier. msi cible.</span><span class="sxs-lookup"><span data-stu-id="3f521-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="3f521-106">Notez que chacun de ces composants doit également être spécifié dans la [table ModuleComponents](modulecomponents-table.md) décrite dans [création de tables ModuleComponents](authoring-modulecomponents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3f521-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="3f521-107">Utilisez la Convention d’affectation de noms standard lorsque vous entrez des noms dans la colonne composant pour vous assurer que l’identificateur de chaque composant est unique pour tous les modules de fusion et les bases de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="3f521-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="3f521-108">Pour plus d’informations, consultez [attribution de noms aux clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="3f521-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="3f521-109">Renseignez les champs restants dans chaque enregistrement comme décrit pour une base de données d’installation dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f521-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="3f521-110">Les composants ajoutés à un package par un module de fusion doivent respecter les instructions relatives aux composants Windows Installer valides décrits dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f521-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="3f521-111">Composants Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3f521-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="3f521-112">Organisation des applications en composants</span><span class="sxs-lookup"><span data-stu-id="3f521-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



