---
description: Chaque enregistrement de la table IsolatedComponent associe le composant spécifié dans la \_ colonne application du composant (généralement un fichier. exe) au composant spécifié dans la \_ colonne partagé du composant (généralement une DLL partagée).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Table IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515664"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="b8818-103">Table IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="b8818-103">IsolatedComponent Table</span></span>

<span data-ttu-id="b8818-104">Chaque enregistrement de la table IsolatedComponent associe le composant spécifié dans la \_ colonne application du composant (généralement un fichier. exe) au composant spécifié dans la \_ colonne partagé du composant (généralement une DLL partagée).</span><span class="sxs-lookup"><span data-stu-id="b8818-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="b8818-105">L' [action IsolateComponents](isolatecomponents-action.md) installe une copie du composant \_ partagé dans un emplacement privé pour une utilisation par l’application de composant \_ .</span><span class="sxs-lookup"><span data-stu-id="b8818-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="b8818-106">Cela isole l’application du composant des \_ autres copies du composant \_ partagé qui peuvent être installées dans un emplacement partagé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b8818-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="b8818-107">Consultez [composants isolés](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="b8818-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="b8818-108">Pour lier un composant \_ partagé à plusieurs applications de composant \_ , incluez un enregistrement distinct pour chaque paire dans la table IsolatedComponents.</span><span class="sxs-lookup"><span data-stu-id="b8818-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="b8818-109">Le programme d’installation copie les fichiers du composant \_ partagé dans le répertoire de chaque application de composant \_ installée.</span><span class="sxs-lookup"><span data-stu-id="b8818-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="b8818-110">La table IsolatedComponent contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8818-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="b8818-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="b8818-111">Column</span></span>                 | <span data-ttu-id="b8818-112">Type</span><span class="sxs-lookup"><span data-stu-id="b8818-112">Type</span></span>                         | <span data-ttu-id="b8818-113">Clé</span><span class="sxs-lookup"><span data-stu-id="b8818-113">Key</span></span> | <span data-ttu-id="b8818-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="b8818-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="b8818-115">Composant \_ partagé</span><span class="sxs-lookup"><span data-stu-id="b8818-115">Component\_Shared</span></span>      | [<span data-ttu-id="b8818-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b8818-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="b8818-117">O</span><span class="sxs-lookup"><span data-stu-id="b8818-117">Y</span></span>   | <span data-ttu-id="b8818-118">N</span><span class="sxs-lookup"><span data-stu-id="b8818-118">N</span></span>        |
| <span data-ttu-id="b8818-119">Application de composant \_</span><span class="sxs-lookup"><span data-stu-id="b8818-119">Component\_Application</span></span> | [<span data-ttu-id="b8818-120">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b8818-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="b8818-121">O</span><span class="sxs-lookup"><span data-stu-id="b8818-121">Y</span></span>   | <span data-ttu-id="b8818-122">N</span><span class="sxs-lookup"><span data-stu-id="b8818-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b8818-123">Colonnes</span><span class="sxs-lookup"><span data-stu-id="b8818-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b8818-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Composant \_ partagé</span><span class="sxs-lookup"><span data-stu-id="b8818-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="b8818-125">Clé étrangère dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b8818-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="b8818-126">Composant qui contient le fichier partagé, généralement une DLL.</span><span class="sxs-lookup"><span data-stu-id="b8818-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="b8818-127">La DLL doit être le fichier de clé pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="b8818-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="b8818-128">Il doit s’agir d’un composant différent de celui indiqué dans la \_ colonne application du composant.</span><span class="sxs-lookup"><span data-stu-id="b8818-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="b8818-129">Le composant partagé contrôle l’inscription de toutes les copies isolées du composant et doit avoir l’indicateur **msidbComponentAttributesSharedDllRefCount** défini dans la colonne attributs de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="b8818-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="b8818-130">Cela permet de s’assurer que le programme d’installation peut gérer la durée de vie du composant partagé.</span><span class="sxs-lookup"><span data-stu-id="b8818-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="b8818-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Application de composant \_</span><span class="sxs-lookup"><span data-stu-id="b8818-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="b8818-132">Clé étrangère dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b8818-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="b8818-133">Composant qui contient le fichier. exe qui charge le fichier partagé.</span><span class="sxs-lookup"><span data-stu-id="b8818-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="b8818-134">Le fichier. exe doit être le fichier de clé pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="b8818-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="b8818-135">Il doit s’agir d’un composant différent de celui indiqué dans la \_ colonne partagé du composant.</span><span class="sxs-lookup"><span data-stu-id="b8818-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="b8818-136">Validation</span><span class="sxs-lookup"><span data-stu-id="b8818-136">Validation</span></span>

<dl>

[<span data-ttu-id="b8818-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="b8818-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b8818-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="b8818-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b8818-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="b8818-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b8818-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="b8818-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="b8818-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="b8818-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="b8818-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="b8818-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



