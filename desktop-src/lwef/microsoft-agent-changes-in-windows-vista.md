---
title: modifications de l’Agent Microsoft dans Windows Vista
description: modifications de l’Agent Microsoft dans Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b9b4e1104152bb21a2ed120d749d92907c1f6be6f2392c299db639cd483bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961199"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>modifications de l’Agent Microsoft dans Windows Vista

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Windows Vista introduit des modifications dans la façon dont la reconnaissance vocale et la reconnaissance vocale interagissent avec Windows Vista.

Microsoft agent prend désormais en charge les composants de reconnaissance vocale et de synthèse vocale SAPI 5. Les propriétés TTSModeID et SRModeID de l’objet agent sont toujours utilisées pour déterminer quelle voix ou reconnaissance est sélectionnée pour l’agent et pour modifier cette sélection. Les modes SAPI 4 apparaissent en tant que chaînes GUID telles que « {ca141fd0-ac7f-11D1-97a3-006008273000} », tandis que les jetons SAPI 5 (équivalents aux modes) s’affichent sous forme de noms standard, tels que « Microsoft Anna ». Comme dans les versions antérieures, l’agent fait un choix par défaut de moteurs TTS et de moteurs de reconnaissance vocale. Si vous installez des moteurs SAPI 5, ceux-ci sont toujours préférés sur les moteurs SAPI 4 qui peuvent être installés. Le moteur de synthèse vocale par défaut de l’utilisateur, tel que spécifié dans le panneau de configuration, est utilisé si son sexe correspond à celui du caractère, sinon un moteur SAPI 5 du même sexe est choisi, s’il est disponible. Les ID de mode spécifiés directement sur le caractère sont ignorés si les moteurs SAPI 5 sont présents. Les sélections par défaut peuvent être vérifiées en lisant les propriétés TTSModeID et SRModeID au début de votre script.

Comme précédemment, TTSModeID et SRModeID retournent une chaîne vide si la fonctionnalité de reconnaissance vocale ou de synthèse vocale n’est pas présente. Vous pouvez sélectionner une voix ou un module de reconnaissance spécifique en définissant ces propriétés sur la chaîne de mode SAPI 4 appropriée ou le nom de jeton SAPI 5. Après avoir défini un mode ou un jeton spécifique, vous pouvez également lire à nouveau la propriété pour vérifier que sa valeur a pris, ce qui indique que le nouveau mode ou jeton a été effectivement disponible et a été sélectionné avec succès. Pour les développeurs déployant l’agent sur le Web, Notez que de nombreux utilisateurs de Vista disposent déjà d’une ou de plusieurs voix SAPI 5, ce qui vous permet d’éviter de télécharger automatiquement les voix SAPI 4, à moins que votre script ne les demande spécifiquement, car la voix téléchargée n’est pas utilisée.

Les moteurs de reconnaissance vocale SAPI 5 utilisent un ensemble de normes différent de celui de SAPI 4 pour annoter la parole avec le balisage, par exemple pour modifier la tonalité ou le taux de parole. Dans SAPI 4, vous utilisez des commandes de « barre oblique », telles que/PIT = 170/. Dans SAPI 5, vous utilisez des balises XML, telles que \<PITCH MIDDLE="5"/> . Dans Vista, l’agent acceptera les deux types d’annotations dans les chaînes de méthode Speak. les commandes « slash » seront ignorées par les moteurs SAPI 5, et les balises XML seront ignorées par les moteurs SAPI 4. Comme avec les balises de barre oblique, la prise en charge des balises XML SAPI 5 varie d’un fournisseur à l’autre, et certains fournisseurs peuvent prendre en charge des balises supplémentaires. Pour plus d’informations sur les balises XML SAPI 5, consultez la spécification SAPI 5.

Agent n’intègre plus la prise en charge de plusieurs langues. La langue utilisée par l’agent est toujours supposée être la langue actuelle de l’utilisateur, telle qu’elle est inscrite auprès du système d’exploitation. La propriété LanguageID de l’objet agent est toujours accessible en écriture, mais sa valeur est ignorée par agent sur Vista. Par exemple, si la langue de l’utilisateur est anglais (États-Unis) (&H0409), et qu’il utilise un programme qui définit l’LanguageID sur français (&H040C), les boîtes de dialogue texte de l’info-bulle et options de caractères avancées s’affichent toujours en anglais.

 

 




