---
title: Speak, méthode
description: Speak, méthode
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463047"
---
# <a name="speak-method"></a><span data-ttu-id="fb822-103">Speak, méthode</span><span class="sxs-lookup"><span data-stu-id="fb822-103">Speak Method</span></span>

<span data-ttu-id="fb822-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb822-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fb822-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="fb822-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fb822-106">Parle le texte ou le fichier audio spécifié pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="fb822-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="fb822-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="fb822-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fb822-108">\*agent ***. Caractères («*** CharacterID \* \* * »).* \*  \[ *Texte* Speak \] , \[ *URL*\]</span><span class="sxs-lookup"><span data-stu-id="fb822-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="fb822-109">Partie</span><span class="sxs-lookup"><span data-stu-id="fb822-109">Part</span></span>   | <span data-ttu-id="fb822-110">Description</span><span class="sxs-lookup"><span data-stu-id="fb822-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb822-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="fb822-111">*Text*</span></span> | <span data-ttu-id="fb822-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="fb822-112">Optional.</span></span> <span data-ttu-id="fb822-113">Chaîne qui spécifie ce que le caractère dit.</span><span class="sxs-lookup"><span data-stu-id="fb822-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="fb822-114">*Url*</span><span class="sxs-lookup"><span data-stu-id="fb822-114">*Url*</span></span>  | <span data-ttu-id="fb822-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="fb822-115">Optional.</span></span> <span data-ttu-id="fb822-116">Expression de chaîne spécifiant l’emplacement d’un fichier audio (. WAV ou. Format LWV).</span><span class="sxs-lookup"><span data-stu-id="fb822-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="fb822-117">L’emplacement peut être spécifié sous la forme d’un fichier (y compris une spécification de chemin d’accès UNC) ou d’une URL (lorsque les données d’animation de caractères sont également récupérées via le protocole HTTP).</span><span class="sxs-lookup"><span data-stu-id="fb822-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb822-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fb822-118">Remarks</span></span>

