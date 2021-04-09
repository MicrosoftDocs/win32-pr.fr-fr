---
description: La table ReserveCost est une table facultative qui permet à l’auteur de réserver une quantité d’espace disque dans un répertoire qui dépend de l’état d’installation d’un composant.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Table ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952230"
---
# <a name="reservecost-table"></a><span data-ttu-id="cb52a-103">Table ReserveCost</span><span class="sxs-lookup"><span data-stu-id="cb52a-103">ReserveCost Table</span></span>

<span data-ttu-id="cb52a-104">La table ReserveCost est une table facultative qui permet à l’auteur de réserver une quantité d’espace disque dans un répertoire qui dépend de l’état d’installation d’un composant.</span><span class="sxs-lookup"><span data-stu-id="cb52a-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="cb52a-105">La table ReserveCost contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb52a-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="cb52a-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="cb52a-106">Column</span></span>        | <span data-ttu-id="cb52a-107">Type</span><span class="sxs-lookup"><span data-stu-id="cb52a-107">Type</span></span>                               | <span data-ttu-id="cb52a-108">Clé</span><span class="sxs-lookup"><span data-stu-id="cb52a-108">Key</span></span> | <span data-ttu-id="cb52a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="cb52a-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="cb52a-110">ReserveKey</span><span class="sxs-lookup"><span data-stu-id="cb52a-110">ReserveKey</span></span>    | [<span data-ttu-id="cb52a-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="cb52a-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cb52a-112">O</span><span class="sxs-lookup"><span data-stu-id="cb52a-112">Y</span></span>   | <span data-ttu-id="cb52a-113">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-113">N</span></span>        |
| <span data-ttu-id="cb52a-114">-\_</span><span class="sxs-lookup"><span data-stu-id="cb52a-114">Component\_</span></span>   | [<span data-ttu-id="cb52a-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="cb52a-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cb52a-116">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-116">N</span></span>   | <span data-ttu-id="cb52a-117">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-117">N</span></span>        |
| <span data-ttu-id="cb52a-118">ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="cb52a-118">ReserveFolder</span></span> | [<span data-ttu-id="cb52a-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="cb52a-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="cb52a-120">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-120">N</span></span>   | <span data-ttu-id="cb52a-121">O</span><span class="sxs-lookup"><span data-stu-id="cb52a-121">Y</span></span>        |
| <span data-ttu-id="cb52a-122">ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="cb52a-122">ReserveLocal</span></span>  | [<span data-ttu-id="cb52a-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="cb52a-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="cb52a-124">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-124">N</span></span>   | <span data-ttu-id="cb52a-125">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-125">N</span></span>        |
| <span data-ttu-id="cb52a-126">ReserveSource</span><span class="sxs-lookup"><span data-stu-id="cb52a-126">ReserveSource</span></span> | [<span data-ttu-id="cb52a-127">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="cb52a-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="cb52a-128">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-128">N</span></span>   | <span data-ttu-id="cb52a-129">N</span><span class="sxs-lookup"><span data-stu-id="cb52a-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cb52a-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="cb52a-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cb52a-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span><span class="sxs-lookup"><span data-stu-id="cb52a-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="cb52a-132">Clé primaire qui identifie de façon unique une entrée de table ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="cb52a-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="cb52a-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="cb52a-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="cb52a-134">Clé externe vers la colonne de l’une des tables de [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cb52a-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="cb52a-135">Réserve une quantité d’espace spécifiée si ce composant doit être installé.</span><span class="sxs-lookup"><span data-stu-id="cb52a-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="cb52a-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="cb52a-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="cb52a-137">Cette colonne contient le nom d’une propriété qui est le chemin d’accès complet au répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="cb52a-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="cb52a-138">Ce nom de propriété est généralement le nom d’un répertoire dans la table de [répertoire](directory-table.md) ou le nom d’un jeu de propriétés obtenu à l’aide de l’action [AppSearch](appsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cb52a-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="cb52a-139">Cela ajoute la quantité d’espace disque spécifiée dans ReserveLocal ou ReserveSource au coût du volume de l’appareil contenant le répertoire.</span><span class="sxs-lookup"><span data-stu-id="cb52a-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="cb52a-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="cb52a-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="cb52a-141">Nombre d’octets d’espace disque à réserver si le composant lié est installé pour s’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="cb52a-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="cb52a-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span><span class="sxs-lookup"><span data-stu-id="cb52a-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="cb52a-143">Nombre d’octets d’espace disque à réserver si le composant lié est installé pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="cb52a-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb52a-144">Notes</span><span class="sxs-lookup"><span data-stu-id="cb52a-144">Remarks</span></span>

<span data-ttu-id="cb52a-145">La réservation de coûts de cette façon peut être utile pour les auteurs qui souhaitent s’assurer qu’une quantité minimale d’espace disque sera disponible une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="cb52a-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="cb52a-146">Par exemple, cet espace disque peut être réservé pour les documents utilisateur ou pour les fichiers d’application (tels que les fichiers d’index) qui sont créés uniquement après le démarrage de l’application après l’installation.</span><span class="sxs-lookup"><span data-stu-id="cb52a-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="cb52a-147">Vous pouvez utiliser la table ReserveCost pour permettre aux actions personnalisées de spécifier un coût approximatif pour tous les fichiers, entrées de registre ou autres éléments que l’action personnalisée peut installer.</span><span class="sxs-lookup"><span data-stu-id="cb52a-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="cb52a-148">Les actions personnalisées qui ajoutent des entrées à la table ReserveCost doivent être séquencées entre les actions [CostInitialize](costinitialize-action.md) et [FileCost](filecost-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cb52a-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="cb52a-149">Cela est nécessaire pour que l’action FileCost Initialise correctement les coûts de tous les composants affectés par les entrées de la table ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="cb52a-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="cb52a-150">Validation</span><span class="sxs-lookup"><span data-stu-id="cb52a-150">Validation</span></span>

<dl>

[<span data-ttu-id="cb52a-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="cb52a-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cb52a-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="cb52a-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cb52a-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="cb52a-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



