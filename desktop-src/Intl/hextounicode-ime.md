---
description: La modification enrichie 3,0 prend en charge l’IME HexToUnicode, qui permet à un utilisateur d’effectuer une conversion entre des caractères hexadécimaux et Unicode à l’aide de touches d’accès rapide de l’une des deux manières suivantes.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: IME HexToUnicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530315"
---
# <a name="hextounicode-ime"></a><span data-ttu-id="89d56-103">IME HexToUnicode</span><span class="sxs-lookup"><span data-stu-id="89d56-103">HexToUnicode IME</span></span>

<span data-ttu-id="89d56-104">La modification enrichie 3,0 prend en charge l’IME HexToUnicode, qui permet à un utilisateur d’effectuer une conversion entre des caractères hexadécimaux et Unicode à l’aide de touches d’accès rapide de l’une des deux manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="89d56-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="89d56-105">À l’aide de la première méthode de conversion, l’utilisateur tape le code de caractère au format hexadécimal, puis entre ALT + X.</span><span class="sxs-lookup"><span data-stu-id="89d56-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="89d56-106">L’IME remplace les chiffres hexadécimaux précédant le point d’insertion par le caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="89d56-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="89d56-107">Si la police actuelle ne prend pas en charge le code de caractère, une police appropriée qui la prend en charge est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="89d56-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="89d56-108">Pour convertir du format Unicode au format hexadécimal, l’utilisateur entre MAJ + ALT + X.</span><span class="sxs-lookup"><span data-stu-id="89d56-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="89d56-109">Cette entrée remplace le caractère Unicode qui précède le point d’insertion par les chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="89d56-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="89d56-110">En particulier, cette méthode permet à l’utilisateur de déterminer le caractère indiqué par un indicateur « glyphe manquant ».</span><span class="sxs-lookup"><span data-stu-id="89d56-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="89d56-111">Si le code de caractère hexadécimal suit immédiatement certains caractères hexadécimaux (non caractères) légitimes, l’utilisateur sélectionne les chiffres spécifiques à convertir avant de taper ALT + X.</span><span class="sxs-lookup"><span data-stu-id="89d56-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="89d56-112">L’un des problèmes de cette première méthode est que ALT + X est parfois utilisé comme combinaison de touches pour la commande Exit (autrement dit, eXit).</span><span class="sxs-lookup"><span data-stu-id="89d56-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="89d56-113">Par exemple, dans Microsoft Office, cette commande s’affiche uniquement sous la forme d’une option du menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="89d56-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="89d56-114">La deuxième méthode de conversion entre les caractères hexadécimal et Unicode implique le pavé numérique.</span><span class="sxs-lookup"><span data-stu-id="89d56-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="89d56-115">À l’aide de cette méthode, l’utilisateur tape des nombres ALT + pavé numérique (avec des valeurs supérieures à 255) pour entrer des caractères Unicode à l’aide de valeurs décimales.</span><span class="sxs-lookup"><span data-stu-id="89d56-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="89d56-116">Cette méthode n’est pas aussi utile que la première car l’utilisateur ne peut pas voir les chiffres hexadécimaux qui ont été tapés.</span><span class="sxs-lookup"><span data-stu-id="89d56-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="89d56-117">En outre, l’utilisateur ne peut pas corriger les chiffres hexadécimaux, sauf en entrant à nouveau tous les chiffres.</span><span class="sxs-lookup"><span data-stu-id="89d56-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d56-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89d56-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d56-119">À propos du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="89d56-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



