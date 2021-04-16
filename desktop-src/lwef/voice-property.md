---
title: Propriété Voice (objet Commands)
description: Voice, propriété
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0207fb4fb6f09d460496b6886354bc17738def17
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508237"
---
# <a name="voice-property-commands-object"></a><span data-ttu-id="8e011-103">Propriété Voice (objet Commands)</span><span class="sxs-lookup"><span data-stu-id="8e011-103">Voice Property (Commands Object)</span></span>

<span data-ttu-id="8e011-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8e011-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8e011-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="8e011-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8e011-106">Retourne ou définit le texte qui est passé à la grammaire du moteur de reconnaissance vocale (pour la reconnaissance).</span><span class="sxs-lookup"><span data-stu-id="8e011-106">Returns or sets the text that is passed to the speech engine grammar (for recognition).</span></span>

</dd> <dt>

<span data-ttu-id="8e011-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="8e011-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8e011-108">\*agent \***. Caractères («**_CharacterID_\*_»). Chaîne Commands. Voice_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="8e011-108">*agent\***.Characters ("**_CharacterID_*_").Commands.Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="8e011-109">Partie</span><span class="sxs-lookup"><span data-stu-id="8e011-109">Part</span></span>     | <span data-ttu-id="8e011-110">Description</span><span class="sxs-lookup"><span data-stu-id="8e011-110">Description</span></span>                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e011-111">*string*</span><span class="sxs-lookup"><span data-stu-id="8e011-111">*string*</span></span> | <span data-ttu-id="8e011-112">Expression de chaîne correspondant aux mots ou expressions à utiliser par le moteur de reconnaissance vocale pour la reconnaissance de cette commande.</span><span class="sxs-lookup"><span data-stu-id="8e011-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e011-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8e011-113">Remarks</span></span>

<span data-ttu-id="8e011-114">Si vous ne fournissez pas ce paramètre, le [**VoiceCaption**](voicecaption-property.md) de l’objet [**commandes**](/windows/desktop/lwef/the-commands-collection-object) n’apparaîtra pas dans la fenêtre commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="8e011-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span>

