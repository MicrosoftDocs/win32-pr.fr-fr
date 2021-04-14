---
title: Autres moteurs de reconnaissance vocale compatibles avec Microsoft Agent
description: Autres moteurs de reconnaissance vocale compatibles avec Microsoft Agent
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381599"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a>Autres moteurs de reconnaissance vocale compatibles avec Microsoft Agent

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Outre les moteurs de reconnaissance vocale Microsoft fournis avec et prenant en charge Microsoft Agent, un certain nombre d’entreprises proposent également des moteurs de reconnaissance vocale avec prise en charge de Microsoft Agent. Cette page vous donne une vue d’ensemble de ces moteurs qui peuvent être disponibles en anglais (États-Unis) et dans d’autres langues. Vous trouverez des informations sur l’installation et l’accès, ainsi que la licence et la redistribution des moteurs sur leurs sites Web.

Lorsque vous utilisez un moteur de reconnaissance vocale tiers, vous devez également installer Microsoft SAPI 4.0 en tant que fichiers binaires d’exécution afin que les moteurs soient correctement énumérés. À partir de votre page Web, vous pouvez inclure la balise suivante pour déclencher un téléchargement à partir de l’API Speech :

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Pour plus d’informations sur les fichiers binaires du runtime SAPI, reportez-vous au [site Web du groupe Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx). Microsoft Agent installe également les fichiers binaires du runtime SAPI avec le moteur de reconnaissance vocale Microsoft, le panneau de configuration vocal et l’éditeur de caractères de l’agent.

Veuillez noter que ces liens pointent vers des serveurs qui ne sont pas sous Microsoft Control. Veuillez lire la [déclaration officielle](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) Microsoft concernant les autres serveurs. Microsoft n’approuve pas le contenu ni les logiciels fournis sur ces sites Web. Toutes les questions techniques et de support doivent également être adressées aux fournisseurs des moteurs et non à Microsoft ou à l’équipe Microsoft Agent.

**Digalo moteur de synthèse vocale**

Digalo est un moteur TTS abordable conçu pour les utilisateurs finaux et les développeurs. Le moteur est proposé dans un certain nombre de langages : français, allemand, portugais (Brésil), espagnol, russe et anglais des États-Unis, avec l’italien, le polonais et d’autres langues disponibles prochainement. Des informations sur les développeurs, ainsi que des détails sur l’inscription des utilisateurs finaux et les programmes d’affiliation, sont également disponibles.

**Moteur de reconnaissance réseau ELAN**

Le moteur de reconnaissance vocale Elan utilise la technologie de conversion de texte par synthèse vocale du réseau ELAN et est disponible en sept langues : français, allemand, portugais (Brésil), espagnol, russe, Royaume-Uni et anglais des États-Unis.

**IBM ViaVoice-haute**

IBM a développé plusieurs caractères Microsoft Agent pour une utilisation avec ViaVoice-bruyant. IBM ViaVoice-bruyant est une technologie de synthèse vocale et est disponible en français, allemand, italien, espagnol, anglais du Royaume-Uni et anglais des États-Unis. Lorsqu’il est associé à Microsoft Agent, vous pouvez créer des applications vivantes dans de nombreuses langues et étendre vos opportunités commerciales à de nouveaux marchés internationaux.

 

 




