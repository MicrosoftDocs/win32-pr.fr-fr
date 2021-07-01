---
title: Clarifier et limiter les choix
description: Clarifier et limiter les choix
ms.assetid: 4ec3ca01-231b-4a45-aae1-fba5b2ba0033
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953001d706089244d6366c8dab0cdb580a2d72ca
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118474"
---
# <a name="clarify-and-limit-choices"></a>Clarifier et limiter les choix

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La reconnaissance vocale est plus efficace lorsque l’utilisateur apprend la plage de la grammaire appropriée. Elle fonctionne également mieux lorsque la gamme de choix est limitée. Moins l’entrée est terminée, plus le moteur de reconnaissance vocale peut analyser l’entrée d’informations acoustiques.

Microsoft Agent comprend plusieurs dispositions intégrées qui augmentent la réussite de l’entrée vocale. La première est la fenêtre commandes qui s’affiche lorsque l’utilisateur dit : « ouvrir la fenêtre commandes » ou « que puis-je prononcer ? ». (ou lorsque l’utilisateur choisit ouvrir la fenêtre commandes dans le menu contextuel du caractère). La fenêtre de commande sert de guide visuel à la grammaire active du moteur de reconnaissance vocale. Elle réduit également les erreurs de reconnaissance en activant uniquement la grammaire vocale de l’application d’entrée active et les commandes globales de Microsoft Agent. Par conséquent, la grammaire active du moteur de reconnaissance vocale s’applique au contexte immédiat. Pour plus d’informations sur la fenêtre commandes, consultez [vue d’ensemble de l’interface de programmation de Microsoft Agent](microsoft-agent-programming-interface-overview.md).

Lorsque vous créez des commandes vocales Microsoft Agent, vous pouvez créer le texte de légende qui apparaît dans la fenêtre commandes ainsi que son texte vocal (grammaire), les mots que le moteur doit utiliser pour faire correspondre cette commande. Essayez toujours de rendre vos commandes aussi distinctives que possible. Plus la différence entre le libellé des commandes est importante, en particulier pour le texte vocal, plus le moteur de reconnaissance vocale est susceptible de faire la distinction entre les commandes vocales et de fournir une correspondance exacte. Évitez également les commandes à mot unique ou très courtes. En général, des informations plus acoustiques dans un énoncé oral donnent au moteur une meilleure chance de faire une correspondance exacte.

Lors de la définition du texte vocal d’une commande, fournissez une variété raisonnable de formulations. Les demandes qui signifient la même chose peuvent être formulées très différemment, comme illustré dans l’exemple suivant :

Ajoutez des pepperoni.

J’aimerais des pepperoni.

Pouvez-vous ajouter des pepperoni ?

Pepperoni, veuillez.

Microsoft agent vous permet de spécifier facilement des alternatives ou des mots facultatifs pour la grammaire vocale de votre application. Vous placez des mots ou des expressions de substitution entre parenthèses, séparés par un caractère de barre verticale. Vous pouvez définir des mots facultatifs en les mettant entre crochets. Vous pouvez également imbriquer des alternatives ou des mots facultatifs. En outre, vous pouvez également utiliser des points de suspension (...) dans le texte de la voix comme un espace réservé pour un mot. Toutefois, si vous utilisez des ellipses trop fréquemment, il peut être plus difficile pour le moteur de faire la distinction entre les différentes commandes vocales. Dans tous les cas, assurez-vous toujours que votre texte vocal contient au moins un mot distinctif pour chaque commande qui n’est pas facultative. En règle générale, ce mot de passe doit correspondre à un ou plusieurs mots dans le texte de légende que vous définissez et qui apparaît dans la fenêtre commandes.

Bien que vous puissiez inclure des symboles, des signes de ponctuation ou des abréviations dans le texte de votre légende, évitez-les dans votre texte vocal. De nombreux moteurs de reconnaissance vocale ne peuvent pas gérer les symboles et les abréviations ou peuvent les utiliser pour définir des paramètres d’entrée spéciaux. En outre, écrivez des chiffres. Cela garantit également une prise en charge de la reconnaissance plus fiable.

