---
title: Fournir une bonne récupération d’erreur
description: Fournir une bonne récupération d’erreur
ms.assetid: 48e00638-9274-49db-93ec-ed444f526441
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a20a3d203ab0fcd93a6f4645be4af44b049f3cd
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120794"
---
# <a name="provide-good-error-recovery"></a>Fournir une bonne récupération d’erreur

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Comme avec toute interface bien conçue, le processus interactif devrait réduire les circonstances qui provoquent des erreurs. Toutefois, il est rarement possible d’éliminer toutes les erreurs. par conséquent, la prise en charge d’une bonne récupération d’erreur est essentielle pour maintenir la confiance et l’intérêt de l’utilisateur. En général, la récupération des erreurs implique la détection d’une erreur, la détermination de la cause et la définition d’un moyen de résoudre l’erreur. Les utilisateurs répondent mieux aux interfaces coopératives, qui collaborent avec l’utilisateur pour accomplir une tâche.

La première étape de la récupération d’erreur vocale est la détection de la condition d’échec. La reconnaissance vocale peut échouer en raison de diverses erreurs. Les conditions d’erreur peuvent généralement être détectées en raison d’une entrée non valide, d’une correction ou d’une annulation explicites de l’utilisateur ou d’une répétition par l’utilisateur.

Une *erreur de rejet* se produit lorsque le moteur de reconnaissance n’a pas de correspondance pour ce que l’utilisateur a dit. Le bruit de fond ou les démarrages précoces sont également des causes courantes de l’échec de la reconnaissance. par conséquent, demander à l’utilisateur de répéter une commande est souvent une bonne solution initiale. Toutefois, si l’expression est en dehors de la grammaire active actuelle, le fait de demander à l’utilisateur de reformuler la demande peut résoudre le problème. La différence dans le libellé peut aboutir à une correspondance avec un objet dans la grammaire actuelle. Une autre solution consiste à répertorier ou suggérer des options d’entrée appropriées.

Une bonne stratégie pour la récupération des erreurs de rejet consiste à combiner ces techniques pour remettre l’utilisateur en route, offrant ainsi une assistance de plus en plus si l’échec persiste. Par exemple, vous pouvez commencer par répondre à l’échec initial avec une interrogation de type « non ? ». ou « quoi ? » ou un geste de la main à l’oreille. Une réponse brève augmente la probabilité que l’instruction répétée de l’utilisateur n’échoue pas parce que l’utilisateur a fait un spoke trop tôt. En cas de défaillance répétée, la demande de nouvelle phrase suivante améliore le risque de faire correspondre un résultat dans la grammaire donnée. À partir de là, fournir des invites explicites de commandes acceptées augmente davantage la probabilité d’une correspondance. Cette technique est illustrée dans l’exemple suivant :

**Utilisateur**: J’aimerais une pizza de type Chicago avec anchovies.

**Caractère**: (main à oreille) non ?

**Utilisateur**: Je souhaite une pizza à Chicago avec anchovies.

**Caractère**: (en-tête) Veuillez reformuler votre demande.

**Utilisateur**: J’ai dit Chicago pizza, avec anchovies.

**Caractère**: (ignorer) je suis désolé. Dites-moi le style de la pizza que vous souhaitez.

**Utilisateur**: Chicago, avec anchovies.

**Caractère**: toujours pas de chance. Voici ce que vous pouvez prononcer : « Chicago », « Hawaii » ou « combo ».

Pour que la gestion des erreurs semble plus naturelle, veillez à fournir un degré de variation aléatoire lors de la réponse aux erreurs. En outre, une réaction de l’utilisateur naturel à toute demande de répétition d’une réponse consiste à faire croître ou augmenter le volume lors de la répétition de l’instruction. Il peut être utile de rappeler occasionnellement à l’utilisateur qu’il doit parler de manière normale et claire, étant donné que l’effet de la surcharge ou l’augmentation du volume peut compliquer la reconnaissance des mots par le moteur de reconnaissance vocale.

L’assistance progressive doit faire plus que mettre l’erreur à l’attention de l’utilisateur ; il doit guider l’utilisateur dans la grammaire actuelle en fournissant successivement des messages plus informatifs. Les interfaces qui semblent essayer de comprendre un degré élevé de satisfaction et de tolérance de l’utilisateur.

Les *Erreurs de substitution*, où le moteur de reconnaissance vocale reconnaît l’entrée, mais qui correspond à la mauvaise commande, sont plus difficiles à résoudre, car le moteur de reconnaissance vocale détecte une énoncé correspondante. Une incompatibilité peut également se produire lorsque le moteur de reconnaissance vocale interprète les sons superflus comme des entrées valides (également appelées *erreur d’insertion*). Dans ces situations, l’aide de l’utilisateur est nécessaire pour identifier la condition d’erreur. Pour ce faire, vous pouvez répéter ce que le moteur de reconnaissance vocale a renvoyé et demander à l’utilisateur de le confirmer avant de continuer :

**Utilisateur**: J’aimerais une pizza de type Chicago.

**Caractère**: Saviez-vous que vous aimeriez une « pizza de type Chicago » ?

**Utilisateur**: Oui.

