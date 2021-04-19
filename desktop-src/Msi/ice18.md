---
description: ICE18 valide que tous les répertoires vides utilisés comme chemin de clé pour un composant sont répertoriés dans la table CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524487"
---
# <a name="ice18"></a><span data-ttu-id="02928-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="02928-103">ICE18</span></span>

<span data-ttu-id="02928-104">ICE18 valide que tous les répertoires vides utilisés comme chemin de clé pour un composant sont répertoriés dans la [table CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="02928-105">Si la colonne keyPath de la [table Component](component-table.md) est null, cela signifie que le répertoire figurant dans la \_ colonne Directory est le chemin d’accès de clé de ce composant.</span><span class="sxs-lookup"><span data-stu-id="02928-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="02928-106">Étant donné que les dossiers créés par le programme d’installation sont supprimés lorsqu’ils sont vides, ce dossier doit être répertorié dans la [table CreateFolder](createfolder-table.md) pour empêcher le programme d’installation de tenter de s’installer à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="02928-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="02928-107">Ne faites pas du répertoire SystemFolder le chemin d’accès de clé d’un composant.</span><span class="sxs-lookup"><span data-stu-id="02928-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="02928-108">Étant donné que ce dossier est présent sur chaque système d’exploitation, le programme d’installation détecte toujours le chemin d’accès de la clé, que le composant soit présent ou non.</span><span class="sxs-lookup"><span data-stu-id="02928-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="02928-109">Dans ce cas, le chemin d’accès de la clé doit être un fichier, une entrée de registre ou une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="02928-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="02928-110">Lorsque vous effectuez une validation, ICE18 vérifie d’abord si les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="02928-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="02928-111">La colonne keyPath de la [table Component](component-table.md) contient une valeur null.</span><span class="sxs-lookup"><span data-stu-id="02928-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="02928-112">Aucun fichier n’est répertorié pour le composant dans la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="02928-113">Il n’existe aucun fichier pour le composant répertorié dans la [table RemoveFile](removefile-table.md) et que la valeur de DirProperty est identique à celle \_ de la colonne Directory de la [table Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="02928-114">Il n’existe aucun fichier pour le composant répertorié dans la [table DuplicateFile](duplicatefile-table.md) et que la valeur de DestFolder est identique à celle \_ de la colonne Directory de la [table Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="02928-115">Il n’y a pas de fichiers pour le composant répertorié dans la [table MoveFile](movefile-table.md) et que la valeur de DestFolder est identique à celle \_ de la colonne Directory de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="02928-116">Si la valeur est true, ICE18 valide les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="02928-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="02928-117">Que la \_ colonne Component de la [table CreateFolder](createfolder-table.md) a la même valeur que la colonne Component de la [table Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="02928-118">Que la \_ colonne Directory de la table CreateFolder a la même valeur que la \_ colonne Directory de la [table Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="02928-119">Résultats</span><span class="sxs-lookup"><span data-stu-id="02928-119">Result</span></span>

<span data-ttu-id="02928-120">ICE18 publie un message d’erreur si le package d’installation spécifie un répertoire comme chemin de clé pour le composant qui n’est pas listé dans la [table CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="02928-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02928-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02928-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02928-122">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="02928-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



