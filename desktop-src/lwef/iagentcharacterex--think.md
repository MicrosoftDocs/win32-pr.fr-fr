---
title: IAgentCharacterEx réfléchir
description: IAgentCharacterEx réfléchir
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031144"
---
# <a name="iagentcharacterexthink"></a><span data-ttu-id="016b2-103">IAgentCharacterEx :: pensez</span><span class="sxs-lookup"><span data-stu-id="016b2-103">IAgentCharacterEx::Think</span></span>

<span data-ttu-id="016b2-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="016b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="016b2-105">Affiche la bulle de mot de pensée du caractère avec le texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="016b2-105">Displays the character's thought word balloon with the specified text.</span></span>

-   <span data-ttu-id="016b2-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="016b2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="016b2-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="016b2-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="016b2-108">Texte à afficher dans la bulle d’idée du caractère.</span><span class="sxs-lookup"><span data-stu-id="016b2-108">The text to appear in the character's thought balloon.</span></span>

</dd> <dt>

<span data-ttu-id="016b2-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="016b2-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="016b2-110">Adresse d’une variable qui reçoit l’ID de demande de **réflexion** .</span><span class="sxs-lookup"><span data-stu-id="016b2-110">Address of a variable that receives the **Think** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="016b2-111">À l’instar de la méthode [**IAgentCharacter :: Speak**](iagentcharacter--speak.md) , la méthode de **réflexion** est une demande en file d’attente qui affiche du texte dans une bulle de mot, sauf que les pensées s’affichent dans une bulle d’idées spéciale.</span><span class="sxs-lookup"><span data-stu-id="016b2-111">Like the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method, the **Think** method is a queued request that displays text in a word balloon, except that thoughts display in a special thought balloon.</span></span> <span data-ttu-id="016b2-112">La bulle de réflexion ne prend en charge que la balise de contrôle de voix de signets (**\\ MRK**) et ignore toutes les autres balises de contrôle vocal.</span><span class="sxs-lookup"><span data-stu-id="016b2-112">The thought balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="016b2-113">Contrairement à **IAgentCharacter :: Speak**, la méthode de **réflexion** ne modifie pas l’état d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="016b2-113">Unlike **IAgentCharacter::Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="016b2-114">Les paramètres de [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) s’appliquent également au style d’apparence de la bulle de pensée.</span><span class="sxs-lookup"><span data-stu-id="016b2-114">The [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) settings also apply to the appearance style of the thought balloon.</span></span> <span data-ttu-id="016b2-115">Par exemple, la propriété [**Enabled**](enabled-property.md) de la bulle doit également avoir la **valeur true** pour que le texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="016b2-115">For example, the balloon's [**Enabled**](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="016b2-116">La césure automatique des mots de Microsoft Agent dans le mot-bulle arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace et tabulation).</span><span class="sxs-lookup"><span data-stu-id="016b2-116">Microsoft Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="016b2-117">Toutefois, il peut également endommager un mot pour l’ajuster à l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="016b2-117">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="016b2-118">Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un espace de largeur nulle (0x200B) Unicode entre les caractères pour définir des césures lexicales.</span><span class="sxs-lookup"><span data-stu-id="016b2-118">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="016b2-119">Définissez l’ID de langue du caractère (à l’aide de [**IAgentCharacterEx :: SetLanguageID**](iagentcharacterex--setlanguageid.md) avant d’utiliser la méthode [**IAgentCharacter :: Speak**](iagentcharacter--speak.md) pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="016b2-119">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**IAgentCharacter::Speak**](iagentcharacter--speak.md) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="016b2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="016b2-120">See Also</span></span>

<span data-ttu-id="016b2-121">[**IAgentBalloon :: GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx :: SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter :: Speak**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="016b2-121">[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)</span></span>


 

 