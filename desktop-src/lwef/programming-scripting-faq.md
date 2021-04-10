---
title: FAQ sur les scripts de programmation
description: FAQ sur les scripts de programmation
ms.assetid: 84078c5b-7b04-48fa-9d0a-d95393c323eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dec468eb5147968ca0db774f081212a78cf40d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028466"
---
# <a name="programming-scripting-faq"></a>FAQ sur les scripts de programmation

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

### <a name="when-i-use-microsoft-visual-basic-or-other-development-tools-for-scripting-microsoft-agent-i-do-not-see-all-the-properties-and-events-used-in-your-samples-how-do-i-access-them"></a>Lorsque j’utilise Microsoft Visual Basic (ou d’autres outils de développement) pour l’écriture de scripts Microsoft Agent, je ne vois pas toutes les propriétés et tous les événements utilisés dans vos exemples. Comment faire y accéder ?

La plupart des événements, méthodes et propriétés pris en charge par le contrôle Microsoft Agent sont exposés uniquement au moment de l’exécution. Pour plus d’informations, consultez [programmation du contrôle Microsoft Agent](programming-the-microsoft-agent-control.md) .

### <a name="the-map-tag-or-some-other-tag-doesnt-seem-to-work"></a>La balise Map (ou une autre balise) ne semble pas fonctionner.

Certaines balises incluent des chaînes entre guillemets. Pour certains langages de programmation, tels que Microsoft Visual Basic et Visual Basic Scripting Edition, vous devrez peut-être utiliser deux guillemets pour désigner le paramètre de la balise ou concaténer un guillemet double comme faisant partie de la chaîne. Ce dernier s’affiche dans cet exemple de Visual Basic :

Agent1. Characters ("génie"). Speak "Ceci est \\ Map =" + Chr (34) + "texte parlé" \_ + Chr (34) + "=" + Chr (34) + "texte de la bulle" + Chr (34) + " \\ ."

Pour la programmation C, C++ et Java, faites précéder les barres obliques inverses et les guillemets doubles par une barre oblique inverse. Par exemple :

BSTR bszSpeak = SysAllocString (L "il s’agit de \\ \\ Map = \\ " texte parlé \\ "= \\ " texte de bulle \\ " \\ \\ ");

pCharacter->Speak (bszSpeak,......);

