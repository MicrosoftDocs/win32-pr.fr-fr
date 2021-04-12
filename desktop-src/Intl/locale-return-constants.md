---
description: '\_Constantes de retour de paramètres régionaux \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210052"
---
# <a name="locale_return-constants"></a><span data-ttu-id="fd7fe-103">\_Constantes de retour de paramètres régionaux \*</span><span class="sxs-lookup"><span data-stu-id="fd7fe-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="fd7fe-104">Cette rubrique définit les \_ constantes de retour de paramètres régionaux \* utilisées par nls.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd7fe-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd7fe-105">Value</span></span></th>
<th><span data-ttu-id="fd7fe-106">Signification</span><span class="sxs-lookup"><span data-stu-id="fd7fe-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd7fe-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="fd7fe-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="fd7fe-108"><strong>Windows 7 et versions ultérieures :</strong> Récupérez les noms génitif des mois, qui sont les noms utilisés lorsque les noms de mois sont combinés à d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="fd7fe-109">Par exemple, en ukrainien, l’équivalent de janvier est écrit &quot; Січень &quot; lorsque le mois est nommé seul.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="fd7fe-110">Toutefois, lorsque le nom du mois est utilisé en combinaison, par exemple, dans une date telle que le 5 janvier 2003, la forme génitif du nom est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="fd7fe-111">Pour l’exemple ukrainien, le nom du mois génitif s’affiche sous la forme &quot; 5 січня 2003 &quot; .</span><span class="sxs-lookup"><span data-stu-id="fd7fe-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="fd7fe-112">La liste des noms de mois génitif commence par janvier et est délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="fd7fe-113">S’il n’y a pas de 13e mois, utilisez un point-virgule à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fd7fe-114">Les noms de mois génitif n’existent pas dans toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd7fe-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="fd7fe-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="fd7fe-116"><strong>Windows Me/98, Windows NT 4,0 et versions ultérieures :</strong> Récupérez un nombre.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="fd7fe-117">Cette constante fait en sorte que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> récupère une valeur sous la forme d’un nombre et non sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="fd7fe-118">La mémoire tampon qui reçoit la valeur doit être au moins égale à la longueur d’une valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="fd7fe-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="fd7fe-119">Cette constante peut être combinée à toute autre constante dont le nom commence par &quot; LOCALE_I &quot; .</span><span class="sxs-lookup"><span data-stu-id="fd7fe-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




