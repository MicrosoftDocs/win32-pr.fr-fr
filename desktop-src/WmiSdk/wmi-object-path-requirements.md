---
description: WMI utilise les chemins d’accès des objets dans les propriétés de référence des classes d’association pour identifier les objets connexes, ainsi que l’utilisation de chemins d’accès aux objets dans les paramètres d’entrée ou de sortie pour plusieurs méthodes.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Exigences relatives au chemin d’accès de l’objet WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393568"
---
# <a name="wmi-object-path-requirements"></a><span data-ttu-id="e681f-103">Exigences relatives au chemin d’accès de l’objet WMI</span><span class="sxs-lookup"><span data-stu-id="e681f-103">WMI Object Path Requirements</span></span>

<span data-ttu-id="e681f-104">WMI utilise les chemins d’accès des objets dans les propriétés de référence des classes d’association pour identifier les objets connexes, ainsi que l’utilisation de chemins d’accès aux objets dans les paramètres d’entrée ou de sortie pour plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="e681f-104">WMI uses object paths in the reference properties of association classes to identify related objects, as well as using object paths in input or output parameters for several methods.</span></span> <span data-ttu-id="e681f-105">Étant donné que les chemins d’accès aux objets sont traités comme des chaînes à des fins de recherche et de comparaison, la valeur d’un chemin d’accès d’objet lorsqu’il est utilisé comme propriété de référence est toujours la chaîne elle-même et non l’objet déréférencé.</span><span class="sxs-lookup"><span data-stu-id="e681f-105">Because object paths are treated as strings for the purpose of lookup and comparison, the value of an object path when used as a reference property is always the string itself and not the dereferenced object.</span></span> <span data-ttu-id="e681f-106">Les comparaisons de chaînes qui traitent les chemins d’accès aux objets sont toujours sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e681f-106">String comparisons that deal with object paths are always case-insensitive.</span></span>

<span data-ttu-id="e681f-107">Un chemin d’accès d’objet peut utiliser la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="e681f-107">An object path can use the following syntax:</span></span>

-   <span data-ttu-id="e681f-108">Chaînes contenues entre guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="e681f-108">Strings contained in single quotation marks.</span></span>
-   <span data-ttu-id="e681f-109">Barres obliques comme séparateurs.</span><span class="sxs-lookup"><span data-stu-id="e681f-109">Forward slashes as separators.</span></span>
-   <span data-ttu-id="e681f-110">Barres obliques inverses en tant que séparateurs.</span><span class="sxs-lookup"><span data-stu-id="e681f-110">Backslashes as separators.</span></span>
-   <span data-ttu-id="e681f-111">Constantes hexadécimales pour les entiers.</span><span class="sxs-lookup"><span data-stu-id="e681f-111">Hexadecimal constants for integers.</span></span>
-   <span data-ttu-id="e681f-112">Constantes booléennes pour les classes avec des clés qui acceptent des valeurs booléennes.</span><span class="sxs-lookup"><span data-stu-id="e681f-112">Boolean constants for classes with keys that take Boolean values.</span></span>
-   <span data-ttu-id="e681f-113">Notation d’URL pour représenter des caractères non imprimables, tels que %20 pour un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="e681f-113">URL notation to represent nonprinting characters, such as %20 for a blank space.</span></span>

<span data-ttu-id="e681f-114">En outre, une chaîne de chemin d’accès d’objet doit respecter les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e681f-114">In addition, an object path string must obey the following restrictions:</span></span>

-   <span data-ttu-id="e681f-115">Un serveur local supposé avec un chemin d’accès d’espace de noms partiel.</span><span class="sxs-lookup"><span data-stu-id="e681f-115">An assumed local server with a partial namespace path.</span></span> <span data-ttu-id="e681f-116">Par conséquent, la spécification de l’espace de noms root et default implique l’espace de noms racine et l’espace de noms par défaut sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="e681f-116">Thus, specifying the root and default namespace implies the root and default namespace on the local server.</span></span>
-   <span data-ttu-id="e681f-117">Aucun espace blanc dans un élément ou entre des éléments.</span><span class="sxs-lookup"><span data-stu-id="e681f-117">No white space either within an element or between elements.</span></span>
-   <span data-ttu-id="e681f-118">Les guillemets incorporés dans les chemins d’accès aux objets sont autorisés, mais doivent délimiter le guillemet avec les caractères d’échappement, comme dans une application C ou C++.</span><span class="sxs-lookup"><span data-stu-id="e681f-118">Embedded quotation marks in object paths are allowed but must delimit the quotation mark with escape characters, as in a C or C++ application.</span></span>
-   <span data-ttu-id="e681f-119">Seules les valeurs décimales sont reconnues comme des parties numériques de clés.</span><span class="sxs-lookup"><span data-stu-id="e681f-119">Only decimal values are recognized as numeric portions of keys.</span></span>

 

 