Vous pouvez également utiliser des invites de directive pour éviter une entrée ouverte. Les invites de directives référencent implicitement les choix ou les signalent explicitement, comme indiqué dans les exemples suivants :



| Prompt                                           | Évaluation                                                    |
|--------------------------------------------|-----------------------------------------------------|
| Que veux-tu?                          | Trop général, une demande ouverte                  |
| Choisissez un style de pizza ou un ingrédient.        | Bon, si les choix sont visibles, mais toujours généraux     |
| Dites « Hawaii », « Chicago » ou « The Works ». | Mieux, une directive explicite avec des options spécifiques |



 

Cela Guide l’utilisateur vers l’émission d’une commande valide. En suggérant les mots ou l’expression, il est plus probable que vous reveniez à la formulation attendue. Pour éviter une répétition naturelle, modifiez la formulation ou raccourcissez l’original pour la présentation suivante à mesure que l’utilisateur devient plus expérimenté avec le style d’entrée. Les invites de directive peuvent également être utilisées dans les situations où l’utilisateur ne parvient pas à émettre une commande dans un délai imparti ou ne parvient pas à fournir une commande attendue. Les invites de directive peuvent être fournies à l’aide de la sortie vocale, de vos interfaces d’application, ou des deux. La clé permet à l’utilisateur de connaître les choix appropriés.

La formulation influence la réussite d’une invite. Par exemple, l’invite « voulez-vous commander votre pizza ? » peut générer une réponse « oui » ou « non », mais elle peut également générer une demande de commande. Définissez les invites de manière à ce qu’elles soient non ambiguës ou soyez prêtes à accepter un plus grand nombre de réponses possibles. En outre, notez la tendance pour que les gens imitent les mots et les constructions qu’ils entendent. Cela peut souvent être utilisé pour évoquer une réponse appropriée, comme dans l’exemple suivant :

**Utilisateur :** Afficher tous les messages de Paul.

**Symbole**

Cela est plus susceptible de provoquer le nom complet de l’une des parties avec le préfixe possible « je signifie » ou « je veux ».

Étant donné que les caractères Microsoft Agent fonctionnent dans l’interface visuelle de Microsoft Windows, vous pouvez utiliser des éléments visuels pour fournir des invites de directives pour les entrées vocales. Par exemple, vous pouvez avoir le geste de caractère dans une liste de choix et demander que l’utilisateur en sélectionne un, ou afficher les choix dans une boîte de dialogue ou une fenêtre de message. Cela présente deux avantages : il suggère explicitement les mots que vous souhaitez que l’utilisateur parle et il fournit une autre façon pour l’utilisateur de répondre.

Vous pouvez également utiliser d’autres modes d’interaction pour suggérer discrètement aux utilisateurs la grammaire vocale appropriée, comme illustré dans l’exemple suivant :

**Utilisateur :** (cliquer sur l’option pizza de style Hawaii avec la souris)

**Caractère :** Hawaii-type pizza.

**Utilisateur :** (clique sur l’option de fromage supplémentaire avec la souris)

**Caractère :** Ajoutez des « fromages supplémentaires ».

Un autre facteur important dans la réussite de l’entrée vocale est cueing l’utilisateur lorsque le moteur est prêt pour l’entrée, car de nombreux moteurs de reconnaissance vocale n’autorisent qu’un seul énoncé à la fois. Microsoft agent prend en charge ce mode de deux manières. Tout d’abord, si la carte son prend en charge MIDI, Microsoft Agent génère un bref ton pour signaler quand le canal d’entrée vocale est disponible. Deuxièmement, la fenêtre info-bulle d’écoute affiche une invite de texte appropriée lorsque le caractère (moteur de reconnaissance vocale) est à l’écoute de l’entrée. En outre, ce Conseil affiche ce que le moteur a entendu.

 

 




