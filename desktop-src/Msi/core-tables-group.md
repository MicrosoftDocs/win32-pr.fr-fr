---
description: Pour plus d’informations sur le diagramme suivant, consultez la légende diagramme de relation d’entité.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Groupe de tables principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952892"
---
# <a name="core-tables-group"></a><span data-ttu-id="7b5ae-103">Groupe de tables principales</span><span class="sxs-lookup"><span data-stu-id="7b5ae-103">Core Tables Group</span></span>

<span data-ttu-id="7b5ae-104">Pour plus d’informations sur le diagramme suivant, consultez la [légende diagramme de relation d’entité](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="7b5ae-104">For more information about the following diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

![Groupe de tables principales](images/core.png)

<span data-ttu-id="7b5ae-106">Le groupe principal se compose de tables décrivant les fonctionnalités et les composants fondamentaux de l’application et du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-106">The core group consists of tables describing the fundamental features and components of the application and the installer package.</span></span> <span data-ttu-id="7b5ae-107">Par conséquent, les développeurs de packages d’installation doivent réfléchir à la façon de remplir ces tables en premier, car l’organisation d’une grande partie de la base de données est visible à partir du contenu de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-107">Developers of install packages should therefore consider how to populate these tables first because the organization of much of the database will become apparent from the content of this group.</span></span>

-   <span data-ttu-id="7b5ae-108">Le [tableau de fonctionnalités](feature-table.md) répertorie toutes les fonctionnalités appartenant à l’application.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-108">The [Feature table](feature-table.md) lists all features belonging to the application.</span></span>
-   <span data-ttu-id="7b5ae-109">La [table de condition](condition-table.md) contient les expressions conditionnelles qui déterminent si une fonctionnalité particulière sera installée ou non.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-109">The [Condition table](condition-table.md) contains the conditional expressions that determine whether or not a particular feature will be installed.</span></span>
-   <span data-ttu-id="7b5ae-110">Le [tableau FeatureComponents](featurecomponents-table.md) décrit les composants qui appartiennent à chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-110">The [FeatureComponents table](featurecomponents-table.md) describes which components belong to each feature.</span></span>
-   <span data-ttu-id="7b5ae-111">La [table](component-table.md) des composants répertorie tous les composants appartenant à l’installation.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-111">The [Component table](component-table.md) lists all components belonging to the installation.</span></span>
-   <span data-ttu-id="7b5ae-112">Le [tableau répertoire](directory-table.md) répertorie les répertoires nécessaires au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-112">The [Directory table](directory-table.md) lists the directories that are needed during the installation.</span></span> <span data-ttu-id="7b5ae-113">Étant donné que chaque composant doit être associé à un et un seul annuaire, la table des composants est étroitement liée à cette table et possède une clé externe pour la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-113">Because each component must be associated with one and only one directory, the Component table is closely related to this table and has an external key to the Directory table.</span></span>
-   <span data-ttu-id="7b5ae-114">Le [tableau PublishComponent](publishcomponent-table.md) répertorie les fonctionnalités et les composants qui sont publiés pour une utilisation par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-114">The [PublishComponent table](publishcomponent-table.md) lists the features and components that are published for use by other applications.</span></span> <span data-ttu-id="7b5ae-115">Les [composants et les fonctionnalités](components-and-features.md) sont les deux types de publication de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-115">[Components and Features](components-and-features.md) are the two types of feature advertisement.</span></span>
-   <span data-ttu-id="7b5ae-116">La [table MsiAssembly](msiassembly-table.md) spécifie Windows Installer paramètres pour .NET Framework assemblys Common Language Runtime et les assemblys Win32.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-116">The [MsiAssembly table](msiassembly-table.md) specifies Windows Installer settings for .NET Framework common language runtime assemblies and Win32 assemblies.</span></span>
-   <span data-ttu-id="7b5ae-117">La [table MsiAssemblyName](msiassemblyname-table.md) spécifie le schéma pour les éléments d’un nom de cache d’assembly fort pour un assembly Common Language Runtime ou Win32.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-117">The [MsiAssemblyName table](msiassemblyname-table.md) specifies the schema for the elements of a strong assembly cache name for a common language runtime or Win32 assembly.</span></span>
-   <span data-ttu-id="7b5ae-118">La [table ComPlus](complus-table.md) contient les informations nécessaires pour installer les applications com+.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-118">The [Complus table](complus-table.md) contains information needed to install COM+ applications.</span></span>
-   <span data-ttu-id="7b5ae-119">La [table IsolatedComponent](isolatedcomponent-table.md) associe le composant spécifié dans la \_ colonne application du composant (généralement un fichier. exe) au composant spécifié dans la \_ colonne partagé du composant (généralement une DLL partagée).</span><span class="sxs-lookup"><span data-stu-id="7b5ae-119">The [IsolatedComponent table](isolatedcomponent-table.md) associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span>
-   <span data-ttu-id="7b5ae-120">La [table de mise à niveau](upgrade-table.md) contient les informations requises lors des [mises à niveau majeures](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="7b5ae-120">The [Upgrade table](upgrade-table.md) contains information required during [major upgrades](major-upgrades.md).</span></span>

 

 