**Caractère**: Quels autres ingrédients souhaitez-vous en obtenir ?

**Utilisateur**: anchovies.

**Caractère**: avez-vous dit « anchovies » ?

**Utilisateur**: Oui.

Toutefois, l’utilisation de cette technique pour chaque énoncé devient inefficace et pénible. Pour gérer cela, limitez la confirmation aux situations qui ont des conséquences négatives significatives ou augmentent la complexité de la tâche immédiate. S’il est facile pour l’utilisateur d’effectuer ou d’inverser des modifications, vous pouvez éviter de demander la confirmation de ses choix. De même, si vous faites des choix visibles, vous n’aurez peut-être pas besoin de fournir une correction explicite. Par exemple, le choix d’un élément dans une liste peut ne pas nécessiter de vérification, car l’utilisateur peut voir les résultats et les modifier facilement. Vous pouvez également utiliser des scores de confiance et alternatifs pour fournir un seuil de confirmation. Vous pouvez ajuster le seuil en conservant un historique des actions de l’utilisateur dans une situation donnée et en éliminant la vérification basée sur une confirmation de l’utilisateur cohérente. Enfin, prenez en compte la nature multimodale de l’interface. La confirmation à partir de la souris ou du clavier est également appropriée.

Choisissez soigneusement le libellé des confirmations. Par exemple, « avez-vous dit... ? » ou « je pense que vous avez dit... » sont meilleures que « voulez-vous vraiment vouloir... ? » étant donné que les expressions précédentes impliquent que l’exactitude de l’écoute du caractère (reconnaissance) est interrogée, et non que l’utilisateur n’a peut-être pas parlé.

Tenez également compte de la grammaire d’une réponse. Par exemple, une réponse négative est susceptible de générer une erreur de rejet, nécessitant une invite supplémentaire, comme illustré dans l’exemple suivant :

**Utilisateur**: J’aimerais certains pepperoni.

**Caractère**: avez-vous dit « no Ham » ?

**Utilisateur**: non, j’ai dit pepperoni.

**Caractère**: non ?

**Utilisateur**: pepperoni.

La modification de la grammaire pour inclure des préfixes pour gérer les variations de réponse naturelle augmente l’efficacité du processus de récupération, en particulier lorsque l’utilisateur ne confirme pas l’invite de vérification. Dans cet exemple, la confirmation peut avoir été traitée en une seule étape en modifiant la grammaire de la « pepperoni » en incluant également « no I dit pepperoni », « j’ai dit pepperoni » et « no pepperoni ».

Vous pouvez également gérer les erreurs de substitution à l’aide des autres correspondances renvoyées par le moteur de reconnaissance vocale en tant que confirmation corrective :

**Utilisateur**: J’aimerais certains pepperoni.

**Caractère**: (Ecoute « no Ham » comme meilleure correspondance, « pepperoni » comme première alternative) avez-vous dit « no Ham » ?

**Utilisateur**: non, pepperoni.

**Caractère**: (continue d’entendre « aucun Ham » comme meilleure correspondance, mais offre maintenant la première alternative) « pepperoni » ?

De même, vous pouvez conserver un historique des erreurs de substitution courantes et, si une erreur particulière est fréquente, offrir l’alternative la première fois.

Dans toutes les situations d’erreur de reconnaissance, évitez blâmer l’utilisateur. Si le caractère suggère ou même implique que l’utilisateur est responsable de la responsabilité ou que le caractère semble indifférent de l’erreur, l’utilisateur peut devenir fautif. Ici également, choisissez soigneusement le libellé qui accepte explicitement la responsabilité, est approprié à la situation et utilise la variété pour créer une réponse plus naturelle. Lors de l’expression d’une excuses, évitez les mots ambigus comme « Désolé » ou « Désolé-Oh » qui pourraient être interprétés comme blâmer l’utilisateur. Utilisez plutôt des expressions telles que « je suis désolée » ou « ma faute ». Des erreurs répétitives ou répétées peuvent utiliser des excuses plus élaborées comme « je suis vraiment désolé ». Prenez également en compte la personnalité du caractère lorsque vous déterminez le type de réponse. Une autre option consiste à être responsable d’une situation externe. Des commentaires tels que « garçon », c’est qu’ils sont bruyants, «prenez la responsabilité de l’utilisateur et du personnage. Le rappel de l’utilisateur de la nature coopérative de l’interaction peut également être utile : pensez à des expressions telles que, « voyons ce que nous pouvons faire pour faire ce travail. »

Microsoft agent prend également en charge des commentaires automatiques pour la reconnaissance. Lorsqu’un énoncé est détecté, le Conseil d’écoute affiche le texte vocal de la meilleure correspondance. Vous pouvez définir votre propre texte pour qu’il s’affiche en fonction du paramètre de confiance d’une commande que vous définissez.

En raison du potentiel d’erreur, exige toujours une confirmation pour les choix qui ont des conséquences négatives graves et qui sont irréversibles. Naturellement, vous souhaiterez demander confirmation lorsque les résultats d’une action pourraient être destructifs. Toutefois, pensez également à exiger une confirmation pour les situations qui abandonnent un processus ou une opération de longue durée.

 

 




