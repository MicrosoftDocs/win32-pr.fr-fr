---
title: Propriété Voice (objet Command)
description: Voice, propriété
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8f9003b5200882fc01ee37edb868a261c68c7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511730"
---
# <a name="voice-property-command-object"></a>Propriété Voice (objet Command)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le texte qui est passé à la grammaire du moteur de reconnaissance vocale (pour la reconnaissance) pour la correspondance de cette [**commande**](/windows/desktop/lwef/the-command-object) pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_*_»)._ *  \[  =  *Chaîne* vocale\]



| Partie     | Description                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Expression de chaîne correspondant aux mots ou expressions à utiliser par le moteur de reconnaissance vocale pour la reconnaissance de cette [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous ne fournissez pas ce paramètre, le [**VoiceCaption**](voicecaption-property.md) de l’objet [**commandes**](/windows/desktop/lwef/the-commands-collection-object) n’apparaîtra pas dans la fenêtre commandes vocales. Si vous spécifiez un paramètre [**vocal**](voice-property.md) , mais pas un **VoiceCaption** (ou une [**légende**](https://www.bing.com/search?q=**Caption**)), la commande n’apparaît pas dans la fenêtre commandes vocales, mais elle est accessible en voix lorsque l’application cliente devient entrée-active.

Votre expression de chaîne peut inclure des crochets ( \[ \] ) pour indiquer des mots facultatifs et des caractères de barre verticale ( \| ) pour indiquer d’autres chaînes. Les remplacements doivent être placés entre parenthèses. Par exemple, « (Bonjour \[ Bonjour \] \| ) » indique au moteur de reconnaissance vocale d’accepter « Hello », « Hello This » ou « HI » pour la commande. N’oubliez pas d’inclure des espaces appropriés entre le texte entre crochets ou entre parenthèses et le texte qui ne se trouve pas entre crochets ou entre parenthèses.

Vous pouvez utiliser l’opérateur Star ( \* ) pour spécifier zéro, une ou plusieurs instances des mots inclus dans le groupe ou l’opérateur plus (+) pour spécifier une ou plusieurs instances. Par exemple, le code suivant génère une grammaire qui prend en charge « essayez cela », veuillez essayer ceci « », veuillez essayer cela », avec des itérations illimitées de « veuillez » :


```
   "please* try this"
```



Le format de grammaire suivant exclut « essayer », car l’opérateur + définit au moins une instance de « veuillez » :


```
   "please+ try this"
```



Les opérateurs de répétition suivent les règles de précédence normales et s’appliquent à l’élément de texte qui précède immédiatement. Par exemple, la grammaire suivante aboutit à « New York » et à « New York York », mais pas à « New York New York » :


```
   "New York+"
```



Par conséquent, vous souhaitez généralement utiliser ces opérateurs avec les caractères de regroupement. Par exemple, la grammaire suivante comprend à la fois « New York » et « New York New York » :


```
   "(New York)+"
```



Les opérateurs de répétition sont utiles lorsque vous souhaitez composer une grammaire qui comprend une séquence répétée telle qu’un numéro de téléphone ou une spécification d’une liste d’éléments.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Bien que les opérateurs puissent également être utilisés avec le caractère facultatif de regroupement des crochets, cela peut réduire l’efficacité du traitement de l’agent de la grammaire.

Vous pouvez également utiliser des points de suspension (...) *pour prendre en* charge la détection de mots, c’est-à-dire dire au moteur de reconnaissance vocale d’ignorer les mots prononcés à cette position dans l’expression ( *parfois appelés «* mots de passe »). Par conséquent, le moteur de reconnaissance vocale ne reconnaît que des mots spécifiques dans la chaîne, quel que soit le moment où il est parlé avec des mots ou expressions adjacents. Par exemple, si vous définissez cette propriété sur « \[ ... \] vérifier \[ le courrier... \] », le moteur de reconnaissance vocale met en correspondance les expressions telles que « Veuillez vérifier la messagerie » ou « vérifier la messagerie » à cette commande. Les ellipses peuvent être utilisées n’importe où dans une chaîne. Toutefois, veillez à utiliser cette technique, car elle peut augmenter le potentiel des correspondances indésirables.

Quand vous définissez le mot grammaire pour votre commande, incluez au moins un mot requis ; autrement dit, évitez de fournir uniquement des mots facultatifs. En outre, assurez-vous que le mot contient uniquement des mots et des lettres de prononce. Pour les nombres, il est préférable d’épeler le mot plutôt que d’utiliser une représentation ambiguë. Par exemple, « 345 » n’est pas une bonne forme de grammaire. De même, au lieu de « IEEE », utilisez « I triple E ». De même, omettez les signes de ponctuation ou les symboles. Par exemple, au lieu de « The \# $1 10 pizza ! », utilisez « the number 1 10 dollar pizza ». L’inclusion de caractères ou symboles non prononceables pour une commande peut entraîner l’échec du moteur de reconnaissance vocale à compiler la grammaire pour toutes vos commandes. Enfin, rendez votre paramètre vocal aussi distinct que possible à partir d’autres commandes vocales que vous définissez. Plus la similarité entre la grammaire vocale pour les commandes est grande, plus le moteur de reconnaissance vocale est susceptible de générer une erreur de reconnaissance. Vous pouvez également utiliser les scores de confiance pour mieux distinguer deux commandes qui peuvent avoir une grammaire vocale similaire ou similaire.

Vous pouvez inclure dans vos mots de grammaire sous la forme «*\\ prononciation du texte*», où *texte* est le texte affiché et la *prononciation* est le texte qui clarifie la prononciation. Par exemple, la grammaire « 1er \\ prénom » est reconnue quand l’utilisateur dit « First », mais l’événement de [**commande**](/windows/desktop/lwef/the-command-object) retourne le texte « First \\ First ». Vous pouvez également utiliser la Loi sur l’alphabet phonétique international pour spécifier une prononciation en commençant la prononciation par un signe dièse (« \# »), puis en incluant le texte représentant la prononciation de la Loi sur la Loi.

Pour les moteurs de reconnaissance vocale en japonais, vous pouvez définir la grammaire sous la forme «*Kana \\ kanji*», ce qui réduit les prononciations alternatives et l’amélioration de la précision. (L’ordre est inversé pour des raisons de compatibilité descendante.) Ceci est particulièrement important pour la prononciation des noms corrects en kanji. Toutefois, vous pouvez simplement passer le kanji sans le kana, auquel cas le moteur doit écouter toutes les prononciations acceptables pour le kanji. Vous pouvez également passer en Kana uniquement.

Notez également que pour les langues telles que le japonais, le chinois et le thaï, qui n’utilisent pas de caractères d’espace pour désigner les césures de mots, insérez un caractère d’espace de largeur nulle Unicode (0x200B) pour indiquer les césures de mots logiques.

À l’exception des erreurs utilisant les caractères de mise en forme de regroupement ou de répétition, l’agent ne signale pas les erreurs dans votre grammaire, à moins que le moteur lui-même ne signale l’erreur. Si vous transmettez au texte dans votre grammaire que le moteur ne parvient pas à se compiler, mais que le moteur ne gère pas et ne retourne pas d’erreur, l’agent ne peut pas signaler l’erreur. Par conséquent, l’application cliente doit définir avec soin la grammaire pour la propriété [**Voice**](voice-property.md) .

> [!Note]  
> Les fonctionnalités grammaticales disponibles peuvent dépendre du moteur de reconnaissance vocale. Vous pouvez consulter le fournisseur du moteur pour déterminer les options grammaticales prises en charge. Utilisez [**SRModeID**](srmodeid-property.md) pour utiliser un moteur spécifique.

 

Le fonctionnement de cette propriété dépend de l’état de la propriété de reconnaissance vocale du serveur. Par exemple, si la reconnaissance vocale est désactivée ou n’est pas installée, cette propriété n’a aucun effet.

 

 
