---
description: L’action ProcessComponents inscrit et désinscrit les composants, leurs chemins d’accès aux clés et les clients des composants.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Action ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530166"
---
# <a name="processcomponents-action"></a><span data-ttu-id="20e63-103">Action ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="20e63-103">ProcessComponents Action</span></span>

<span data-ttu-id="20e63-104">L’action ProcessComponents inscrit et désinscrit les composants, leurs chemins d’accès aux clés et les clients des composants.</span><span class="sxs-lookup"><span data-stu-id="20e63-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="20e63-105">L’action ProcessComponents interroge la colonne keyPath de la [table Component](component-table.md) pour déterminer les chemins d’accès de keyPath.</span><span class="sxs-lookup"><span data-stu-id="20e63-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="20e63-106">Cette inscription est utilisée par [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) pour retourner le chemin d’accès d’un composant pour un client produit.</span><span class="sxs-lookup"><span data-stu-id="20e63-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="20e63-107">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="20e63-107">Sequence Restrictions</span></span>

<span data-ttu-id="20e63-108">L’action ProcessComponents doit venir après l’action [InstallInitialize](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="20e63-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="20e63-109">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="20e63-109">ActionData Messages</span></span>

<span data-ttu-id="20e63-110">Pour chaque composant en cours d’inscription.</span><span class="sxs-lookup"><span data-stu-id="20e63-110">For each component being registered.</span></span>



| <span data-ttu-id="20e63-111">Champ</span><span class="sxs-lookup"><span data-stu-id="20e63-111">Field</span></span> | <span data-ttu-id="20e63-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="20e63-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="20e63-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="20e63-113">\[1\]</span></span> | <span data-ttu-id="20e63-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="20e63-114">ProductId</span></span>                       |
| <span data-ttu-id="20e63-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="20e63-115">\[2\]</span></span> | <span data-ttu-id="20e63-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="20e63-116">ComponentId</span></span>                     |
| <span data-ttu-id="20e63-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="20e63-117">\[3\]</span></span> | <span data-ttu-id="20e63-118">Chemin d’accès de la clé du composant.</span><span class="sxs-lookup"><span data-stu-id="20e63-118">The key path for the component.</span></span> |



 

<span data-ttu-id="20e63-119">Pour chaque composant en cours d’annulation d’inscription.</span><span class="sxs-lookup"><span data-stu-id="20e63-119">For each component being unregistered.</span></span>



| <span data-ttu-id="20e63-120">Champ</span><span class="sxs-lookup"><span data-stu-id="20e63-120">Field</span></span> | <span data-ttu-id="20e63-121">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="20e63-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="20e63-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="20e63-122">\[1\]</span></span> | <span data-ttu-id="20e63-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="20e63-123">ProductId</span></span>                  |
| <span data-ttu-id="20e63-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="20e63-124">\[2\]</span></span> | <span data-ttu-id="20e63-125">ComponentId</span><span class="sxs-lookup"><span data-stu-id="20e63-125">ComponentId</span></span>                |



 

 

 



