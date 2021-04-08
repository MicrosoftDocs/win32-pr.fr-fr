---
title: Comment AMSI vous protège contre les programmes malveillants
description: En tant que développeur d’applications, vous pouvez participer activement à la défense contre les programmes malveillants. Plus précisément, vous pouvez protéger vos clients contre les programmes malveillants basés sur des scripts dynamiques et à partir de voies non traditionnelles de cyberattaque.
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671633"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>Comment l’interface d’analyse anti-programme malveillant (AMSI) vous permet de vous défendre contre les programmes malveillants

Pour une introduction à l’interface de l’analyse anti-programme malveillant de Windows (AMSI), consultez [interface d’analyse anti-programme malveillant (AMSI)](antimalware-scan-interface-portal.md).

En tant que développeur d’applications, vous pouvez participer activement à la défense contre les programmes malveillants. Plus précisément, vous pouvez protéger vos clients contre les programmes malveillants basés sur des scripts dynamiques et à partir de voies non traditionnelles de cyberattaque.

Par exemple, supposons que votre application soit scriptable : elle accepte le script arbitraire et l’exécute via un moteur de script. À l’endroit où un script est prêt à être fourni au moteur de script, votre application peut appeler les API AMSI Windows pour demander une analyse du contenu. De cette façon, vous pouvez déterminer en toute sécurité si le script est malveillant avant de décider de l’exécuter.

Cela est vrai même si le script a été généré au moment de l’exécution. Le script (malveillant ou autre) peut passer par plusieurs passages de débrouillage. Mais vous devez finalement fournir le moteur de script avec du code brut et non masqué. C’est là que vous appelez les API AMSI.

Voici une illustration de l’architecture AMSI, où votre propre application est représentée par l’une des zones « autres applications ».

![architecture AMSI](images/AMSI7Archi.jpg)

L’interface Windows AMSI est ouverte. Ce qui signifie que toute application peut l’appeler ; et tout moteur anti-programme malveillant inscrit peut traiter le contenu qui lui est soumis.

Nous n’avons pas besoin de limiter la discussion aux moteurs de script. Par exemple, votre application est une application de communication et elle analyse les messages instantanés à la recherche de virus avant de les afficher à vos clients. Ou peut-être votre logiciel est un jeu qui valide les plug-ins avant de les installer. Il existe de nombreuses opportunités et scénarios pour l’utilisation de AMSI.

## <a name="amsi-in-action"></a>AMSI en action

Jetons un coup d’œil à AMSI en action. Dans cet exemple, Windows Defender est l’application qui appelle les API AMSI. Toutefois, vous pouvez appeler les mêmes API à partir de votre propre application.

Voici un exemple de script qui utilise la technique XOR-Encoding pour masquer son intention (que cette intention soit bénigne ou non). Pour cette illustration, nous pouvons imaginer que ce script a été téléchargé à partir d’Internet.

![exemple de script encodé en base64](images/AMSI8.png)

Pour rendre les choses plus intéressantes, nous pouvons entrer ce script manuellement sur la ligne de commande afin qu’il n’y ait pas de fichier réel à analyser. Cela reflète ce que l’on appelle une « menace de fichier ». Ce n’est pas aussi simple que d’analyser des fichiers sur disque. La menace peut être une porte dérobée qui réside uniquement dans la mémoire d’un ordinateur.

Ci-dessous, nous voyons le résultat de l’exécution du script dans Windows PowerShell. Vous verrez que Windows Defender est en mesure de détecter l’exemple de test AMSI dans ce scénario compliqué, simplement à l’aide de la signature d’exemple de test AMSI standard.