<span data-ttu-id="fb822-119">Bien que les paramètres *Text* et *URL* soient facultatifs, l’un d’eux doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="fb822-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="fb822-120">Pour utiliser cette méthode avec un caractère configuré pour parler uniquement dans sa bulle de mot ou à l’aide d’un moteur TTS (Text-to-Speech), fournissez simplement le paramètre *Text* .</span><span class="sxs-lookup"><span data-stu-id="fb822-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="fb822-121">Insérez un espace entre les mots pour définir les césures lexicales appropriées dans la bulle de mot, même pour les langues qui n’incluent pas traditionnellement des espaces.</span><span class="sxs-lookup"><span data-stu-id="fb822-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="fb822-122">Vous pouvez également inclure des caractères de barre verticale ( \| ) dans le paramètre *Text* pour désigner d’autres chaînes, afin que le serveur choisisse de manière aléatoire une autre chaîne chaque fois qu’il traite la méthode.</span><span class="sxs-lookup"><span data-stu-id="fb822-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="fb822-123">La prise en charge des caractères de la sortie TTS est définie lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fb822-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fb822-124">Pour générer une sortie TTS, un moteur TTS compatible doit déjà être installé avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fb822-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="fb822-125">Pour plus d’informations, consultez [accès aux services vocaux](accessing-speech-services.md).</span><span class="sxs-lookup"><span data-stu-id="fb822-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="fb822-126">Si vous utilisez le fichier audio enregistré (. WAV ou. LWV format uniquement) sortie pour le caractère, spécifiez l’emplacement du fichier dans le paramètre *URL* .</span><span class="sxs-lookup"><span data-stu-id="fb822-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="fb822-127">Cette spécification de fichier peut inclure un chemin d’accès local (absolu ou relatif) ou UNC (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="fb822-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="fb822-128">Le nom de fichier ne peut pas contenir de caractères non inclus dans la page de codes US 1252.</span><span class="sxs-lookup"><span data-stu-id="fb822-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="fb822-129">Toutefois, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' [**extraction**](get-method.md) pour charger l’animation avant d’appeler la méthode **Speak** .</span><span class="sxs-lookup"><span data-stu-id="fb822-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="fb822-130">Pour plus d’informations sur Creative, consultez [utilisation de l’outil de modification des informations linguistiques Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) . Fichiers LWV.</span><span class="sxs-lookup"><span data-stu-id="fb822-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="fb822-131">Lorsque vous utilisez la sortie enregistrée de fichier audio, vous pouvez toujours utiliser le paramètre text pour spécifier les mots qui apparaissent dans la bulle de *texte* du caractère.</span><span class="sxs-lookup"><span data-stu-id="fb822-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="fb822-132">Toutefois, si vous spécifiez un fichier audio linguistiquement amélioré (. LWV) pour le paramètre *URL* et ne spécifiez pas de texte pour le mot Balloon, le paramètre *Text* utilise le texte stocké dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="fb822-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="fb822-133">Vous pouvez également modifier les paramètres de la sortie vocale avec des balises spéciales que vous incluez dans le paramètre *Text* .</span><span class="sxs-lookup"><span data-stu-id="fb822-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="fb822-134">Pour plus d’informations, consultez [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="fb822-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="fb822-135">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="fb822-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="fb822-136">Vous pouvez l’utiliser pour synchroniser d’autres parties de votre code avec la sortie orale du caractère, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fb822-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



<span data-ttu-id="fb822-137">Vous pouvez également utiliser un objet de [**requête**](/windows/desktop/lwef/the-request-object) pour vérifier certaines conditions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fb822-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="fb822-138">Par exemple, si vous utilisez la méthode **Speak** pour parler et que vous n’avez pas de moteur TTS compatible installé, le serveur définit la propriété [**Status**](status-property.md) de l’objet **Request** sur « failed » et sa propriété [**Description**](description-property.md) sur « Class not registered » ou « Unknown or Object retournad Error ».</span><span class="sxs-lookup"><span data-stu-id="fb822-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="fb822-139">Pour déterminer si un moteur TTS est installé, utilisez la propriété [**TTSModeID**](ttsmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fb822-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="fb822-140">De même, si vous avez le caractère de la tentative de dicter un fichier audio, et si le fichier n’a pas été chargé ou qu’il y a un problème avec le périphérique audio, le serveur définit également la propriété [**Status**](status-property.md) de l’objet [**Request**](/windows/desktop/lwef/the-request-object) sur « failed » avec un numéro de code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="fb822-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="fb822-141">Vous pouvez également inclure des balises vocales de signets dans votre texte Speak pour synchroniser votre code :</span><span class="sxs-lookup"><span data-stu-id="fb822-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



<span data-ttu-id="fb822-142">Pour plus d’informations sur la balise de discours de signet, consultez [balises de sortie vocale](mrk-tag.md).</span><span class="sxs-lookup"><span data-stu-id="fb822-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="fb822-143">La méthode **Speak** utilise la dernière action jouée pour déterminer l’animation parlant à lire.</span><span class="sxs-lookup"><span data-stu-id="fb822-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="fb822-144">Par exemple, si vous avez précédé la commande **Speak** avec la [**lecture**](play-method.md) «**GestureRight**», le serveur lira **GestureRight** , puis l’animation **GestureRight** Speaking.</span><span class="sxs-lookup"><span data-stu-id="fb822-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="fb822-145">Si la dernière animation jouée n’a pas d’animation parlant, agent lit l’animation affectée à l’état de **conversation** du caractère.</span><span class="sxs-lookup"><span data-stu-id="fb822-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="fb822-146">Si vous appelez **Speak** et que le canal audio est occupé, la sortie audio du caractère n’est pas audible, mais le texte s’affiche dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="fb822-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="fb822-147">La césure automatique des mots de l’agent dans le mot-bulle arrête les mots à l’aide de caractères d’espace blanc (par exemple, espace ou tabulation).</span><span class="sxs-lookup"><span data-stu-id="fb822-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="fb822-148">Toutefois, si ce n’est pas le cas, il peut endommager un mot pour l’ajuster à la bulle.</span><span class="sxs-lookup"><span data-stu-id="fb822-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="fb822-149">Dans les langages tels que le japonais, le chinois et le thaï, où les espaces ne sont pas utilisés pour couper des mots, insérez un caractère d’espace de largeur nulle Unicode (0x200B) entre les caractères pour définir des césures lexicales.</span><span class="sxs-lookup"><span data-stu-id="fb822-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="fb822-150">La propriété [**Enabled**](enabled-property.md) de la bulle de mot doit également avoir la **valeur true** pour que le texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fb822-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb822-151">Définissez l’ID de langue du caractère (en définissant la valeur **LanguageID** du caractère avant d’utiliser la méthode **Speak** pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="fb822-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="fb822-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb822-152">See Also</span></span>

<span data-ttu-id="fb822-153">[**Événement Bookmark**](bookmark-event.md), [**événement RequestStart**](requeststart-event.md), [**événement RequestComplete**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="fb822-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 