---
title: IAgentCharacter parler
description: IAgentCharacter parler
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507902"
---
# <a name="iagentcharacterspeak"></a><span data-ttu-id="12503-103">IAgentCharacter :: Speak</span><span class="sxs-lookup"><span data-stu-id="12503-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="12503-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="12503-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="12503-105">Parle du fichier texte ou audio.</span><span class="sxs-lookup"><span data-stu-id="12503-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="12503-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="12503-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="12503-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="12503-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="12503-108">Texte que le caractère doit prononcer.</span><span class="sxs-lookup"><span data-stu-id="12503-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="12503-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span><span class="sxs-lookup"><span data-stu-id="12503-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="12503-110">URL (ou spécification de fichier) d’un fichier audio à utiliser pour la sortie parlée.</span><span class="sxs-lookup"><span data-stu-id="12503-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="12503-111">Il peut s’agir d’un fichier audio standard (. WAV) ou fichier audio linguistiquement amélioré (. LWV).</span><span class="sxs-lookup"><span data-stu-id="12503-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="12503-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="12503-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="12503-113">Adresse d’une variable qui reçoit l’ID de demande [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="12503-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="12503-114">Pour utiliser cette méthode avec un caractère configuré pour parler à l’aide d’un moteur TTS (Text-to-Speech); il vous suffit de fournir le paramètre *bszText* .</span><span class="sxs-lookup"><span data-stu-id="12503-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="12503-115">Vous pouvez inclure des caractères de barre verticale ( \| ) dans le paramètre *bszText* pour désigner d’autres chaînes, afin que chaque fois que le serveur traite la méthode, il choisit de façon aléatoire une autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="12503-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="12503-116">La prise en charge de la sortie TTS est définie lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="12503-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="12503-117">Si vous souhaitez utiliser la sortie de fichier audio pour le caractère, spécifiez l’emplacement du fichier dans le paramètre *bszURL* .</span><span class="sxs-lookup"><span data-stu-id="12503-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="12503-118">Lorsque vous utilisez le protocole HTTP pour télécharger un fichier audio, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité du fichier avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="12503-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="12503-119">Vous pouvez utiliser le paramètre *bszText* pour spécifier les mots qui s’affichent dans la bulle de texte du caractère.</span><span class="sxs-lookup"><span data-stu-id="12503-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="12503-120">Si vous spécifiez un fichier audio linguistiquement amélioré (. LWV) pour le paramètre *bszURL* et ne spécifient pas de texte, le paramètre *bszText* utilise le texte stocké dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="12503-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="12503-121">La méthode [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) utilise la dernière animation jouée pour déterminer l’animation parlant à lire.</span><span class="sxs-lookup"><span data-stu-id="12503-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="12503-122">Par exemple, si vous faites précéder la commande **Speak** d’un [**IAgentCharacter ::P Posez**](iagentcharacter--play.md) «**GestureRight**», le serveur lira **GestureRight** , puis l’animation **GestureRight** Speaking.</span><span class="sxs-lookup"><span data-stu-id="12503-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="12503-123">Si la dernière animation jouée n’a pas d’animation parlante, Microsoft Agent lit l’animation affectée à l’état de **conversation** du caractère.</span><span class="sxs-lookup"><span data-stu-id="12503-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="12503-124">Si vous appelez [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) et que le canal audio est occupé, la sortie audio du caractère n’est pas audible, mais le texte s’affiche dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="12503-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="12503-125">La propriété [Enabled](enabled-property.md) de l’info-bulle du mot doit également avoir la **valeur true** pour que le texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="12503-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="12503-126">La césure automatique des mots de Microsoft Agent dans la bulle de mot, arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace et tabulation).</span><span class="sxs-lookup"><span data-stu-id="12503-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="12503-127">Toutefois, il peut également endommager un mot pour l’ajuster à l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="12503-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="12503-128">Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un espace de largeur nulle (0x200B) Unicode entre les caractères pour définir des césures lexicales.</span><span class="sxs-lookup"><span data-stu-id="12503-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="12503-129">Définissez l’ID de langue du caractère (à l’aide de [**IAgentCharacterEx :: SetLanguageID**](iagentcharacterex--setlanguageid.md) avant d’utiliser la méthode [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="12503-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="12503-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12503-130">See Also</span></span>

<span data-ttu-id="12503-131">[**IAgentCharacter ::P poser**](iagentcharacter--play.md), [**IAgentBalloon :: GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter ::P**](iagentcharacter--prepare.md) restante</span><span class="sxs-lookup"><span data-stu-id="12503-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 