<span data-ttu-id="8e011-115">L’expression de chaîne que vous fournissez peut inclure des caractères de crochet ( \[ \] ) pour indiquer des mots facultatifs et des caractères de barre verticale ( \| ) pour indiquer d’autres chaînes.</span><span class="sxs-lookup"><span data-stu-id="8e011-115">The string expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="8e011-116">Les remplacements doivent être placés entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="8e011-116">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="8e011-117">Par exemple, « (Bonjour \[ Bonjour \] \| ) » indique au moteur de reconnaissance vocale d’accepter « Hello », « Hello This » ou « HI » pour la commande.</span><span class="sxs-lookup"><span data-stu-id="8e011-117">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="8e011-118">N’oubliez pas d’inclure des espaces appropriés entre le texte entre crochets ou entre parenthèses et le texte qui ne se trouve pas entre crochets ou entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="8e011-118">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span> <span data-ttu-id="8e011-119">Vous pouvez utiliser l’opérateur Star ( \* ) pour spécifier zéro, une ou plusieurs instances des mots inclus dans le groupe ou l’opérateur plus (+) pour spécifier une ou plusieurs instances.</span><span class="sxs-lookup"><span data-stu-id="8e011-119">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="8e011-120">Par exemple, le code suivant génère une grammaire qui prend en charge « essayez cela », veuillez essayer ceci « », veuillez essayer cela », avec des itérations illimitées de « veuillez » :</span><span class="sxs-lookup"><span data-stu-id="8e011-120">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="8e011-121">Le format de grammaire suivant exclut « essayer », car l’opérateur + définit au moins une instance de « veuillez » :</span><span class="sxs-lookup"><span data-stu-id="8e011-121">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="8e011-122">Les opérateurs de répétition suivent les règles de précédence normales et s’appliquent à l’élément de texte qui précède immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8e011-122">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="8e011-123">Par exemple, la grammaire suivante aboutit à « New York » et à « New York York », mais pas à « New York New York » :</span><span class="sxs-lookup"><span data-stu-id="8e011-123">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="8e011-124">Par conséquent, vous souhaitez généralement utiliser ces opérateurs avec les caractères de regroupement.</span><span class="sxs-lookup"><span data-stu-id="8e011-124">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="8e011-125">Par exemple, la grammaire suivante comprend à la fois « New York » et « New York New York » :</span><span class="sxs-lookup"><span data-stu-id="8e011-125">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="8e011-126">Les opérateurs de répétition sont utiles lorsque vous souhaitez composer une grammaire qui comprend une séquence répétée telle qu’un numéro de téléphone ou une spécification d’une liste d’éléments.</span><span class="sxs-lookup"><span data-stu-id="8e011-126">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="8e011-127">Bien que les opérateurs puissent également être utilisés avec le caractère facultatif de regroupement des crochets, cela peut réduire l’efficacité du traitement de l’agent de la grammaire.</span><span class="sxs-lookup"><span data-stu-id="8e011-127">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="8e011-128">Vous pouvez également utiliser des points de suspension (...) *pour prendre en* charge la détection de mots, c’est-à-dire dire au moteur de reconnaissance vocale d’ignorer les mots prononcés à cette position dans l’expression ( *parfois appelés «* mots de passe »).</span><span class="sxs-lookup"><span data-stu-id="8e011-128">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="8e011-129">Par conséquent, le moteur de reconnaissance vocale ne reconnaît que des mots spécifiques dans la chaîne, quel que soit le moment où il est parlé avec des mots ou expressions adjacents.</span><span class="sxs-lookup"><span data-stu-id="8e011-129">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="8e011-130">Par exemple, si vous définissez cette propriété sur « \[ ... \] vérifier \[ le courrier... \] », le moteur de reconnaissance vocale met en correspondance les expressions telles que « Veuillez vérifier la messagerie » ou « vérifier la messagerie » à cette commande.</span><span class="sxs-lookup"><span data-stu-id="8e011-130">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="8e011-131">Les ellipses peuvent être utilisées n’importe où dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="8e011-131">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="8e011-132">Toutefois, veillez à utiliser cette technique, car elle peut augmenter le potentiel des correspondances indésirables.</span><span class="sxs-lookup"><span data-stu-id="8e011-132">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="8e011-133">Quand vous définissez le mot grammaire pour votre commande, incluez au moins un mot requis ; autrement dit, évitez de fournir uniquement des mots facultatifs.</span><span class="sxs-lookup"><span data-stu-id="8e011-133">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="8e011-134">En outre, assurez-vous que le mot contient uniquement des mots et des lettres de prononce.</span><span class="sxs-lookup"><span data-stu-id="8e011-134">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="8e011-135">Pour les nombres, il est préférable d’épeler le mot plutôt que d’utiliser une représentation ambiguë.</span><span class="sxs-lookup"><span data-stu-id="8e011-135">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="8e011-136">Par exemple, « 345 » n’est pas une bonne forme de grammaire.</span><span class="sxs-lookup"><span data-stu-id="8e011-136">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="8e011-137">De même, au lieu de « IEEE », utilisez « I triple E ».</span><span class="sxs-lookup"><span data-stu-id="8e011-137">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="8e011-138">De même, omettez les signes de ponctuation ou les symboles.</span><span class="sxs-lookup"><span data-stu-id="8e011-138">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="8e011-139">Par exemple, au lieu de « The \# $1 10 pizza ! », utilisez « the number 1 10 dollar pizza ».</span><span class="sxs-lookup"><span data-stu-id="8e011-139">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="8e011-140">L’inclusion de caractères ou symboles non prononceables pour une commande peut entraîner l’échec du moteur de reconnaissance vocale à compiler la grammaire pour toutes vos commandes.</span><span class="sxs-lookup"><span data-stu-id="8e011-140">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="8e011-141">Enfin, rendez votre paramètre vocal aussi distinct que possible à partir d’autres commandes vocales que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="8e011-141">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="8e011-142">Plus la similarité entre la grammaire vocale pour les commandes est grande, plus le moteur de reconnaissance vocale est susceptible de générer une erreur de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="8e011-142">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="8e011-143">Vous pouvez également utiliser les scores de confiance pour mieux distinguer deux commandes qui peuvent avoir une grammaire vocale similaire ou similaire.</span><span class="sxs-lookup"><span data-stu-id="8e011-143">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="8e011-144">Vous pouvez inclure dans vos mots de grammaire sous la forme «*\\ prononciation du texte*», où *texte* est le texte affiché et la *prononciation* est le texte qui clarifie la prononciation.</span><span class="sxs-lookup"><span data-stu-id="8e011-144">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="8e011-145">Par exemple, la grammaire « 1er \\ prénom » est reconnue quand l’utilisateur dit « First », mais l’événement de [**commande**](command-event.md) retourne le texte « First \\ First ».</span><span class="sxs-lookup"><span data-stu-id="8e011-145">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](command-event.md) event will return the text, "1st\\first".</span></span> <span data-ttu-id="8e011-146">Vous pouvez également utiliser la Loi sur l’alphabet phonétique international pour spécifier une prononciation en commençant la prononciation par un signe dièse (« \# »), puis en incluant le texte représentant la prononciation de la Loi sur la Loi.</span><span class="sxs-lookup"><span data-stu-id="8e011-146">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="8e011-147">Pour les moteurs de reconnaissance vocale en japonais, vous pouvez définir la grammaire sous la forme «*Kana \\ kanji*», ce qui réduit les prononciations alternatives et l’amélioration de la précision.</span><span class="sxs-lookup"><span data-stu-id="8e011-147">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="8e011-148">(L’ordre est inversé pour des raisons de compatibilité descendante.) Ceci est particulièrement important pour la prononciation des noms corrects en kanji.</span><span class="sxs-lookup"><span data-stu-id="8e011-148">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="8e011-149">Toutefois, vous pouvez simplement passer le kanji sans le kana, auquel cas le moteur doit écouter toutes les prononciations acceptables pour le kanji.</span><span class="sxs-lookup"><span data-stu-id="8e011-149">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="8e011-150">Vous pouvez également passer en Kana uniquement.</span><span class="sxs-lookup"><span data-stu-id="8e011-150">You can also pass in just Kana.</span></span>