> [!Note]  
> Microsoft Agent ne prend pas en charge toutes les balises spécifiées dans l’API Microsoft Speech. En outre, la prise en charge de certains paramètres peut dépendre du moteur de synthèse vocale installé. Pour plus d’informations, consultez [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

### <a name="i-dont-seem-to-get-requeststart-and-requestcomplete-events-in-my-script-or-program"></a>Je ne semble pas recevoir les événements RequestStart et RequestComplete dans mon script (ou programme).

Cela peut être dû à l’un des problèmes suivants :

-   Votre langage de programmation ne prend pas entièrement en charge les contrôles ActiveX. Consultez votre documentation pour vous assurer qu’il prend en charge l’interface ActiveX et les événements pour les objets ActiveX.
-   Sur une page Web avec script, l’installation ou le chargement d’un autre contrôle a échoué. Vérifiez que tous les autres contrôles sont installés et qu’ils se chargent correctement sans Microsoft Agent.
-   Sur une page Web avec des cadres, vous avez la `<OBJECT>` balise du contrôle Microsoft Agent sur une page et les événements scriptés sur une autre page. Les événements sont envoyés uniquement à la page qui héberge le contrôle.

### <a name="i-am-using-the-microsoft-agent-control-with-other-activex-controls-on-my-webpage-and-i-dont-seem-to-get-any-events"></a>J’utilise le contrôle Microsoft Agent avec d’autres contrôles ActiveX sur ma page Web et je ne semble pas recevoir d’événements.

Vérifiez que les autres contrôles sont correctement installés. Si un autre contrôle ActiveX ne parvient pas à s’inscrire correctement, le contrôle Microsoft Agent peut recevoir ses événements.

### <a name="what-programming-languages-can-i-use-to-program-the-microsoft-agent-control"></a>Quels langages de programmation puis-je utiliser pour programmer le contrôle Microsoft Agent ?

Microsoft Agent doit être pris en charge à partir de n’importe quel langage qui prend en charge l’interface ActiveX. Il comprend des exemples de code pour Visual Basic, VBScript, JScript, C/C++ et Java.

### <a name="can-i-access-the-parameters-returned-from-microsoft-agent-using-jscript"></a>Puis-je accéder aux paramètres retournés par Microsoft Agent à l’aide de JScript ?

Oui, mais actuellement, la seule façon de procéder consiste à utiliser la `<SCRIPT LANGUAGE="JScript" FOR="*object*" EVENT="event()">` syntaxe. Bien que cette syntaxe soit prise en charge pour Microsoft Internet Explorer, les autres navigateurs ne la prennent pas en charge. il est donc préférable d’éviter d’utiliser JScript pour cette partie du script de votre page.

### <a name="can-microsoft-agent-be-used-with-speech-recognition-or-speech-synthesis-text-to-speech-or-tts-engines-other-than-those-supplied-by-microsoft"></a>L’agent Microsoft peut-il être utilisé avec la reconnaissance vocale ou la synthèse vocale (conversion de texte par synthèse vocale) autres que celles fournies par Microsoft ?

Oui, à condition que le moteur prenne en charge les interfaces 4,0 de Microsoft Speech API (SAPI) requises par Microsoft Agent. Contactez le fournisseur du moteur. Pour obtenir des informations détaillées sur les interfaces SAPI requises par Microsoft Agent, consultez [spécifications de prise en charge du moteur de reconnaissance vocale](speech-engine-support-requirements.md).

### <a name="my-page-includes-html-object-tags-for-microsoft-agent-the-lernout--hauspie-truvoice-tts-engine-and-the-microsoft-command-and-control-speech-recognition-engine-but-not-all-the-components-install"></a>Ma page contient des balises d’objet HTML pour Microsoft Agent, le moteur TTS Lernout & Hauspie TruVoice et le moteur de reconnaissance vocale Microsoft Command and Control, mais pas l’ensemble des composants installés.

En règle générale, le problème peut être corrigé en actualisant la page. En règle générale, il est préférable de spécifier d’abord la balise de contrôle Microsoft Agent `<OBJECT>` , puis le moteur Lernout & Hauspie TruVoice, puis le moteur de reconnaissance vocale de commande et de contrôle.

### <a name="after-calling-the-moveto-method-my-character-seems-to-freeze-even-though-i-have-return-animations-assigned-to-moving-state-animations"></a>Après l’appel de la méthode MoveTo, mon caractère semble se figer même si j’ai retourné des animations affectées aux animations d’état de déplacement.

Quand vous jouez une animation, les services d’animation continuent à afficher sa dernière image jusqu’à ce qu’une autre animation soit appelée. Par conséquent, vous devez lire une autre animation après avoir appelé [**MoveTo**](moveto-method.md). Si vous avez défini une animation de **retour** pour l’animation de l’état **mobile** , le serveur la lira d’abord.

### <a name="when-i-query-the-characters-pitch-property-it-returns-a-value-of--1"></a>Lorsque j’interroge la propriété tonale du caractère, elle retourne la valeur-1.

Cela se produit si le caractère a été compilé à l’aide d’une propriété tonale par défaut du moteur de reconnaissance vocale. autrement dit, le pas n’a pas été modifié lors de la génération du caractère.

### <a name="when-my-code-attempts-to-set-the-tts-mode-id-for-a-text-to-speech-engine-i-get-the-following-error-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Quand mon code tente de définir l’ID de mode TTS pour un moteur de synthèse vocale, j’obtiens l’erreur suivante : un appel sortant ne peut pas être effectué car l’application distribue un appel synchrone en entrée.

Pour définir la propriété TTSModeID, Speech.dll doit être installé. Il s’agit généralement d’une partie du code d’installation du moteur de reconnaissance vocale. Vous pouvez également l’installer en installant le panneau de configuration de l’objet Speech, disponible à partir de la page de téléchargement de Microsoft Agent.

### <a name="when-i-retry-loading-a-character-that-failed-to-load-the-call-fails-with-a-character-already-loaded-error"></a>Lorsque je tente de charger un caractère dont le chargement a échoué, l’appel échoue avec une erreur « caractère déjà chargé ».

Le contrôle Microsoft Agent ne décharge pas un objet caractère (Libérez la référence) lorsque le chargement de son fichier de caractères associé échoue. Si vous souhaitez réessayer de charger le caractère, vous devez appeler explicitement [**Unload**](unload-method.md) avant d’appeler [**Load**](load-method.md) la deuxième fois. Si vous tentez cette opération à partir d’un script de page Web, vous devez également faire précéder l’appel de **déchargement** d’une instruction On Error Resume Next, sinon l’appel de **Unload** échouera également. (Notez que JScript n’a pas d’instruction On Error Resume Next.)

Toutefois, vous n’avez peut-être pas besoin d’inclure du code pour réessayer immédiatement de charger un caractère lorsque le chargement du fichier échoue. Microsoft Internet Explorer et le composant serveur Microsoft Agent essaient automatiquement de réessayer plusieurs fois. par conséquent, les chances de réussite de votre tentative de chargement sont distantes. Une meilleure stratégie consiste à attendre (définir un minuteur) quelques secondes avant de réessayer.

### <a name="how-can-i-install-microsoft-agent-as-part-of-my-application-or-from-my-web-server"></a>Comment installer Microsoft Agent dans le cadre de mon application ou de mon serveur Web ?

Vous pouvez installer l’agent à partir du site Web Microsoft en incluant son *CLSID dans une balise d’objet html*. Toutefois, si vous souhaitez inclure et installer l’agent à partir de votre propre programme d’installation d’application ou de votre propre serveur, vous devez télécharger le fichier cab d’installation automatique de Microsoft Agent en le téléchargeant à partir de la page téléchargements. Lors du téléchargement, choisissez l’option Enregistrer plutôt que exécuter du navigateur. Chaque fois que ce fichier est exécuté, il installe automatiquement Microsoft Agent sur l’ordinateur cible. Par conséquent, vous pouvez spécifier le fichier dans votre script d’installation.

N’essayez pas d’installer Microsoft Agent en copiant ses différents. Dll et tente de l’inscrire vous-même. Si vous tentez d’installer l’agent par un autre moyen, son fichier cab à installation automatique n’est pas pris en charge.

Le système cible doit également inclure des versions récentes de MSVCRT.DLL (Runtime VC + +), REGSVR32.EXE (outil d’inscription inclus avec Microsoft VC + +) et COM. La meilleure façon de s’assurer que les versions appropriées sont installées est d’exiger l’installation de Microsoft Internet Explorer 3,02 ou version ultérieure. Toutefois, vous pouvez également accorder une licence pour ces exigences d’exécution. (Pour obtenir la dernière version de COM, accédez à la mise à jour DCOM à partir du site Web Microsoft.)

Microsoft Agent 2,0 ne s’installe pas sur Microsoft Windows 2000, car cette version du système d’exploitation contient déjà agent.

### <a name="can-i-use-the-visual-basic-setup-wizard-to-install-microsoft-agent"></a>Puis-je utiliser l’Assistant Installation de Visual Basic pour installer l’agent Microsoft ?

Bien que vous puissiez créer votre propre programme d’installation à l’aide du code Visual Basic (VB), vous ne pouvez pas utiliser l’Assistant Installation de Visual Basic pour effectuer cette opération. Pour installer l’agent à partir de VB, vous pouvez utiliser la commande shell, en spécifiant le fichier cab d’installation automatique de Microsoft Agent.

### <a name="how-do-i-install-microsoft-agent-on-windows-2000"></a>Comment faire installer Microsoft Agent sur Windows 2000 ?

Microsoft Agent 2,0 ne s’installe pas sur Windows 2000, car il est déjà inclus dans le système d’exploitation.

### <a name="agentsvr-crashes-when-speak-is-called-with-a-wav-file"></a>AgentSvr se bloque quand Speak est appelé avec un fichier WAV.

Cela peut se produire lorsque le caractère utilise TTS pour la sortie parlée, puis change pour utiliser un fichier WAV. Le texte n’a pas été fourni dans le premier paramètre de la méthode Speak.

Pour éviter l’incident, incluez un espace dans le premier paramètre de la méthode Speak, même si vous n’avez pas de sortie de texte.

### <a name="even-though-i-have-already-installed-the-agent-language-component-dll-for-a-particular-language-i-still-got-an-error-that-the-component-is-missing-when-i-set-the-characters-language-to-that-language"></a>Même si j’ai déjà installé le composant de langage de l’agent (DLL) pour une langue particulière, j’obtiens toujours un message d’erreur indiquant que le composant est manquant lorsque je définis la langue du caractère sur cette langue.

Cela se produit généralement lorsque vous avez des applications de l’agent telles que Microsoft Office 2000 ouvertes quand vous installez le composant de langue de l’agent. Fermez toutes les applications et réessayez. Si le problème persiste, redémarrez l’ordinateur et vous devez être en mesure de définir l’ID de langue maintenant.

### <a name="when-i-use-the-ampersand--symbol-the-text-around-the-symbol-in-the-characters-word-balloons-is-truncated"></a>Lorsque j’utilise le symbole esperluette « & », le texte autour du symbole dans les bulles de mot du caractère est tronqué.

Il s’agit d’un problème connu. Vous pouvez contourner ce paramètre à l’aide de la balise map. Par exemple, pour afficher « A & B » dans la bulle de mot du caractère, utilisez « A \\ Map = » et « = » && « \\ B » dans l’instruction Speak.

### <a name="my-application-allows-users-to-change-the-default-character-and-when-they-do-the-program-crashes"></a>Mon application permet aux utilisateurs de modifier le caractère par défaut et, le cas échéant, le programme se bloque.

Il existe deux causes possibles :

Si vous modifiez l’ID de mode TTS du caractère par défaut, puis que vous autorisez l’utilisateur à modifier le caractère par défaut via ShowDefaultCharacterProperties, AgentSvr se bloquera.

Ce problème a été résolu dans les systèmes d’exploitation Windows 2000 et Windows XP. Pour éviter l’incident sur d’autres plateformes, vous ne devez pas autoriser l’utilisateur à modifier le caractère par défaut après avoir modifié l’ID de mode TTS du caractère par défaut, ou à ne pas utiliser le caractère par défaut dans votre application ou votre page Web.

Si votre application n’utilise pas de caractères d’agent fournis par Microsoft, assurez-vous que votre caractère personnalisé utilise une palette avec une palette complète de 256 couleurs. Pour plus d’informations, consultez le document conception de caractères pour Microsoft Agent.

### <a name="my-page-loads-the-agent-character-from-multiple-frames-with-ie-5-i-get-the-microsoft-agent-failed-to-load-error"></a>Ma page charge le caractère d’agent à partir de plusieurs frames. Avec IE 5, j’obtiens l’erreur Échec du chargement de Microsoft Agent.

Il s’agit d’un problème connu avec IE 5. Une modification a été apportée à la façon dont le navigateur gère un certain événement, ce qui entraîne le début de l’exécution du script HTML avant le démarrage de AgentSvr. Pour que votre page fonctionne avec toutes les versions du navigateur, vous devez ajouter cette ligne à votre script :

AgentControl. Connected = true

qui crée explicitement une connexion à AgentSvr. Notez que vous ne devez effectuer cette opération que si votre page charge l’agent à partir de plusieurs frames.

### <a name="when-my-application-tries-to-install-microsoft-agent-on-windows-2000-or-windows-xp-i-get-the-error-that-agent-is-not-compatible-with-windows-2000-or-windows-xp"></a>Quand mon application tente d’installer Microsoft Agent sur Windows 2000 (ou Windows XP), j’obtiens une erreur indiquant que l’agent n’est pas compatible avec Windows 2000 (ou Windows XP).

Une version précédente du fichier CAB du composant principal de l’agent MSAGENT.exe, lorsqu’elle est exécutée sur Windows 2000 (et Windows XP), elle bloque l’installation et affiche un message d’erreur incorrect indiquant que l’agent n’est pas compatible avec la version du système d’exploitation que vous exécutez. En fait, les composants principaux de Microsoft Agent 2,0 sont inclus dans le cadre de Windows 2000 (et Windows XP) et sont déjà installés par défaut par le biais de l’installation de Windows.

Dans cette version, la vérification est supprimée et le fichier d’installation n’affiche pas le message d’erreur ci-dessus sous Windows 2000 (ou Windows XP). Notez qu’il s’agit de la seule modification apportée au fichier d’installation et qu’il n’y a pas de modifications de code pour les composants de base de l’agent eux-mêmes. Par conséquent, vous n’êtes pas affecté par cette mise à jour si vous avez déjà installé l’agent 2,0, ou si votre site Web utilise une balise d’objet pour déclencher des téléchargements automatiques des composants principaux de l’agent à partir du magasin d’objets Microsoft.

Si vous incluez le fichier d’installation du composant principal de l’agent avec votre application, ou si vous publiez le fichier d’installation sur votre serveur, vous souhaiterez peut-être télécharger cette mise à jour. Pour ce faire, cliquez ici et sélectionnez l’option « Enregistrer ce programme sur le disque ». Vous devez disposer d’une licence de distribution d’agent valide et actuelle pour ces circonstances.

Vous pouvez également contourner ce problème en utilisant l’option silencieux lors de l’installation de la version précédente du fichier d’installation MSAGENT.exe. La commande d’interpréteur de commandes est :

**MSAGENT.exe/q : a**

Il en va de même pour les composants de langue de l’agent publiés à l’origine en octobre 1998. Une vérification empêchait l’installation des composants de langue arabe, français, allemand, hébreu, italien, japonais, coréen, chinois simplifié, espagnol et chinois traditionnel sous Windows 2000 (et Windows XP). Les versions plus récentes de ces fichiers d’installation, ainsi que les 19 autres langues ajoutées en mars 2000, ne contiennent pas cette vérification et s’installent correctement sur Windows 2000 (et Windows XP).

### <a name="my-customized-character-exhibits-some-unexpected-behavior-with-its-transparency-color-on-windows-2000-and-windows-xp"></a>Mon caractère personnalisé présente un comportement inattendu avec sa couleur de transparence sur Windows 2000 (et Windows XP).

Il s’agit d’un problème connu pour les caractères créés avec une palette de moins de 256 couleurs. Les problèmes liés à ces caractères incluent la couleur de transparence apparaissant dans l’arrière-plan, le texte de la bulle transparente, la bordure de l’info-bulle transparente ou l’arrière-plan transparent. Notez que ces caractères peuvent provoquer le blocage de vos applications lorsqu’elles sont chargées dans la boîte de dialogue Sélecteur de caractères de l’agent ou dans la Galerie de l’Assistant Microsoft Office. Vos caractères personnalisés doivent utiliser une palette complète avec 256 couleurs. Vous pouvez utiliser l’exemple de palette fourni pour les caractères de l’Assistant Office comme point de départ avec une palette de couleurs 256 complète.

### <a name="the-character-does-not-use-the-british-english-tts-engine-even-though-i-have-set-its-language-id-to-british-english-h0809"></a>Le caractère n’utilise pas le moteur TTS anglais de la British, même si j’ai défini son ID de langue sur anglais britannique &h0809.

Tout d’abord, assurez-vous que tous les composants nécessaires sont installés : les composants principaux de l’agent, les fichiers binaires du runtime SAPI et un moteur de synthèse vocale britannique conforme à SAPI4 comme le moteur TTS3000 britannique English, disponible en téléchargement sur la page des téléchargements de l’agent. Si votre personnage n’utilise toujours pas le moteur de synthèse vocale Britannique, il est probable que vous disposiez également d’un moteur de synthèse vocale en anglais américain. Dans la mesure où les États-Unis et l’anglais américain partagent la même langue principale (anglais) et l’anglais américain, l’anglais est la valeur par défaut, l’agent choisit le premier moteur de synthèse des États-Unis d’Amérique comme retourné par SAPI. Pour utiliser un moteur TTS anglais britannique, utilisez la propriété TTSModeID du caractère à la place. Par exemple, le TTSModeID pour la voix mâle TTS3000 britannique est {227A0E41-A92A-11d1-B17B-0020AFED142E}. Dans Microsoft Visual Basic vous pouvez utiliser ce moteur en définissant les TTSModeID de Merlin comme suit :

AgentControl. Characters ("Merlin"). TTSModeID = {227A0E41-A92A-11d1-B17B-0020AFED142E}

### <a name="when-the-characters-volume-is-set-to-zero-using-the-speech-tag-vol0-it-either-has-no-effects-or-crashes-the-agentsvr"></a>Lorsque le volume du caractère est défini sur zéro à l’aide de la balise Speech \\ vol = 0 \\ , il n’a aucun effet ou plante le agentsvr.

Il s’agit d’un problème connu. Sur les systèmes d’exploitation Windows 95, Windows 98 et Windows Me, le volume du caractère ne change pas, mais il reste au niveau défini précédemment. Sur les plateformes Windows NT 4,0, Windows 2000 et Windows XP, cela entraînera le blocage de AgentSvr, même si aucun moteur TTS n’est installé. Étant donné que la plage du volume du caractère, de 0 (silence) à 65535 (volume maximal), est importante et que la différence entre les niveaux successifs n’est pas facile à décerner, la solution de contournement simple consiste à définir le volume sur 1 au lieu de 0 lorsque vous souhaitez que la voix du caractère soit inaudible.

### <a name="my-customized-characters-return-animation-does-not-play-correctly-after-the-movedown-moveleft-moveright-andor-moveup-animations"></a>L’animation de retour de mon caractère personnalisé ne s’exécute pas correctement après les animations MoveDown, MoveLeft, MoveRight et/ou MoveUp.

Assurez-vous qu’une animation simple est assignée à l’état de conversation. Par exemple, vous pouvez utiliser un cadre unique constitué de la position neutre du caractère avec des superpositions de bouche.

 

 




