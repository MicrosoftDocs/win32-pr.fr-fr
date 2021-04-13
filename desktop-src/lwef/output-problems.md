---
title: Problèmes de sortie
description: Problèmes de sortie
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d909052feb2463637a8eab6343353f0af617c06
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314395"
---
# <a name="output-problems"></a>Problèmes de sortie

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>Le caractère laisse des images ou des traces en arrière-plan lorsqu’il se déplace.

Lorsqu’un caractère d’agent est animé, il requiert que les fenêtres d’application du caractère soient mises à jour en temps utile. Lorsque le caractère se déplace sur l’écran, il est normal que certaines images résiduelles disparaissent rapidement (en fonction de la vitesse de votre PC et des applications que vous exécutez). Si ce n’est pas le cas, la cause peut être la suivante :

-   Votre système ne répond pas à la configuration système minimale requise pour l’agent.
-   La fenêtre d’application derrière le caractère ne traite pas les mises à jour en temps opportun. Essayez de faire glisser le caractère sur le bureau ou une fenêtre de dossier, ou fermez certaines de vos applications. Si vous constatez une amélioration notable, le problème peut être inévitable.
-   La version officielle de Microsoft Internet Explorer 4,0 (ou version ultérieure) n’est peut-être pas installée. Les premières versions préliminaires d’Internet Explorer 4,0 n’ont pas géré correctement la mise à jour de l’écran. Cela entraînerait des images résiduelles du caractère restant sur l’écran. Pour résoudre le problème, installez la dernière version officielle d’Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Il peut y avoir un problème avec les pilotes d’écran ou le matériel de votre système. Assurez-vous que vous disposez des pilotes les plus récents pour votre matériel graphique. Si le problème persiste, vous souhaiterez peut-être contacter le fournisseur de votre PC.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>Le caractère ne produit pas de sortie audio lorsqu’il parle.

Ce symptôme peut avoir plusieurs causes. Essayez ce qui suit pour isoler le problème :

-   Vérifiez que vos haut-parleurs sont branchés et que votre carte son est compatible avec Windows. Il est judicieux de les tester avec une autre application saine pour confirmer que la sortie audio fonctionne correctement.
-   Vérifiez que l’application activée par agent ou la page Web prend en charge l’entrée vocale. Les exemples de pages ne prennent pas tous en charge l’entrée vocale. Appuyez sur la touche d’écoute et maintenez-la enfoncée (en général, il s’agit de la touche Arrêt défil, sauf si vous l’avez modifiée). Une fenêtre contextuelle doit apparaître sous le caractère. Le texte de l’info-bulle indique l’état d’écoute du caractère. Si aucun Conseil ne s’affiche, cela signifie que l’application ou la page Web ne prend pas en charge l’entrée vocale ou que vous n’avez pas de moteur vocal compatible. Si l’info-bulle apparaît et indique que le caractère est à l’écoute, parlez-en une des commandes vocales du caractère. Si vous ne savez pas quelles commandes vocales sont disponibles : relâchez la touche écouteur, cliquez avec le bouton droit sur le caractère, puis choisissez Ouvrir la fenêtre commandes vocales dans le menu contextuel. Si la commande n’apparaît pas, la prise en charge de la reconnaissance vocale n’est pas disponible pour l’application ou la page Web que vous utilisez. S’il n’apparaît pas, appuyez de nouveau sur la touche d’écoute et maintenez-la enfoncée. Si l’info-bulle d’écoute apparaît sous le caractère et indique que le caractère est à l’écoute, parlez-en une des commandes listées dans la fenêtre. Si le caractère ne répond pas, passez à l’étape suivante.
-   Vérifiez qu’aucune autre application n’utilise actuellement l’appareil de sortie audio.
-   Vérifiez que le caractère que vous utilisez a été configuré pour la sortie parlée. (Vous devrez peut-être vérifier auprès du site Web ou du fournisseur de l’application.)
-   Vérifier que les paramètres de l’agent Microsoft sont activés pour la sortie orale
-   Si le caractère utilise un moteur TTS (Text-to-Speech) pour produire une sortie orale, vérifiez que vous avez installé un moteur TTS compatible. Par exemple, lorsqu’il est installé en tant que composant additionnel Internet Explorer 4,0, seuls les composants principaux de Microsoft Agent sont installés. Les composants principaux n’incluent pas de moteur de conversion de texte par synthèse vocale. Sans ce moteur TTS (moteur compatible avec l’API Microsoft Speech), les exemples de caractères Microsoft Agent ne génèrent pas de sortie parlée.
-   Vérifiez que l’utilisation de MIDI par Microsoft Agent ne bloque pas le canal audio (voir la rubrique suivante, les applications qui jouent sur MIDI n’ont pas de sortie audio lorsque Microsoft Agent est en cours d’exécution).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Les applications qui jouent un MIDI n’ont pas de sortie audio lorsque Microsoft Agent est en cours d’exécution.