<span data-ttu-id="8e011-151">Notez également que pour les langues telles que le japonais, le chinois et le thaï, qui n’utilisent pas de caractères d’espace pour désigner les césures de mots, insérez un caractère d’espace de largeur nulle Unicode (0x200B) pour indiquer les césures de mots logiques.</span><span class="sxs-lookup"><span data-stu-id="8e011-151">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="8e011-152">À l’exception des erreurs utilisant les caractères de mise en forme de regroupement ou de répétition, l’agent ne signale pas les erreurs dans votre grammaire, à moins que le moteur lui-même ne signale l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8e011-152">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="8e011-153">Si vous transmettez au texte dans votre grammaire que le moteur ne parvient pas à se compiler, mais que le moteur ne gère pas et ne retourne pas d’erreur, l’agent ne peut pas signaler l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8e011-153">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="8e011-154">Par conséquent, l’application cliente doit définir avec soin la grammaire pour la propriété **Voice** .</span><span class="sxs-lookup"><span data-stu-id="8e011-154">Therefore, the client application must be carefully define grammar for the **Voice** property.</span></span>

> [!Note]  
> <span data-ttu-id="8e011-155">Les fonctionnalités grammaticales disponibles peuvent dépendre du moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="8e011-155">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="8e011-156">Vous pouvez consulter le fournisseur du moteur pour déterminer les options grammaticales prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8e011-156">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="8e011-157">Utilisez [**SRModeID**](srmodeid-property.md) pour utiliser un moteur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8e011-157">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="8e011-158">Le fonctionnement de cette propriété dépend de l’état de la propriété de reconnaissance vocale du serveur.</span><span class="sxs-lookup"><span data-stu-id="8e011-158">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="8e011-159">Par exemple, si la reconnaissance vocale est désactivée ou n’est pas installée, cette propriété n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="8e011-159">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
