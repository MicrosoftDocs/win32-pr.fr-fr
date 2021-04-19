---
description: L’opérateur LIKE détermine si une chaîne de caractères correspond à un modèle spécifié.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE, opérateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518415"
---
# <a name="like-operator"></a><span data-ttu-id="c66b8-103">LIKE, opérateur</span><span class="sxs-lookup"><span data-stu-id="c66b8-103">LIKE Operator</span></span>

<span data-ttu-id="c66b8-104">L’opérateur LIKE détermine si une chaîne de caractères correspond à un modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="c66b8-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="c66b8-105">Le modèle spécifié peut contenir exactement les caractères à faire correspondre, ou il peut contenir des caractères méta.</span><span class="sxs-lookup"><span data-stu-id="c66b8-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="c66b8-106">En effet, l’opérateur LIKE met en correspondance les sous-chaînes à l’aide des caractères génériques figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c66b8-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="c66b8-107">Caractère</span><span class="sxs-lookup"><span data-stu-id="c66b8-107">Character</span></span>       | <span data-ttu-id="c66b8-108">Description</span><span class="sxs-lookup"><span data-stu-id="c66b8-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c66b8-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="c66b8-109">\[ \]</span></span>           | <span data-ttu-id="c66b8-110">N’importe quel caractère dans la plage spécifiée ( \[ a-f \] ) ou Set ( \[ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="c66b8-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="c66b8-111">N’importe quel caractère ne figurant pas dans la plage ( \[ ^ a-f \] ) ou défini ( \[ ^ abcdef \] .)</span><span class="sxs-lookup"><span data-stu-id="c66b8-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="c66b8-112">Toute chaîne de 0 (zéro) ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="c66b8-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="c66b8-113">L’exemple suivant recherche toutes les instances où « Win » est trouvé n’importe où dans le nom de la classe : `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="c66b8-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="c66b8-114">\_ (trait de soulignement)</span><span class="sxs-lookup"><span data-stu-id="c66b8-114">\_ (underscore)</span></span> | <span data-ttu-id="c66b8-115">N’importe quel caractère.</span><span class="sxs-lookup"><span data-stu-id="c66b8-115">Any one character.</span></span> <span data-ttu-id="c66b8-116">Tout trait de soulignement littéral utilisé dans la chaîne de requête doit être placé dans une séquence d’échappement en le plaçant à l’intérieur de \[ \] (crochets).</span><span class="sxs-lookup"><span data-stu-id="c66b8-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="c66b8-117">Par exemple, le code PowerShell suivant récupère toutes les instances de la classe **Win32 \_ OperatingSystem** dont la propriété **Name** commence par **FirstName**:</span><span class="sxs-lookup"><span data-stu-id="c66b8-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="c66b8-118">Étant donné que le trait de soulignement est un caractère méta, si la cible de la requête a un trait de soulignement, les \[ \] caractères d’échappement «» doivent l’entourer.</span><span class="sxs-lookup"><span data-stu-id="c66b8-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="c66b8-119">Par exemple, vous pouvez interroger toutes les classes qui ont un double trait de soulignement dans le nom.</span><span class="sxs-lookup"><span data-stu-id="c66b8-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="c66b8-120">Pour rechercher toutes les classes avec un trait de soulignement double dans le nom, vous devez échapper les deux traits de soulignement avec \[ \] (crochets), par exemple :</span><span class="sxs-lookup"><span data-stu-id="c66b8-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="c66b8-121">Vous pouvez nier une instruction LIKE à l’aide de NOT ; pour ce faire, veillez à placer le non directement devant le nom du champ.</span><span class="sxs-lookup"><span data-stu-id="c66b8-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="c66b8-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c66b8-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="c66b8-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c66b8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c66b8-124">Opérateurs WQL</span><span class="sxs-lookup"><span data-stu-id="c66b8-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



