---
description: Créez des liens symboliques qui utilisent un chemin d’accès absolu ou relatif à l’aide de la fonction CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Création de liens symboliques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252b999b05004fd7735b16582783ef0c3afb0013
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387705"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="dbd64-103">Création de liens symboliques</span><span class="sxs-lookup"><span data-stu-id="dbd64-103">Creating Symbolic Links</span></span>

<span data-ttu-id="dbd64-104">La fonction [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) vous permet de créer des liens symboliques à l’aide d’un chemin d’accès absolu ou relatif.</span><span class="sxs-lookup"><span data-stu-id="dbd64-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="dbd64-105">Les liens symboliques peuvent être des liens absolus ou relatifs.</span><span class="sxs-lookup"><span data-stu-id="dbd64-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="dbd64-106">Les liens absolus sont des liens qui spécifient chaque partie du nom de chemin d’accès ; les liens relatifs sont déterminés par rapport à l’emplacement relatif : les spécificateurs de lien se trouvent dans un chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="dbd64-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="dbd64-107">Les liens relatifs sont spécifiés à l’aide des conventions suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbd64-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="dbd64-108">Point (.</span><span class="sxs-lookup"><span data-stu-id="dbd64-108">Dot (.</span></span> <span data-ttu-id="dbd64-109">et..) les conventions, par exemple, « .. \\ » résout le chemin d’accès relatif au répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="dbd64-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="dbd64-110">Les noms sans barres obliques ( \\ ), par exemple, « tmp » résout le chemin d’accès relatif au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="dbd64-110">Names with no slashes (\\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="dbd64-111">La racine relative, par exemple « \\ Windows \\ system32 », est résolue en «*lecteur actuel*: \\ Windows \\ system32 ».</span><span class="sxs-lookup"><span data-stu-id="dbd64-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="dbd64-112">Répertoire</span><span class="sxs-lookup"><span data-stu-id="dbd64-112">directory</span></span>
-   <span data-ttu-id="dbd64-113">Répertoire de travail actuel-relatif : par exemple, si le répertoire de travail actuel est « C : \\ Windows \\ system32 », « C:File.txt » est résolu en « c : \\ Windows \\ system32 \\File.txt ».</span><span class="sxs-lookup"><span data-stu-id="dbd64-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="dbd64-114">**Remarque**  Si vous spécifiez un lien relatif au répertoire de travail actif, il est créé en tant que lien absolu, en raison de la façon dont le répertoire de travail actuel est traité en fonction de l’utilisateur et du thread.</span><span class="sxs-lookup"><span data-stu-id="dbd64-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="dbd64-115">Un lien symbolique peut également contenir des points de jonction et des dossiers montés dans le cadre du nom du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="dbd64-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="dbd64-116">Les liens symboliques peuvent pointer directement vers un fichier ou un répertoire distant à l’aide du chemin d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="dbd64-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="dbd64-117">Les liens symboliques relatifs sont limités à un seul volume.</span><span class="sxs-lookup"><span data-stu-id="dbd64-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="dbd64-118">Exemple de lien symbolique absolu</span><span class="sxs-lookup"><span data-stu-id="dbd64-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="dbd64-119">Dans cet exemple, le chemin d’accès d’origine contient un composant, '*x*', qui est un lien symbolique absolu.</span><span class="sxs-lookup"><span data-stu-id="dbd64-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="dbd64-120">Lorsque'*x*'est rencontré, le fragment du chemin d’accès d’origine jusqu’à'*x*', y compris, est complètement remplacé par le chemin d’accès désigné par'*x*'.</span><span class="sxs-lookup"><span data-stu-id="dbd64-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="dbd64-121">Le reste du chemin d’accès après «*x*» est ajouté à ce nouveau chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="dbd64-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="dbd64-122">Cela devient alors le chemin d’accès modifié.</span><span class="sxs-lookup"><span data-stu-id="dbd64-122">This now becomes the modified path.</span></span>

<span data-ttu-id="dbd64-123">X : « C : \\ alpha \\ beta \\ absLink \\ gamma \\ file »</span><span class="sxs-lookup"><span data-stu-id="dbd64-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="dbd64-124">Lien : « absLink » est mappé à « \\ \\ machineB \\ share »</span><span class="sxs-lookup"><span data-stu-id="dbd64-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="dbd64-125">Chemin modifié : « \\ \\ machineB \\ share \\ gamma \\ file »</span><span class="sxs-lookup"><span data-stu-id="dbd64-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="dbd64-126">Exemple de liens symboliques relatifs</span><span class="sxs-lookup"><span data-stu-id="dbd64-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="dbd64-127">Dans cet exemple, le chemin d’accès d’origine contient un composant «*x*», qui est un lien symbolique relatif.</span><span class="sxs-lookup"><span data-stu-id="dbd64-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="dbd64-128">Lorsque'*x*'est rencontré, '*x*'est complètement remplacé par le nouveau fragment pointé par'*x*'.</span><span class="sxs-lookup"><span data-stu-id="dbd64-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="dbd64-129">Le reste du chemin d’accès après «*x*» est ajouté au nouveau chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="dbd64-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="dbd64-130">Tous les points (..) de ce nouveau chemin remplacent les composants qui apparaissent avant les points (..).</span><span class="sxs-lookup"><span data-stu-id="dbd64-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="dbd64-131">Chaque ensemble de points remplace le composant précédent.</span><span class="sxs-lookup"><span data-stu-id="dbd64-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="dbd64-132">Si le nombre de points (..) dépasse le nombre de composants, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="dbd64-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="dbd64-133">Dans le cas contraire, lorsque tous les composants de remplacement sont terminés, le chemin d’accès final modifié est conservé.</span><span class="sxs-lookup"><span data-stu-id="dbd64-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="dbd64-134">X : C : \\ \\ \\ fichier gamma de liaison bêta \\ alpha \\</span><span class="sxs-lookup"><span data-stu-id="dbd64-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="dbd64-135">Lien : « Link » est mappé à «.. \\ .. \\ thêta</span><span class="sxs-lookup"><span data-stu-id="dbd64-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="dbd64-136">Chemin modifié : «C : \\ alpha \\ beta \\ ... \\ . \\ \\fichier gamma thêta \\ "</span><span class="sxs-lookup"><span data-stu-id="dbd64-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="dbd64-137">Chemin final : « C : \\ Theta \\ gamma \\ file »</span><span class="sxs-lookup"><span data-stu-id="dbd64-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbd64-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbd64-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbd64-139">Liens symboliques</span><span class="sxs-lookup"><span data-stu-id="dbd64-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="dbd64-140">Liens physiques et jonctions</span><span class="sxs-lookup"><span data-stu-id="dbd64-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="dbd64-141">Nommage des fichiers, chemins d’accès et espaces de noms</span><span class="sxs-lookup"><span data-stu-id="dbd64-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



