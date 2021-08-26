---
title: IAgentCommands SetVoice
description: IAgentCommands SetVoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02fb124b51a3be1796258fdcb8ffa31d8b81b59636027f3d99497b27cd2bd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961899"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands::SetVoice

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Définit la propriété de texte [**vocal**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR qui spécifie la valeur de la propriété texte [**vocal**](voice-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

La propriété de texte [**vocal**](voice-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) doit être définie sur Voice-accessible. Elle doit également avoir la propriété [**VoiceCaption**](voicecaption-property.md) ou [**Caption**](caption-property.md) définie pour s’afficher dans la fenêtre commandes vocales et sa propriété [**visible**](visible-property.md) définie sur **true** pour apparaître dans le menu contextuel du caractère.

L’expression BSTR que vous fournissez peut inclure des caractères de crochets ( \[ \] ) pour indiquer des mots facultatifs et des caractères de barre verticale ( \| ) pour indiquer d’autres chaînes. Les remplacements doivent être placés entre parenthèses. Par exemple, « (Bonjour \[ Bonjour \] \| ) » indique au moteur de reconnaissance vocale d’accepter « Hello », « Hello This » ou « HI » pour la commande. N’oubliez pas d’inclure des espaces appropriés entre les mots que vous incluez entre crochets ou entre parenthèses, ainsi que d’autres textes. N’oubliez pas d’inclure des espaces appropriés entre le texte entre crochets ou entre parenthèses et le texte qui ne se trouve pas entre crochets ou entre parenthèses.

Vous pouvez utiliser l’opérateur Star ( \* ) pour spécifier zéro, une ou plusieurs instances des mots inclus dans le groupe ou l’opérateur plus (+) pour spécifier une ou plusieurs instances. Par exemple, le code suivant génère une grammaire qui prend en charge « essayez cela », veuillez essayer cela», et « veuillez essayer cela », avec des itérations illimitées de « veuillez » :

``` syntax
   "please* try this"
```

Le format de grammaire suivant exclut « essayer », car l’opérateur + définit au moins une instance de « veuillez » :

``` syntax
   "please+ try this"
```

Les opérateurs de répétition suivent les règles de précédence normales et s’appliquent à l’élément de texte qui précède immédiatement. Par exemple, la grammaire suivante aboutit à « New York » et à « New York York », mais pas à « New York New York » :

``` syntax
   "New York+"
```

Par conséquent, vous souhaitez généralement utiliser ces opérateurs avec les caractères de regroupement. Par exemple, la grammaire suivante comprend à la fois « New York » et « New York New York » :

``` syntax
   "(New York)+"
```

Les opérateurs de répétition sont utiles lorsque vous souhaitez composer une grammaire qui comprend une séquence répétée telle qu’un numéro de téléphone ou une spécification d’une liste d’éléments :

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Bien que les opérateurs puissent également être utilisés avec des crochets (un caractère de regroupement facultatif), cela peut réduire l’efficacité du traitement de la grammaire par l’agent.

Vous pouvez également utiliser des points de suspension (...) *pour prendre en* charge la détection de mots, c’est-à-dire dire au moteur de reconnaissance vocale d’ignorer les mots prononcés à cette position dans l’expression ( *parfois appelés «* mots de passe »). Lorsque vous utilisez des ellipses, le moteur de reconnaissance vocale ne reconnaît que des mots spécifiques dans la chaîne, quel que soit le moment où il est parlé avec des mots ou expressions adjacents. Par exemple, si vous définissez cette propriété sur « \[ ... \] vérifier \[ le courrier... \] » le moteur de reconnaissance vocale met en correspondance les expressions telles que « Veuillez vérifier la messagerie » ou « vérifier la messagerie » à cette commande. Les ellipses peuvent être utilisées n’importe où dans une chaîne. Toutefois, soyez prudent lorsque vous utilisez cette technique, car les paramètres vocaux avec ellipses peuvent augmenter le potentiel des correspondances indésirables.

Lorsque vous définissez les mots et la grammaire de votre commande, incluez au moins un mot requis ; autrement dit, évitez de fournir uniquement des mots facultatifs. En outre, assurez-vous que le mot contient uniquement des mots et des lettres de prononce. Pour les nombres, il est préférable d’épeler le mot plutôt que d’utiliser une représentation ambiguë. Par exemple, « 345 » n’est pas une bonne forme de grammaire. De même, au lieu de « IEEE », utilisez « I triple E ». De même, omettez les signes de ponctuation ou les symboles. Par exemple, au lieu de « The \# $1 10 pizza ! », utilisez « the number 1 10 dollar pizza ». L’inclusion de caractères ou symboles non prononceables pour une commande peut entraîner l’échec du moteur de reconnaissance vocale à compiler la grammaire pour toutes vos commandes. Enfin, rendez votre paramètre vocal aussi distinct que possible à partir d’autres commandes vocales que vous définissez. Plus la similarité entre la grammaire vocale pour les commandes est grande, plus le moteur de reconnaissance vocale est susceptible de générer une erreur de reconnaissance. Vous pouvez également utiliser les scores de confiance pour mieux distinguer deux commandes qui peuvent avoir une grammaire vocale similaire ou similaire.

Vous pouvez inclure dans vos mots de grammaire sous la forme «*\\ prononciation du texte*», où « texte » est le texte affiché et « prononciation » un texte qui clarifie la prononciation. Par exemple, la grammaire, « premier \\ prénom », est reconnue quand l’utilisateur dit « First », mais l’événement de [**commande**](/windows/desktop/lwef/the-command-object) retourne le texte « First \\ First ». Vous pouvez également utiliser la Loi sur l’alphabet phonétique international pour spécifier une prononciation en commençant par un signe dièse (« \# »), puis le texte représentant la prononciation de la Loi sur la Loi.

Pour les moteurs de reconnaissance vocale en japonais, vous pouvez définir la grammaire sous la forme «*Kana \\ kanji*», en réduisant les autres prononciations et en renforçant la précision. (L’ordre est inversé pour des raisons de compatibilité descendante.) Ceci est particulièrement important pour la prononciation des noms corrects en kanji. Toutefois, vous pouvez simplement transmettre « kanji », sans le kana, auquel cas le moteur doit écouter toutes les prononciations acceptables pour le kanji. Vous pouvez également passer en Kana uniquement.

À l’exception des erreurs qui utilisent les caractères de mise en forme de regroupement ou de répétition, Microsoft Agent ne signale pas les erreurs dans votre grammaire, sauf si le moteur lui-même signale l’erreur. Si vous transmettez au texte dans votre grammaire que le moteur ne parvient pas à se compiler, mais que le moteur ne gère pas et ne retourne pas d’erreur, l’agent ne peut pas signaler l’erreur. Par conséquent, l’application cliente doit faire attention à définir la grammaire de la propriété [**Voice**](voice-property.md) .

> [!Note]  
> Les fonctionnalités grammaticales disponibles peuvent dépendre du moteur de reconnaissance vocale. Vous pouvez consulter le fournisseur du moteur pour déterminer les options grammaticales prises en charge. Utilisez [**SRModeID**](srmodeid-property.md) pour utiliser un moteur spécifique.

 

Le fonctionnement de cette propriété dépend de l’état de la reconnaissance vocale du serveur Microsoft Agent. Par exemple, si la reconnaissance vocale est désactivée ou n’est pas installée, cette fonction n’a aucun effet immédiat. Toutefois, si la reconnaissance vocale est activée au cours d’une session, la commande devient accessible lorsque son application cliente est active.

## <a name="see-also"></a>Voir aussi

[**IAgentCommands :: GetVoice**](iagentcommands--getvoice.md), [**IAgentCommands :: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands :: setVisible**](iagentcommands--setvisible.md)


 

 