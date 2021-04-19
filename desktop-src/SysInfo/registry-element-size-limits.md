---
description: Le tableau suivant identifie les limites de taille pour les différents éléments du Registre.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limites de taille des éléments du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534551"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="7eca4-103">Limites de taille des éléments du Registre</span><span class="sxs-lookup"><span data-stu-id="7eca4-103">Registry Element Size Limits</span></span>

<span data-ttu-id="7eca4-104">Le tableau suivant identifie les limites de taille pour les différents éléments du Registre.</span><span class="sxs-lookup"><span data-stu-id="7eca4-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="7eca4-105">Élément Registry</span><span class="sxs-lookup"><span data-stu-id="7eca4-105">Registry Element</span></span> | <span data-ttu-id="7eca4-106">Taille maximale</span><span class="sxs-lookup"><span data-stu-id="7eca4-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eca4-107">Nom de clé</span><span class="sxs-lookup"><span data-stu-id="7eca4-107">Key name</span></span>         | <span data-ttu-id="7eca4-108">255 caractères.</span><span class="sxs-lookup"><span data-stu-id="7eca4-108">255 characters.</span></span> <span data-ttu-id="7eca4-109">Le nom de clé comprend le chemin d’accès absolu de la clé dans le registre, en commençant toujours à une clé de base, par exemple, HKEY \_ local \_ machine.</span><span class="sxs-lookup"><span data-stu-id="7eca4-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="7eca4-110">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="7eca4-110">Value name</span></span>       | <span data-ttu-id="7eca4-111">16 383 caractères **Windows 2000 :** 260 caractères ANSI ou 16 383 caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="7eca4-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="7eca4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7eca4-112">Value</span></span>            | <span data-ttu-id="7eca4-113">Mémoire disponible (format le plus récent) 1 Mo (format standard)</span><span class="sxs-lookup"><span data-stu-id="7eca4-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="7eca4-114">Arborescence</span><span class="sxs-lookup"><span data-stu-id="7eca4-114">Tree</span></span>             | <span data-ttu-id="7eca4-115">Une arborescence du Registre peut avoir 512 niveaux de profondeur.</span><span class="sxs-lookup"><span data-stu-id="7eca4-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="7eca4-116">Vous pouvez créer jusqu’à 32 niveaux à la fois à l’aide d’un appel d’API de Registre unique.</span><span class="sxs-lookup"><span data-stu-id="7eca4-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="7eca4-117">Les valeurs longues (plus de 2 048 octets) doivent être stockées dans un fichier et l’emplacement du fichier doit être stocké dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7eca4-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="7eca4-118">Cela permet au registre de fonctionner efficacement.</span><span class="sxs-lookup"><span data-stu-id="7eca4-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="7eca4-119">L’emplacement du fichier peut être le nom d’une valeur ou les données d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="7eca4-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="7eca4-120">Chaque barre oblique inverse dans la chaîne d’emplacement doit être précédée d’une autre barre oblique inverse comme caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="7eca4-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="7eca4-121">Par exemple, spécifiez « C : \\ \\ mydir \\ \\ MyFile » pour stocker la chaîne « c : \\ mydir \\ MyFile ».</span><span class="sxs-lookup"><span data-stu-id="7eca4-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="7eca4-122">Un emplacement de fichier peut également être le nom d’une clé s’il se trouve dans la limite de 255 caractères pour les noms de clé et ne contient pas de barres obliques inverses, qui ne sont pas autorisées dans les noms de clés.</span><span class="sxs-lookup"><span data-stu-id="7eca4-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




