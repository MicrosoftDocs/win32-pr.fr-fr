---
description: ICE55 valide que tous les objets LockPermission existent et ont des valeurs d’autorisation valides.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204190"
---
# <a name="ice55"></a><span data-ttu-id="36bee-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="36bee-103">ICE55</span></span>

<span data-ttu-id="36bee-104">ICE55 valide que tous les objets LockPermission existent et ont des valeurs d’autorisation valides.</span><span class="sxs-lookup"><span data-stu-id="36bee-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="36bee-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="36bee-105">Result</span></span>

<span data-ttu-id="36bee-106">ICE55 publie une erreur si un LockObject listé dans la [table LockPermissions](lockpermissions-table.md) n’existe pas ou si aucun niveau de privilège n’est spécifié dans la colonne autorisation.</span><span class="sxs-lookup"><span data-stu-id="36bee-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="36bee-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="36bee-107">Example</span></span>

<span data-ttu-id="36bee-108">ICE55 signale les erreurs suivantes pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="36bee-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="36bee-109">[Table LockPermissions](lockpermissions-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="36bee-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="36bee-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="36bee-110">LockObject</span></span> | <span data-ttu-id="36bee-111">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="36bee-111">Table</span></span> | <span data-ttu-id="36bee-112">Domain</span><span class="sxs-lookup"><span data-stu-id="36bee-112">Domain</span></span> | <span data-ttu-id="36bee-113">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="36bee-113">User</span></span>  | <span data-ttu-id="36bee-114">Autorisation</span><span class="sxs-lookup"><span data-stu-id="36bee-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="36bee-115">Fichier1</span><span class="sxs-lookup"><span data-stu-id="36bee-115">File1</span></span>      | <span data-ttu-id="36bee-116">Fichier</span><span class="sxs-lookup"><span data-stu-id="36bee-116">File</span></span>  |        | <span data-ttu-id="36bee-117">guest</span><span class="sxs-lookup"><span data-stu-id="36bee-117">guest</span></span> |            |
| <span data-ttu-id="36bee-118">Fichier3</span><span class="sxs-lookup"><span data-stu-id="36bee-118">File3</span></span>      | <span data-ttu-id="36bee-119">Fichier</span><span class="sxs-lookup"><span data-stu-id="36bee-119">File</span></span>  |        | <span data-ttu-id="36bee-120">guest</span><span class="sxs-lookup"><span data-stu-id="36bee-120">guest</span></span> | <span data-ttu-id="36bee-121">1</span><span class="sxs-lookup"><span data-stu-id="36bee-121">1</span></span>          |



 

<span data-ttu-id="36bee-122">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="36bee-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="36bee-123">Fichier</span><span class="sxs-lookup"><span data-stu-id="36bee-123">File</span></span>  | <span data-ttu-id="36bee-124">Version</span><span class="sxs-lookup"><span data-stu-id="36bee-124">Version</span></span> | <span data-ttu-id="36bee-125">Language</span><span class="sxs-lookup"><span data-stu-id="36bee-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="36bee-126">Fichier1</span><span class="sxs-lookup"><span data-stu-id="36bee-126">File1</span></span> | <span data-ttu-id="36bee-127">Fichier2</span><span class="sxs-lookup"><span data-stu-id="36bee-127">File2</span></span>   |          |
| <span data-ttu-id="36bee-128">Fichier2</span><span class="sxs-lookup"><span data-stu-id="36bee-128">File2</span></span> | <span data-ttu-id="36bee-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="36bee-129">1.0.0.0</span></span> | <span data-ttu-id="36bee-130">1033</span><span class="sxs-lookup"><span data-stu-id="36bee-130">1033</span></span>     |



 

<span data-ttu-id="36bee-131">L’objet fichier1 a une valeur null dans la colonne autorisation.</span><span class="sxs-lookup"><span data-stu-id="36bee-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="36bee-132">Chaque ligne doit avoir une valeur dans la colonne autorisations.</span><span class="sxs-lookup"><span data-stu-id="36bee-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="36bee-133">Pour corriger cette erreur, spécifiez une valeur numérique dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="36bee-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="36bee-134">Si aucun privilège n’est nécessaire pour cet objet, vous devez supprimer la ligne.</span><span class="sxs-lookup"><span data-stu-id="36bee-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="36bee-135">L’objet fichier3 décrit dans la table LockPermissions n’est pas répertorié dans la table file.</span><span class="sxs-lookup"><span data-stu-id="36bee-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="36bee-136">Pour corriger cette erreur, reportez-vous à un objet valide.</span><span class="sxs-lookup"><span data-stu-id="36bee-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36bee-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36bee-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bee-138">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="36bee-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



