---
description: Représente une collection des fenêtres ouvertes qui appartiennent au shell. Les méthodes associées à ces objets peuvent contrôler et exécuter des commandes dans l’interpréteur de commandes, et obtenir d’autres objets liés à l’interpréteur de commandes.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Objet ShellWindows (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973278"
---
# <a name="shellwindows-object"></a><span data-ttu-id="e5023-104">Objet ShellWindows</span><span class="sxs-lookup"><span data-stu-id="e5023-104">ShellWindows object</span></span>

<span data-ttu-id="e5023-105">Représente une collection des fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="e5023-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="e5023-106">Les méthodes associées à ces objets peuvent contrôler et exécuter des commandes dans l’interpréteur de commandes, et obtenir d’autres objets liés à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e5023-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="e5023-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e5023-107">Members</span></span>

<span data-ttu-id="e5023-108">L’objet **ShellWindows** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e5023-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="e5023-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e5023-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5023-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e5023-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5023-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e5023-111">Methods</span></span>

<span data-ttu-id="e5023-112">L’objet **ShellWindows** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e5023-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="e5023-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="e5023-113">Method</span></span>                                                 | <span data-ttu-id="e5023-114">Description</span><span class="sxs-lookup"><span data-stu-id="e5023-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5023-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e5023-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="e5023-116">Crée et retourne un nouvel objet **ShellWindows** qui est une copie de cet objet **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="e5023-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="e5023-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e5023-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="e5023-118">Récupère un objet [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) qui représente la fenêtre de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e5023-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e5023-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e5023-119">Properties</span></span>

<span data-ttu-id="e5023-120">L’objet **ShellWindows** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e5023-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="e5023-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="e5023-121">Property</span></span>                                       | <span data-ttu-id="e5023-122">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="e5023-122">Access type</span></span>          | <span data-ttu-id="e5023-123">Description</span><span class="sxs-lookup"><span data-stu-id="e5023-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="e5023-124">**Count**</span><span class="sxs-lookup"><span data-stu-id="e5023-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="e5023-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e5023-125">Read-only</span></span><br/> | <span data-ttu-id="e5023-126">Contient le nombre d’éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="e5023-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5023-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e5023-127">Requirements</span></span>



| <span data-ttu-id="e5023-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5023-128">Requirement</span></span> | <span data-ttu-id="e5023-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5023-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5023-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5023-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5023-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5023-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e5023-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5023-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5023-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5023-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5023-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5023-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5023-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5023-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="e5023-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e5023-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5023-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e5023-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
