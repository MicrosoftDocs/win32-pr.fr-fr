---
description: ICE45 valide que les colonnes de champ de bits dans la base de données ne définissent pas de bits réservés sur 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202541"
---
# <a name="ice45"></a><span data-ttu-id="c6e45-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="c6e45-103">ICE45</span></span>

<span data-ttu-id="c6e45-104">ICE45 valide que les colonnes de champ de bits dans la base de données ne définissent pas de bits réservés sur 1.</span><span class="sxs-lookup"><span data-stu-id="c6e45-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="c6e45-105">Les bits réservés ne fournissent aucune fonctionnalité dans les versions actuelles du programme d’installation, mais peuvent l’être dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c6e45-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="c6e45-106">Ils doivent avoir la valeur 0 pour être compatibles avec les futures versions de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c6e45-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="c6e45-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="c6e45-107">Result</span></span>

<span data-ttu-id="c6e45-108">ICE45 publie un message d’erreur si l’une des tables suivantes contient un champ de bits avec un bit réservé défini sur la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="c6e45-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="c6e45-109">Table BBControl</span><span class="sxs-lookup"><span data-stu-id="c6e45-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="c6e45-110">Table de boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="c6e45-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="c6e45-111">Tableau des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c6e45-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="c6e45-112">Table de fichiers</span><span class="sxs-lookup"><span data-stu-id="c6e45-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="c6e45-113">Table MoveFile</span><span class="sxs-lookup"><span data-stu-id="c6e45-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="c6e45-114">Table ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6e45-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="c6e45-115">Table ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="c6e45-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="c6e45-116">Table des correctifs</span><span class="sxs-lookup"><span data-stu-id="c6e45-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="c6e45-117">Table RemoveFile</span><span class="sxs-lookup"><span data-stu-id="c6e45-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="c6e45-118">Table ServiceControl</span><span class="sxs-lookup"><span data-stu-id="c6e45-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="c6e45-119">Table ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="c6e45-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="c6e45-120">Table TextStyle</span><span class="sxs-lookup"><span data-stu-id="c6e45-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="c6e45-121">ICE45 publie l’un des deux messages d’avertissement si la [table de contrôle](control-table.md) contient un champ de bits avec un bit réservé défini sur la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="c6e45-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="c6e45-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="c6e45-122">Example</span></span>

<span data-ttu-id="c6e45-123">ICE45 signale l’erreur suivante pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="c6e45-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="c6e45-124">ICE45 signale l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="c6e45-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="c6e45-125">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="c6e45-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="c6e45-126">Fichier</span><span class="sxs-lookup"><span data-stu-id="c6e45-126">File</span></span>  | <span data-ttu-id="c6e45-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6e45-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="c6e45-128">Fichier1</span><span class="sxs-lookup"><span data-stu-id="c6e45-128">File1</span></span> | <span data-ttu-id="c6e45-129">128</span><span class="sxs-lookup"><span data-stu-id="c6e45-129">128</span></span>        |



 

<span data-ttu-id="c6e45-130">[Table de contrôle](control-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="c6e45-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="c6e45-131">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="c6e45-131">Dialog</span></span>  | <span data-ttu-id="c6e45-132">Contrôler</span><span class="sxs-lookup"><span data-stu-id="c6e45-132">Control</span></span> | <span data-ttu-id="c6e45-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6e45-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="c6e45-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="c6e45-134">Dialog1</span></span> | <span data-ttu-id="c6e45-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="c6e45-135">Edit1</span></span>   | <span data-ttu-id="c6e45-136">2 097 152</span><span class="sxs-lookup"><span data-stu-id="c6e45-136">2097152</span></span>    |
| <span data-ttu-id="c6e45-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="c6e45-137">Dialog1</span></span> | <span data-ttu-id="c6e45-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="c6e45-138">Edit2</span></span>   | <span data-ttu-id="c6e45-139">1 048 576</span><span class="sxs-lookup"><span data-stu-id="c6e45-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="c6e45-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6e45-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6e45-141">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="c6e45-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



