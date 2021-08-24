---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45af753dea18e9fda7b613e3b800ac886d949eb6494fd969cd8b7ceb488dfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477239"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand::SetVoice

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Définit la propriété [**Voice**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR qui spécifie le texte de la propriété [**Voice**](voice-property.md) d’une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Une [**commande**](/windows/desktop/lwef/the-command-object) doit avoir sa propriété [**Voice**](voice-property.md) et la propriété [**Enabled**](enabled-property.md) définie sur la valeur Voice-accessible. Sa propriété [**VoiceCaption**](voicecaption-property.md) doit également être définie pour s’afficher dans la **fenêtre commandes vocales**. (Pour la compatibilité descendante, s’il n’y a aucun **VoiceCaption**, le paramètre de [**légende**](caption-property.md) est utilisé.)

L’expression BSTR que vous fournissez peut inclure des caractères de crochets ( \[ \] ) pour indiquer des mots facultatifs et des caractères de barre verticale ( \| ) pour indiquer d’autres chaînes. Les remplacements doivent être placés entre parenthèses. Par exemple, « (Bonjour \[ Bonjour \] \| ) » indique au moteur de reconnaissance vocale d’accepter « Hello », « Hello This » ou « HI » pour la commande. N’oubliez pas d’inclure des espaces appropriés entre le texte entre crochets ou entre parenthèses et le texte qui ne se trouve pas entre crochets ou entre parenthèses.

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

Par conséquent, vous souhaiterez généralement utiliser ces opérateurs avec les caractères de regroupement. Par exemple, la grammaire suivante comprend à la fois « New York » et « New York New York » :

``` syntax
   "(New York)+"
```

Les opérateurs de répétition sont utiles lorsque vous souhaitez composer une grammaire qui comprend une séquence répétée telle qu’un numéro de téléphone ou une spécification d’une liste d’éléments :

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Bien que les opérateurs puissent également être utilisés avec les crochets (un caractère de regroupement facultatif), cela peut réduire l’efficacité du traitement de la grammaire par l’agent.

Vous pouvez également utiliser des points de suspension (...) *pour prendre en* charge la détection de mots, c’est-à-dire dire au moteur de reconnaissance vocale d’ignorer les mots prononcés à cette position dans l’expression ( *parfois appelés «* mots de passe »). Par conséquent, le moteur de reconnaissance vocale ne reconnaît que des mots spécifiques dans la chaîne, quel que soit le moment où il est parlé avec des mots ou expressions adjacents. Par exemple, si vous définissez cette propriété sur « \[ ... \] vérifier \[ le courrier... \] » le moteur de reconnaissance vocale met en correspondance les expressions telles que « Veuillez vérifier la messagerie » ou « vérifier la messagerie » à cette commande. Les ellipses peuvent être utilisées n’importe où dans une chaîne. Toutefois, soyez prudent en utilisant cette technique, car les paramètres vocaux avec ellipses peuvent augmenter le potentiel des correspondances indésirables.

Lorsque vous définissez les mots et la grammaire de votre commande, assurez-vous toujours d’inclure au moins un mot requis ; autrement dit, évitez de fournir uniquement des mots facultatifs. En outre, assurez-vous que le mot contient uniquement des mots et des lettres de prononce. Pour les nombres, il est préférable d’épeler le mot plutôt que d’utiliser la représentation numérique. De même, omettez les signes de ponctuation ou les symboles. Par exemple, au lieu de « The \# $1 10 pizza ! », utilisez « the number 1 10 dollar pizza ». L’inclusion de caractères ou symboles non prononceables pour une commande peut entraîner l’échec du moteur de reconnaissance vocale à compiler la grammaire pour toutes vos commandes. Enfin, rendez votre paramètre vocal aussi distinct que possible à partir d’autres commandes vocales que vous définissez. Plus la similarité entre la grammaire vocale pour les commandes est grande, plus le moteur de reconnaissance vocale est susceptible de générer une erreur de reconnaissance. Vous pouvez également utiliser les scores de confiance pour mieux distinguer deux commandes qui peuvent avoir une grammaire vocale similaire ou similaire.

La définition de la propriété [**Voice**](voice-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object) active automatiquement les services vocaux de l’agent, ce qui rend la clé d’écoute et l’info-bulle d’écoute disponibles. Toutefois, il ne charge pas le moteur de reconnaissance vocale.

> [!Note]  
> Les fonctionnalités grammaticales disponibles peuvent dépendre du moteur de reconnaissance vocale. Vous pouvez consulter le fournisseur du moteur pour déterminer les options grammaticales prises en charge. Utilisez [**IAgentCharacterEx :: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) pour spécifier un moteur.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCommand :: GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand :: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 