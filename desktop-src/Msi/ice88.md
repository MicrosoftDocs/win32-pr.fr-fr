---
description: ICE88 vérifie que le répertoire référencé dans la colonne DirProperty de la table IniFile existe dans le package Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867686"
---
# <a name="ice88"></a><span data-ttu-id="1a111-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="1a111-103">ICE88</span></span>

<span data-ttu-id="1a111-104">ICE88 vérifie que le répertoire référencé dans la colonne DirProperty de la [table inifile](inifile-table.md) existe dans le package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1a111-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="1a111-105">ICE88 émet un avertissement si la valeur DirProperty ne représente pas une propriété dans les tables Directory, AppSearch ou Property, certaines [Propriétés du dossier système](property-reference.md)ou une propriété définie par une action personnalisée de type 51.</span><span class="sxs-lookup"><span data-stu-id="1a111-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="1a111-106">ICE88 analyse les tables et les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a111-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="1a111-107">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="1a111-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="1a111-108">Table AppSearch</span><span class="sxs-lookup"><span data-stu-id="1a111-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="1a111-109">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="1a111-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="1a111-110">[Table CustomAction](customaction-table.md) , où l’action personnalisée est un [type d’action personnalisé 51](custom-action-type-51.md)</span><span class="sxs-lookup"><span data-stu-id="1a111-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="1a111-111">**Propriété ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="1a111-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="1a111-112">**Propriété CommonFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="1a111-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="1a111-113">**Propriété SystemFolder**</span><span class="sxs-lookup"><span data-stu-id="1a111-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="1a111-114">**Propriété ProgramFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="1a111-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="1a111-115">**Propriété CommonFiles64Folder**</span><span class="sxs-lookup"><span data-stu-id="1a111-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="1a111-116">**Propriété System64Folder**</span><span class="sxs-lookup"><span data-stu-id="1a111-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="1a111-117">Résultats</span><span class="sxs-lookup"><span data-stu-id="1a111-117">Result</span></span>

<span data-ttu-id="1a111-118">ICE88 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="1a111-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="1a111-119">AVERTISSEMENT ICE88</span><span class="sxs-lookup"><span data-stu-id="1a111-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="1a111-120">Description</span><span class="sxs-lookup"><span data-stu-id="1a111-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a111-121">Dans l’entrée de table IniFile (IniFile =) \[ 3, \] DirProperty = \[ 1 \] est introuvable dans les tables Directory/Property/AppSearch/ca-Type51 et il ne s’agit pas de l’une des propriétés du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1a111-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="1a111-122">Pour chaque enregistrement de la table IniFile, ICE88 lit la valeur dans la colonne DirProperty.</span><span class="sxs-lookup"><span data-stu-id="1a111-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="1a111-123">ICE88 recherche la valeur dans la table de [répertoire](directory-table.md), la [table AppSearch](appsearch-table.md)et la [table de propriétés](property-table.md) , et analyse également la liste des propriétés définies par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1a111-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="1a111-124">ICE88 publie cet avertissement si la valeur est introuvable dans l’analyse.</span><span class="sxs-lookup"><span data-stu-id="1a111-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1a111-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a111-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a111-126">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="1a111-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



