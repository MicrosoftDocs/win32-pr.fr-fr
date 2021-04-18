---
description: ICE53 recherche des entrées dans la table de Registre qui écrivent des informations de stratégie d’installation privées ou des valeurs de stratégie dans le registre système.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526192"
---
# <a name="ice53"></a><span data-ttu-id="7c850-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="7c850-103">ICE53</span></span>

<span data-ttu-id="7c850-104">ICE53 recherche des entrées dans la table de Registre qui écrivent des informations de stratégie d’installation privées ou des valeurs de stratégie dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="7c850-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="7c850-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="7c850-105">Result</span></span>

<span data-ttu-id="7c850-106">ICE53 publie un avertissement si la table du Registre spécifie l’écriture des informations internes ou de stratégie dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7c850-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="7c850-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c850-107">Example</span></span>

<span data-ttu-id="7c850-108">ICE53 publie l’avertissement suivant pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="7c850-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="7c850-109">[Table du Registre](registry-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7c850-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="7c850-110">Registre</span><span class="sxs-lookup"><span data-stu-id="7c850-110">Registry</span></span>             | <span data-ttu-id="7c850-111">Root</span><span class="sxs-lookup"><span data-stu-id="7c850-111">Root</span></span>         | <span data-ttu-id="7c850-112">Clé</span><span class="sxs-lookup"><span data-stu-id="7c850-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c850-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="7c850-113">Registry1</span></span><br/> | <span data-ttu-id="7c850-114">1</span><span class="sxs-lookup"><span data-stu-id="7c850-114">1</span></span><br/> | <span data-ttu-id="7c850-115">**Logiciel** \\ **Stratégies** \\ **Microsoft** \\ **Windows** \\ **Programme d’installation** \\ **DisableRollback**</span><span class="sxs-lookup"><span data-stu-id="7c850-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="7c850-116">La ligne de la table de Registre « Registry1 » écrit une valeur de stratégie système dans le Registre qui affecte l’installation de tous les packages.</span><span class="sxs-lookup"><span data-stu-id="7c850-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="7c850-117">Selon le package, il peut être possible de désactiver la restauration pour ce package seul en définissant la propriété [**disablerollback**](-disablerollback.md) dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="7c850-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="7c850-118">Consultez [restauration de l’installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="7c850-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c850-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c850-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c850-120">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="7c850-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