Microsoft Agent utilise MIDI pour émettre une tonalité quand vous appuyez sur la touche d’écoute. Si vous constatez que cela interfère avec d’autres applications qui jouent un MIDI ou interfère avec l’entrée vocale, vous pouvez désactiver l’option de lecture quand vous pouvez parler dans les propriétés de l’agent Microsoft.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>J’obtiens le message suivant : un appel sortant ne peut pas être effectué car l’application distribue un appel synchrone en entrée.

Ce message peut se produire dans les circonstances suivantes :

Quand une page Web incluant Microsoft Agent est fermée (en cliquant avec le bouton droit sur l’entrée de la barre des tâches et en choisissant fermer dans le menu contextuel), cela peut se produire. Cela est dû à un problème de synchronisation entre l’agent et le navigateur lorsqu’ils s’arrêtent en même temps. L’erreur est sans conséquence. Cliquez sur OK pour fermer le message.

La page Web (ou l’application) activée par agent a tenté de demander un moteur de synthèse vocale (TTS) spécifique. Speechapi.dll n’a pas été installé.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>Les moteurs de reconnaissance vocale ne semblent pas fonctionner avec Microsoft Agent dans Windows XP ?

Microsoft Agent utilise SAPI 4,0 pour fournir des services vocaux. Windows XP est désormais fourni avec SAPI 5,0 qui ne fournit pas de prise en charge de la compatibilité descendante pour son prédécesseur. Heureusement, SAPI 4,0 et SAPI 5,0 peuvent coexister ensemble sur le même ordinateur Windows XP.

Pour que les moteurs de reconnaissance vocale fonctionnent avec Microsoft Agent dans Windows XP, commencez par installer les [fichiers binaires SAPI 4,0 Runtime](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe), puis installez les moteurs de reconnaissance vocale en particulier.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Les moteurs de reconnaissance vocale utilisés pour fonctionner avec Microsoft Agent jusqu’à la mise à niveau vers Windows XP. Que s’est-il passé ?

Consultez la question et la réponse précédentes. Le processus de mise à niveau de Windows XP a peut-être supprimé la prise en charge de SAPI 4,0 déjà présente sur l’ordinateur. Réinstallez simplement les moteurs de reconnaissance vocale SAPI 4,0 Runtime et SAPI 4,0 après la mise à niveau vers Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>J’ai installé les moteurs de conversion de texte par synthèse vocale TTS3000 sur mon ordinateur qui exécute Windows XP (ou Windows 2000) et j’ai correctement modifié ma programmation en conséquence. Les caractères Microsoft Agent parlent de manière audible à l’aide de ces moteurs de synthèse vocale TTS3000 lorsque je ou d’autres administrateurs locaux sont connectés, mais pas lorsque d’autres utilisateurs *sans privilèges d’administrateur* sont connectés à cet ordinateur. Sur Windows 98 et Windows Me, ces moteurs de synthèse vocale TTS3000 fonctionnent correctement pour les deux ensembles d’utilisateurs. Comment puis-je résoudre ce problème ?

Vous devez configurer les autorisations de sécurité pour certaines des clés de registre des moteurs de synthèse vocale TTS3000 pour permettre leur utilisation par les comptes d’utilisateur sans privilèges d’administrateur. Pour ce faire, vous pouvez utiliser l’éditeur du Registre du système d’exploitation.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>J’ai suivi la procédure décrite comme solution au problème mentionné dans la question précédente. Cela fonctionnait correctement pour que les caractères Microsoft Agent puissent parler de manière audible à l’aide de ces moteurs de synthèse vocale TTS3000 quand *des utilisateurs sans privilèges d’administrateur* étaient connectés à l’ordinateur Windows XP (ou Windows 2000). Maintenant, les mois ultérieurs, ces mêmes TTS3000 les mêmes moteurs de synthèse vocale ont cessé de fonctionner. Que s’est-il passé ?

Lorsque vous avez suivi la procédure décrite pour la question précédente, les comptes d’utilisateur non-administrateurs disposant des autorisations contrôle total sur les clés de Registre requises ont été fournis. Il est possible que l’un de ces utilisateurs ait peut-être volontairement modifié les valeurs, a modifié les autorisations ou même supprimé entièrement la clé de registre.

Vérifiez si ces clés de Registre et leurs autorisations ont été modifiées, supprimées ou modifiées depuis. Si nécessaire, modifiez à nouveau ces clés de Registre et leurs autorisations, ou réinstallez la conversion de texte par synthèse vocale TTS3000.

 

 