![Windows Defender-détection de l’exemple de test AMSI](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>Intégration de AMSI avec JavaScript/VBA

Le flux de travail illustré ci-dessous décrit le flux de bout en bout d’un autre exemple, dans lequel nous illustrerons l’intégration de AMSI avec l’exécution de macros dans Microsoft Office.

![Intégration de AMSI avec JavaScript/VBA](images/integ-js-vba.png)

- L’utilisateur reçoit un document contenant une macro (malveillante) qui échappe aux analyses logicielles antivirus statiques en employant des techniques telles que l’obscurcissement, les fichiers protégés par mot de passe ou autres.
- L’utilisateur ouvre ensuite le document contenant la macro (malveillante). Si le document s’ouvre en mode protégé, l’utilisateur clique sur **activer la modification** pour quitter le mode protégé.
- L’utilisateur clique sur **activer les macros** pour permettre l’exécution des macros.
- À mesure que la macro s’exécute, le runtime VBA utilise une mémoire tampon circulaire pour enregistrer \[ 1 \] données et paramètres liés aux appels aux API Win32, com et VBA.
- Lorsque des API Win32 ou COM spécifiques considérées comme étant à haut risque (également appelées *déclencheurs*) \[ 2 \] sont observées, l’exécution de la macro est interrompue et le contenu de la mémoire tampon circulaire est transmis à AMSI.
- Le fournisseur de services anti-programmes malveillants AMSI inscrit répond avec un verdict pour indiquer si le comportement de la macro est malveillant.
- Si le comportement est non malveillant, l’exécution de la macro se poursuit.
- Dans le cas contraire, si le comportement est malveillant, Microsoft Office ferme la session en réponse à l’alerte \[ 3 \] , et l’antivirus peut mettre le fichier en quarantaine.

## <a name="what-does-this-mean-for-you"></a>Qu’est-ce que cela signifie pour vous ?

Pour les utilisateurs de Windows, tout logiciel malveillant qui utilise des techniques d’obscurcissement et de fraude sur les hôtes de script intégrés de Windows 10 est automatiquement inspecté à un niveau plus approfondi que jamais, offrant ainsi des niveaux de protection supplémentaires.

Pour vous, en tant que développeur d’applications, vous devez faire appel à votre application pour appeler l’interface AMSI de Windows si vous souhaitez tirer parti de l’analyse et de l’analyse supplémentaires du contenu potentiellement malveillant.

En tant que fournisseur de logiciels antivirus, vous pouvez envisager d’implémenter la prise en charge de l’interface AMSI. Dans ce cas, votre moteur aura un aperçu plus approfondi des données que les applications (y compris les hôtes de script intégrés à Windows 10) sont potentiellement malveillantes.

## <a name="more-background-info-about-fileless-threats"></a>Plus d’informations générales sur les menaces de fichiers

Vous pouvez être curieux d’obtenir plus d’informations générales sur les types de menaces sans fichier que Windows AMSI est conçu pour vous aider à vous défendre contre. Dans cette section, nous allons jeter un coup d’œil au jeu de chat et de souris traditionnel qui s’exécute dans l’écosystème des logiciels malveillants.

Nous allons utiliser PowerShell comme exemple. Mais vous pouvez tirer parti des mêmes techniques et processus que nous allons démontrer avec les langages &mdash; VBScript, Perl, Python, Ruby et bien plus encore.

Voici un exemple de script PowerShell malveillant.

![exemple de script PowerShell malveillant](images/AMSI1.png)

Bien que ce script écrive simplement un message à l’écran, le programme malveillant est généralement plus être mal intentionné. Mais vous pouvez facilement écrire une signature pour détecter celle-ci. Par exemple, la signature peut rechercher la chaîne « Write-Host’pwnd ! ' » dans un fichier ouvert par l’utilisateur. Parfait : nous avons détecté nos premiers programmes malveillants !

Après avoir été détecté par notre première signature, les auteurs de programmes malveillants répondront. Ils répondent en créant des scripts dynamiques tels que cet exemple.

![exemple de script dynamique](images/AMSI2.png)

Dans ce scénario, les auteurs de programmes malveillants créent une chaîne représentant le script PowerShell à exécuter. Mais elles utilisent une technique simple de concaténation de chaînes pour rompre la signature précédente. Si vous affichez la source d’une page Web à charge Active Directory, vous verrez que de nombreuses instances de cette technique sont utilisées pour éviter les logiciels de blocage publicitaire.

Enfin, l’auteur du programme malveillant passe cette chaîne concaténée au `Invoke-Expression` mécanisme de l’applet de commande &mdash; PowerShell pour évaluer les scripts composés ou créés au moment de l’exécution.

En réponse, un logiciel anti-programme malveillant commence à effectuer une émulation de langage de base. Par exemple, si deux chaînes sont concaténées, nous émulons la concaténation de ces deux chaînes, puis nous exécutons nos signatures sur le résultat. Malheureusement, il s’agit d’une approche relativement délicate, car les langages ont tendance à avoir de nombreuses façons de représenter et de concaténer des chaînes.

Par conséquent, après avoir été intercepté par cette signature, les auteurs de programmes malveillants seront plus compliqués &mdash; par exemple, en encodant le contenu du script en base64, comme dans l’exemple suivant.

![exemple de contenu de script en base64](images/AMSI3.png)

En ingénieux, la plupart des moteurs anti-programme malveillant implémentent également l’émulation de décodage base64. Par conséquent, puisque nous implémentons également l’émulation de décodage base64, nous sommes anticipés pour une heure.

En réponse, les auteurs de programmes malveillants passent à l’obscurcissement algorithmique &mdash; comme un simple mécanisme d’encodage XOR dans les scripts qu’ils exécutent.

![exemple de script d’obscurcissement algorithmique](images/AMSI4.png)

À ce stade, nous avons généralement dépassé les moteurs antivirus qui seront émulés ou détectés. nous ne détectons donc pas nécessairement ce que ce script fait. Toutefois, nous pouvons commencer à écrire des signatures sur les techniques d’obscurcissement et d’encodage. En fait, c’est ce qui compte pour la grande majorité des signatures pour les programmes malveillants basés sur des scripts.

Mais que se passe-t-il si l’obscurcissement est tellement trivial qu’il ressemble à de nombreux scripts corrects ? Une signature pour cela générerait un nombre inacceptable de faux positifs. Voici un exemple de script *intermédiaire* trop Bénin pour la détection autonome.

![exemple de script intermédiaire trop Bénin pour la détection autonome](images/AMSI5.png)

Dans cet exemple, nous téléchargeons une page Web et appelons du contenu à partir de celle-ci. Voici l’équivalent dans Visual Basic Script.

![équivalent dans Visual Basic Script](images/AMSI6.png)

Ce qui complique ces deux exemples, c’est que le moteur antivirus inspecte les fichiers ouverts par l’utilisateur. Si le contenu malveillant se trouve uniquement dans la mémoire, l’attaque peut potentiellement passer inaperçue.

Cette section a montré les limitations de la détection à l’aide de signatures traditionnelles. Toutefois, si un script malveillant peut traverser plusieurs passages de débrouillage, il doit finalement fournir le moteur de script avec du code brut et non brouillé. Et à ce stade &mdash; , comme nous l’avons décrit dans la première section ci-dessus, &mdash; les hôtes de script intégrés de Windows 10 appellent les API AMSI pour demander une analyse de ce contenu non protégé. Et votre application peut faire la même chose.

## <a name="related-resources"></a>Ressources associées

* [Menaces de fichiers](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI : présentation du voile sur les macros malveillantes](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [Prêt à l’emploi, mais pas invisible : déchargement de logiciels malveillants sans fichier avec surveillance du comportement, AMSI et AV nouvelle génération](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
