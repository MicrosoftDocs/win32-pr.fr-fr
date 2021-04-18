---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509252"
---
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="b399b-103">IAgentCommand::SetVoice</span><span class="sxs-lookup"><span data-stu-id="b399b-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="b399b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b399b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="b399b-105">Définit la propriété [**Voice**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b399b-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="b399b-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b399b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b399b-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="b399b-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="b399b-108">BSTR qui spécifie le texte de la propriété [**Voice**](voice-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b399b-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="b399b-109">Une [**commande**](/windows/desktop/lwef/the-command-object) doit avoir sa propriété [**Voice**](voice-property.md) et la propriété [**Enabled**](enabled-property.md) définie sur la valeur Voice-accessible.</span><span class="sxs-lookup"><span data-stu-id="b399b-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="b399b-110">Sa propriété [**VoiceCaption**](voicecaption-property.md) doit également être définie pour s’afficher dans la **fenêtre commandes vocales**.</span><span class="sxs-lookup"><span data-stu-id="b399b-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="b399b-111">(Pour la compatibilité descendante, s’il n’y a aucun **VoiceCaption**, le paramètre de [**légende**](caption-property.md) est utilisé.)</span><span class="sxs-lookup"><span data-stu-id="b399b-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="b399b-112">L’expression BSTR que vous fournissez peut inclure des caractères de crochets ( \[ \] ) pour indiquer des mots facultatifs et des caractères de barre verticale ( \| ) pour indiquer d’autres chaînes.</span><span class="sxs-lookup"><span data-stu-id="b399b-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="b399b-113">Les remplacements doivent être placés entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b399b-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="b399b-114">Par exemple, « (Bonjour \[ Bonjour \] \| ) » indique au moteur de reconnaissance vocale d’accepter « Hello », « Hello This » ou « HI » pour la commande.</span><span class="sxs-lookup"><span data-stu-id="b399b-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="b399b-115">N’oubliez pas d’inclure des espaces appropriés entre le texte entre crochets ou entre parenthèses et le texte qui ne se trouve pas entre crochets ou entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b399b-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="b399b-116">Vous pouvez utiliser l’opérateur Star ( \* ) pour spécifier zéro, une ou plusieurs instances des mots inclus dans le groupe ou l’opérateur plus (+) pour spécifier une ou plusieurs instances.</span><span class="sxs-lookup"><span data-stu-id="b399b-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="b399b-117">Par exemple, le code suivant génère une grammaire qui prend en charge « essayez cela », veuillez essayer cela», et « veuillez essayer cela », avec des itérations illimitées de « veuillez » :</span><span class="sxs-lookup"><span data-stu-id="b399b-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="b399b-118">Le format de grammaire suivant exclut « essayer », car l’opérateur + définit au moins une instance de « veuillez » :</span><span class="sxs-lookup"><span data-stu-id="b399b-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="b399b-119">Les opérateurs de répétition suivent les règles de précédence normales et s’appliquent à l’élément de texte qui précède immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b399b-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="b399b-120">Par exemple, la grammaire suivante aboutit à « New York » et à « New York York », mais pas à « New York New York » :</span><span class="sxs-lookup"><span data-stu-id="b399b-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="b399b-121">Par conséquent, vous souhaiterez généralement utiliser ces opérateurs avec les caractères de regroupement.</span><span class="sxs-lookup"><span data-stu-id="b399b-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="b399b-122">Par exemple, la grammaire suivante comprend à la fois « New York » et « New York New York » :</span><span class="sxs-lookup"><span data-stu-id="b399b-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="b399b-123">Les opérateurs de répétition sont utiles lorsque vous souhaitez composer une grammaire qui comprend une séquence répétée telle qu’un numéro de téléphone ou une spécification d’une liste d’éléments :</span><span class="sxs-lookup"><span data-stu-id="b399b-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="b399b-124">Bien que les opérateurs puissent également être utilisés avec les crochets (un caractère de regroupement facultatif), cela peut réduire l’efficacité du traitement de la grammaire par l’agent.</span><span class="sxs-lookup"><span data-stu-id="b399b-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="b399b-125">Vous pouvez également utiliser des points de suspension (...) *pour prendre en* charge la détection de mots, c’est-à-dire dire au moteur de reconnaissance vocale d’ignorer les mots prononcés à cette position dans l’expression ( *parfois appelés «* mots de passe »).</span><span class="sxs-lookup"><span data-stu-id="b399b-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="b399b-126">Par conséquent, le moteur de reconnaissance vocale ne reconnaît que des mots spécifiques dans la chaîne, quel que soit le moment où il est parlé avec des mots ou expressions adjacents.</span><span class="sxs-lookup"><span data-stu-id="b399b-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="b399b-127">Par exemple, si vous définissez cette propriété sur « \[ ... \] vérifier \[ le courrier... \] » le moteur de reconnaissance vocale met en correspondance les expressions telles que « Veuillez vérifier la messagerie » ou « vérifier la messagerie » à cette commande.</span><span class="sxs-lookup"><span data-stu-id="b399b-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="b399b-128">Les ellipses peuvent être utilisées n’importe où dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b399b-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="b399b-129">Toutefois, soyez prudent en utilisant cette technique, car les paramètres vocaux avec ellipses peuvent augmenter le potentiel des correspondances indésirables.</span><span class="sxs-lookup"><span data-stu-id="b399b-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="b399b-130">Lorsque vous définissez les mots et la grammaire de votre commande, assurez-vous toujours d’inclure au moins un mot requis ; autrement dit, évitez de fournir uniquement des mots facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b399b-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="b399b-131">En outre, assurez-vous que le mot contient uniquement des mots et des lettres de prononce.</span><span class="sxs-lookup"><span data-stu-id="b399b-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="b399b-132">Pour les nombres, il est préférable d’épeler le mot plutôt que d’utiliser la représentation numérique.</span><span class="sxs-lookup"><span data-stu-id="b399b-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="b399b-133">De même, omettez les signes de ponctuation ou les symboles.</span><span class="sxs-lookup"><span data-stu-id="b399b-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="b399b-134">Par exemple, au lieu de « The \# $1 10 pizza ! », utilisez « the number 1 10 dollar pizza ».</span><span class="sxs-lookup"><span data-stu-id="b399b-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="b399b-135">L’inclusion de caractères ou symboles non prononceables pour une commande peut entraîner l’échec du moteur de reconnaissance vocale à compiler la grammaire pour toutes vos commandes.</span><span class="sxs-lookup"><span data-stu-id="b399b-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="b399b-136">Enfin, rendez votre paramètre vocal aussi distinct que possible à partir d’autres commandes vocales que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="b399b-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="b399b-137">Plus la similarité entre la grammaire vocale pour les commandes est grande, plus le moteur de reconnaissance vocale est susceptible de générer une erreur de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="b399b-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="b399b-138">Vous pouvez également utiliser les scores de confiance pour mieux distinguer deux commandes qui peuvent avoir une grammaire vocale similaire ou similaire.</span><span class="sxs-lookup"><span data-stu-id="b399b-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="b399b-139">La définition de la propriété [**Voice**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) active automatiquement les services vocaux de l’agent, ce qui rend la clé d’écoute et l’info-bulle d’écoute disponibles.</span><span class="sxs-lookup"><span data-stu-id="b399b-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="b399b-140">Toutefois, il ne charge pas le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="b399b-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="b399b-141">Les fonctionnalités grammaticales disponibles peuvent dépendre du moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="b399b-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="b399b-142">Vous pouvez consulter le fournisseur du moteur pour déterminer les options grammaticales prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b399b-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="b399b-143">Utilisez [**IAgentCharacterEx :: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) pour spécifier un moteur.</span><span class="sxs-lookup"><span data-stu-id="b399b-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b399b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b399b-144">See Also</span></span>

<span data-ttu-id="b399b-145">[**IAgentCommand :: GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="b399b-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 