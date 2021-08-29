---
title: Bonnes pratiques de sécurité dans le développement de jeux
description: Cet article décrit les meilleures pratiques à utiliser dans le développement de jeux.
ms.assetid: 20956529-42ed-722b-cfa3-e3230d89fdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4890030dc66277b3b4e4e63861a23fdc2776a357c2054b183041e2dd8cb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051199"
---
# <a name="best-security-practices-in-game-development"></a>Bonnes pratiques de sécurité dans le développement de jeux

Cet article décrit les meilleures pratiques à utiliser dans le développement de jeux.

-   [Introduction](#introduction)
-   [Exemples de code non sécurisé](#examples-of-insecure-code)
-   [Méthodes d’amélioration de la sécurité](#ways-to-improve-security)
-   [Résumé](#summary)

## <a name="introduction"></a>Introduction

Un nombre grandissant de personnes jouent en ligne des jeux et des jeux avec un contenu créé par l’utilisateur. ceci, combiné à la sécurité accrue du système d’exploitation Microsoft Windows, signifie que les jeux sont une cible croissante et plus tentante pour les attaquants. Les développeurs de jeux doivent insister sur le fait que les jeux qu’ils publient ne créent pas de nouvelles brèches de sécurité pour que les attaquants puissent les exploiter. Les développeurs de jeux ont une responsabilité et un intérêt pour empêcher les ordinateurs de leurs clients d’être piratés par des données de réseau malveillantes, des modifications de l’utilisateur ou des falsifications. Si une vulnérabilité est exploitée, cela peut entraîner la perte de clients et/ou d’argent. Cet article présente et explique quelques méthodes et outils courants pour améliorer la sécurité du code sans dépasser le temps de développement.

Les trois erreurs les plus courantes faites par une équipe de développement lors de la publication d’un produit sont les suivantes :

-   Nécessite des privilèges d’administrateur. Les jeux ne doivent pas nécessiter de privilèges d’administrateur. Pour plus d’informations, consultez [contrôle de compte d’utilisateur pour les développeurs de jeux](./user-account-control-for-game-developers.md).
-   N’utilise pas la protection automatisée. Les développeurs n’utilisent généralement pas **/GS**, **/SAFESEH** ou **/NX**. L’utilisation de ces indicateurs de compilation/liaison peut détecter de nombreuses failles de sécurité de base sans augmenter considérablement la charge de travail. Ces indicateurs sont décrits plus loin dans cet article.
-   Utilisation d’API interdits. Il existe de nombreuses API (**strcpy**, **strncpy**, etc.) qui sont sujettes aux erreurs des programmeurs et qui génèrent facilement des failles de sécurité. Les développeurs doivent remplacer ces API par les versions sécurisées. Visual Studio 2005 est fourni avec un outil d’analyse des fichiers binaires qui peut vérifier automatiquement les fichiers objets pour les références à des api non sécurisées. pour plus d’informations sur la procédure à suivre avec les informations générées avec cet outil, consultez [repousser les attaques sur votre Code avec les bibliothèques Visual Studio 2005 Coffre C et C++](/archive/msdn-magazine/2005/may/repel-attacks-with-visual-studio-2005-safe-c-and-c-libraries) de Martyn Lovell. En outre, vous pouvez obtenir le fichier d’en-tête [interdit. h](https://www.microsoft.com/downloads/details.aspx?FamilyID=6aed14bd-4766-4d9d-9ee2-fa86aad1e3c9) qui peut vous aider à supprimer du code les fonctions interdites.

Chacune des erreurs figurant dans la liste est non seulement courante, mais peut facilement être corrigée sans modification significative de la charge de travail de développement, des normes de codage ou des fonctionnalités.

## <a name="examples-of-insecure-code"></a>Exemples de code non sécurisé

Voici un exemple simple de tout ce qu’il faut pour permettre à une personne malveillante d’effectuer une attaque de dépassement de mémoire tampon :


```
void GetPlayerName(char *pDatafromNet)
{
    char playername[256]; 
    strncpy(playername, pDatafromNet, strlen(pDatafromNet));

    // ...
}
```



Sur la surface, ce code semble OK : il appelle une fonction sécurisée, après tout. Les données du réseau sont copiées dans une mémoire tampon de 256 octets. La fonction **strncpy** s’appuie sur la recherche d’une marque de fin null dans la chaîne source ou est limitée par le nombre de mémoires tampons fourni. Le problème est que la taille de la mémoire tampon est incorrecte. Si les données du réseau ne sont pas validées ou si la taille de la mémoire tampon est incorrecte (comme dans cet exemple), une personne malveillante peut simplement fournir une mémoire tampon importante pour remplacer les données de la pile, après la fin de la mémoire tampon, avec toutes les données du paquet réseau. Cela permet à l’attaquant d’exécuter du code arbitraire en remplaçant le pointeur d’instruction et en modifiant l’adresse de retour. La leçon la plus simple de cet exemple consiste à ne jamais faire confiance à l’entrée jusqu’à ce qu’elle ait été vérifiée.

Même si les données ne proviennent pas à l’origine du réseau, il existe toujours un risque potentiel. Le développement moderne de jeux nécessite de nombreuses personnes pour la conception, le développement et le test de la même base de code. Il n’existe aucun moyen de savoir comment la fonction sera appelée à l’avenir. Toujours vous demander où proviennent les données et ce qu’une personne malveillante peut contrôler ? Bien que les attaques basées sur le réseau soient les plus courantes, ce ne sont pas les seules méthodes pour créer des failles de sécurité. Une personne malveillante peut-elle créer un mod ou modifier un fichier enregistré d’une manière qui ouvre une brèche de sécurité ? Qu’en est-il des fichiers image et audio fournis par l’utilisateur ? Des versions malveillantes de ces fichiers peuvent être publiées sur Internet et créer des risques de sécurité dangereux pour vos clients.

en guise de note, utilisez strsafe. h ou Coffre CRT au lieu de **strncpy** pour corriger l’exemple. Coffre CRT est une révision de sécurité complète du Runtime C et est fourni avec une partie de Visual Studio 2005. vous trouverez plus d’informations sur Coffre CRT dans [améliorations de la sécurité dans le crt](https://msdn.microsoft.com/library/8ef0s5kh(VS.80).aspx) par Michael Howard.

## <a name="ways-to-improve-security"></a>Méthodes d’amélioration de la sécurité

Il existe plusieurs façons d’améliorer la sécurité dans le cycle de développement. Voici quelques-unes des meilleures façons :

<dl> <dt>

<span id="Reading_about_security"></span><span id="reading_about_security"></span><span id="READING_ABOUT_SECURITY"></span>En savoir plus sur la sécurité
</dt> <dd>

Le livre, *Writing Secure Code, Second Edition* de Michael Howard et David LeBlanc, fournit une explication détaillée et claire des stratégies et méthodes permettant d’empêcher les attaques et d’atténuer les attaques. En commençant par les méthodes de conception de la sécurité dans une version pour les techniques de sécurisation des applications réseau, le livre couvre tous les aspects dont un développeur de jeux a besoin pour se protéger, ses produits et ses clients contre les attaquants. Le livre peut être utilisé pour mission une culture de sécurité dans un studio de développement. Ne vous contentez pas de considérer la sécurité du code comme un problème de développeur ou un problème de testeur. Considérer la sécurité comme toute l’équipe, du responsable de programme au concepteur et au développeur, doit réfléchir au moment où elle travaille sur un projet. Plus les yeux font partie du processus de révision, plus le risque d’interception d’une brèche de sécurité avant la version est élevé.

l' *écriture de Code sécurisé, la deuxième édition* est disponible auprès de [Microsoft Learning](https://www.microsoftpressstore.com/store/writing-secure-code-9780735617223) et d’autres informations générales sur la sécurité sont disponibles dans la lutte [contre les attaques futures en réduisant la Surface d’attaque](/previous-versions/ms972812(v=msdn.10)) de Michael Howard.

Michael Howard, David LeBlanc et John Viega ont écrit un autre ouvrage sur le sujet qui couvre tous les systèmes d’exploitation et langages de programmation courants, *19 mortelle Sins de la sécurité logicielle*.

Des présentations de sécurité axées sur les jeux sont disponibles sur la page de téléchargement des [présentations Microsoft XNA Developer](/previous-versions/dn629515(v=msdn.10)) .

</dd> <dt>

<span id="Threat_Modeling_Analysis"></span><span id="threat_modeling_analysis"></span><span id="THREAT_MODELING_ANALYSIS"></span>Analyse de modélisation des menaces
</dt> <dd>

Une analyse de modélisation des menaces est un bon moyen d’évaluer la sécurité du système, non dans une langue spécifique ou à l’aide d’un outil, mais dans une méthode de bout en bout étendue qui peut être accomplie en quelques réunions. En cas d’implémentation correcte, un modèle de thread peut identifier toutes les forces et les faiblesses d’un système, sans ajouter une charge de travail ou un temps de réunion significatif au projet. La méthode de modélisation des menaces insiste également sur l’idée d’évaluer la sécurité du système avant et Pendant le processus de développement afin de garantir qu’une évaluation complète est effectuée tout en se concentrant sur les fonctionnalités les plus risquées. Il peut être considéré comme un profileur pour la sécurité. En ne se basant pas sur un langage particulier ou sur un outil spécifique, la modélisation des menaces peut être utilisée dans n’importe quel projet de développement qui fonctionne sur n’importe quel projet dans n’importe quel genre. La modélisation des menaces est également une excellente méthode pour renforcer l’idée que la sécurité est la responsabilité de tout le monde et qu’il ne s’agit pas d’un problème de quelqu’un d’autre.

Lors de la modélisation des menaces, portez une attention particulière à :

-   Sources de données UDP
-   Sources de données qui ne requièrent pas d’authentification
-   Sources de données fréquemment et normalement interrogées dans le cadre d’une collecte d’informations à grande échelle
-   Toute capacité d’un client à envoyer directement des données à d’autres clients

Il s’agit des zones qui présentent de bons risques pour les faiblesses de sécurité.

Pour plus d’informations sur la modélisation des menaces, consultez [modélisation des menaces](https://technet.microsoft.com/security/) dans le centre de développement de la sécurité MSDN et dans le livre [Threat Modeling](https://www.amazon.com/Threat-Modeling-Microsoft-Professional-Swiderski/dp/0735619913) de Frank Swiderski et Window Snyder.

</dd> <dt>

<span id="Data_Execution_Prevention___NX_"></span><span id="data_execution_prevention___nx_"></span><span id="DATA_EXECUTION_PREVENTION___NX_"></span>Prévention de l’exécution des données (/NX)
</dt> <dd>

La prévention de l’exécution des données (DEP) est un outil récent pour atténuer les attaques multiples. si vous incluez le commutateur **/NX** dans la commande de génération, Visual Studio marquera les pages de mémoire avec des indicateurs qui indiquent si le code a le droit de s’exécuter ou non. Tout programme tentant de s’exécuter dans une page de mémoire non marquée avec l’autorisation EXECUTe entraîne l’arrêt forcé du programme. La prévention est appliquée au niveau du processeur et aura un impact sur les développeurs qui utilisent du code à modification automatique ou des compilateurs de langage JIT natifs. Actuellement, seuls les processeurs AMD Athlon64 et Opteron et Intel Itanium et les derniers processeurs Pentium 4 prennent en charge la prévention de l’exécution, mais il est prévu que tous les processeurs 32 bits et 64 bits prennent en charge la prévention de l’exécution à l’avenir. (Un schéma de protection contre la copie utilisé par un développeur peut être affecté par la prévention de l’exécution, mais Microsoft travaille avec des fournisseurs de protection contre la copie pour réduire l’impact.) Il est recommandé d’utiliser DEP.

Pour plus d’informations sur DEP, consultez [prévention de l’exécution des données](../memory/data-execution-prevention.md).

</dd> <dt>

<span id="Buffer_Security_Check___GS__and_Image_has_Safe_Exception_Handlers___SAFESEH_"></span><span id="buffer_security_check___gs__and_image_has_safe_exception_handlers___safeseh_"></span><span id="BUFFER_SECURITY_CHECK___GS__AND_IMAGE_HAS_SAFE_EXCEPTION_HANDLERS___SAFESEH_"></span>le contrôle de sécurité de la mémoire tampon (/gs) et l’Image ont Coffre gestionnaires d’exceptions (/safeseh)
</dt> <dd>

la vérification de la sécurité de la *mémoire tampon*, spécifiée par l’indicateur de compilateur **/gs**, et l' *Image a Coffre gestionnaires d’exceptions*, spécifiés par l’indicateur de l’éditeur de liens **/safeseh** (d’abord implémenté dans Visual Studio .net 2003), peut faciliter le travail du développeur en sécurisant le code.

L’utilisation de l’indicateur **/GS** fait en sorte que le compilateur crée une vérification de certaines formes de dépassements de mémoire tampon basés sur la pile qui pourraient être exploitées pour remplacer l’adresse de retour d’une fonction. L’utilisation de **/GS** ne détecte pas chaque dépassement de mémoire tampon possible et ne doit pas être considérée comme un tout, mais constitue une bonne technologie de défense en profondeur.

L’utilisation de l’indicateur **/SAFESEH** indique à l’éditeur de liens de générer uniquement un exécutable ou une dll s’il peut également générer une table des gestionnaires d’exceptions sécurisés de l’exécutable ou de la dll. Coffre La gestion structurée des exceptions élimine la gestion des exceptions comme une cible d’attaques de dépassement de mémoire tampon en garantissant que, avant qu’une exception soit distribuée, le gestionnaire d’exceptions est inscrit dans la table de fonctions située dans le fichier image. ces avantages de protection sont activés avec Windows XP SP2, Windows Server 2003, Windows Vista et Windows 7. De même, pour que **/SAFESEH** fonctionne correctement, il doit être utilisé dans une méthode « tout ou rien ». Toutes les bibliothèques contenant du code lié à un fichier exécutable ou une DLL doivent être compilées avec **/SAFESEH** ou la table ne sera pas générée.

pour plus d’informations sur le contrôle de sécurité de la [mémoire tampon](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) (**/gs**) et l' [Image, Coffre les gestionnaires d’exceptions](https://msdn.microsoft.com/library/9a89h429(vs.71).aspx) (**/safeseh**) se trouvent dans MSDN.

pour plus d’informations sur l’indicateur [ **/SDL**](/cpp/build/reference/sdl-enable-additional-security-checks?view=vs-2019) d’Microsoft Visual Studio 2012 et [les améliorations apportées à l’indicateur **/gs** dans](https://www.microsoft.com/security/blog/2012/01/26/enhancements-to-gs-in-visual-studio-11/)Visual Studio 2012, consultez.

</dd> <dt>

<span id="PREfast"></span><span id="prefast"></span><span id="PREFAST"></span>PREfast
</dt> <dd>

PREfast est un outil gratuit proposé par Microsoft qui analyse les chemins d’exécution dans le langage C ou C++ compilé pour faciliter la recherche des bogues au moment de l’exécution. PREfast fonctionne en utilisant tous les chemins d’exécution dans toutes les fonctions et en évaluant chaque chemin d’accès pour résoudre les problèmes. Utilisé à l’origine pour développer des pilotes et d’autres codes de noyau, cet outil peut aider les développeurs de jeux à gagner du temps en éliminant les bogues difficiles à trouver ou ignorés par le compilateur. L’utilisation de PREfast est un excellent moyen de réduire la charge de travail et de concentrer les efforts de l’équipe de développement et de l’équipe de test. prefast est disponible dans Visual Studio Team Suite et Visual Studio Team Edition for Software Developers en tant que Code Analysis, activée par le commutateur de compilateur **/analyze**. (cette option est également disponible dans la version gratuite du compilateur fourni avec le Kit de développement logiciel (sdk) Windows.)

> [!Note]  
> Visual Studio 2012 prend en charge **/analyze** dans toutes les éditions. pour plus d’informations sur la disponibilité de l’analyse du code dans toutes les éditions de Visual Studio, consultez [what’s New in Code Analysis](/archive/blogs/codeanalysis/?m=20123).

 

Grâce à l’utilisation de l’annotation d’en-tête (en particulier pour les arguments de pointeur de mémoire tampon), PREfast peut exposer des problèmes supplémentaires, tels que des bogues de remplacement de mémoire, une source commune d’incidents et des failles de sécurité potentielles. Cette opération s’effectue à l’aide du langage d’annotation standard (SAL), qui est une forme de marquage pour les prototypes de fonction C/C++ qui fournissent des informations supplémentaires sur la sémantique attendue des arguments du pointeur et la corrélation avec les paramètres de longueur, les tailles des mémoires tampons déclarées, etc. tous les en-têtes pour les systèmes d’exploitation Windows sont annotés, et l’ajout de la marque SAL dans les en-têtes d’API publics dans vos propres bibliothèques permet à prefast d’effectuer des contrôles plus détaillés et plus ambitieux dans votre code client pour ces api. Pour obtenir une présentation de SAL et des liens vers des informations supplémentaires, consultez l’entrée de blog de Michael Howard, «[une brève introduction au langage d’annotation standard (SAL)](/archive/blogs/michael_howard/a-brief-introduction-to-the-standard-annotation-language-sal)».

</dd> <dt>

<span id="Windows_Application_Verifier"></span><span id="windows_application_verifier"></span><span id="WINDOWS_APPLICATION_VERIFIER"></span>Windows Application Verifier
</dt> <dd>

le Windows Application Verifier ou AppVerifier peut aider les testeurs en fournissant plusieurs fonctions dans un même outil. AppVerifier est un outil qui a été développé pour rendre les erreurs de programmation courantes plus faciles à tester. AppVerifier peut vérifier les paramètres passés aux appels d’API, injecter une entrée erronée pour vérifier la capacité de gestion des erreurs et enregistrer les modifications dans le registre et le système de fichiers. AppVerifier peut également détecter les dépassements de mémoire tampon dans le segment de mémoire, vérifier qu’une liste de Access Control (ACL) a été correctement définie et appliquer l’utilisation sécurisée des API de Socket. Bien qu’il ne soit pas exhaustif, AppVerifier peut être un outil de la boîte à outils du testeur pour aider un produit de la qualité de la version de Development Studio.

Pour plus d’informations sur Application Verifier, consultez [Application Verifier](/previous-versions/visualstudio/visual-studio-2008/ms220948(v=vs.90)) et [utilisation de Application Verifier dans le cycle de vie du développement de logiciels](/previous-versions/aa480483(v=msdn.10)) sur MSDN.

</dd> <dt>

<span id="Fuzz_Testing"></span><span id="fuzz_testing"></span><span id="FUZZ_TESTING"></span>Test aléatoire
</dt> <dd>

Le *test aléatoire* est une méthode semi-automatisée de test qui peut améliorer les méthodologies de test actuelles. L’idée centrale derrière le test de fuzzs consiste à effectuer une évaluation complète de toutes les entrées en entrant des données aléatoires pour voir ce qui se passe. Cela comprend toutes les données réseau, mods et les jeux enregistrés, etc. Le test aléatoire est relativement facile à effectuer. Il suffit de modifier les fichiers bien formés ou les données réseau en insérant des octets aléatoires, en inversant les octets adjacents ou en inversant les valeurs numériques. 0xFF, 0xFFFF, 0xFFFFFFFF, 0x00, 0x0000, 0x00000000 et 0x80000000 sont des valeurs qui sont efficaces pour exposer des failles de sécurité pendant des tests de fuzzing. Vous pouvez observer les combinaisons d’interaction résultantes à l’aide de AppVerifier. Si le fuzzing n’est pas exhaustif, il est facile à implémenter et à automatiser, et il peut intercepter les bogues plus difficiles et imprévisibles.

Pour plus d’informations sur les tests de fuzzing, consultez les *étapes pratiques de présentation de* [Gamefest 2007](/previous-versions/dn629515(v=msdn.10)) dans Game Security.

</dd> <dt>

<span id="Authenticode_Signing"></span><span id="authenticode_signing"></span><span id="AUTHENTICODE_SIGNING"></span>Signature Authenticode
</dt> <dd>

Authenticode est une méthode permettant de s’assurer que les fichiers exécutables, les fichiers DLL et les packages d’installation Windows (fichiers .msi) reçus par l’utilisateur ne sont pas modifiés par rapport à ce qu’un développeur a publié. En utilisant une combinaison de principes cryptographiques, d’entités approuvées et de normes industrielles, Authenticode vérifie l’intégrité du contenu exécutable. Microsoft fournit une API de chiffrement, CryptoAPI, qui peut être utilisée pour détecter automatiquement la falsification du code signé. Si une fuite de sécurité se produit après une publication, un certificat peut être révoqué et tout le code signé avec ce certificat arrête de s’authentifier. La révocation d’un certificat révoque la validation de tous les titres signés avec ce certificat. Windows a été conçu pour fonctionner avec la signature Authenticode et alertera un utilisateur de code non signé, dans des situations spécifiques, qui pourrait exposer l’ordinateur d’un utilisateur à des attaques.

Authenticode ne doit pas être considéré comme une méthode d’élimination des problèmes de sécurité, mais une méthode de détection de falsification après la publication d’un fichier exécutable. Un exécutable ou une DLL qui contient un problème de sécurité exploitable peut être signé et vérifié à l’aide d’Authenticode, mais il présente toujours le problème de sécurité au nouveau système. Une fois que le produit ou la mise à jour a été vérifié pour être sécurisé, le code doit être signé pour garantir aux utilisateurs qu’ils disposent d’une version qui n’a pas été falsifiée.

Même si un développeur pense qu’il n’y a aucune menace de la modification de ses versions, d’autres technologies et services s’appuient sur Authenticode. La signature de code est facile à intégrer et à automatiser ; Il n’y a aucune raison pour laquelle les versions ne sont pas signées par les développeurs.

Pour plus d’informations sur la signature Authenticode, consultez [signature Authenticode pour les développeurs de jeux](./authenticode-signing-for-game-developers.md).

</dd> <dt>

<span id="Minimize_Privileges"></span><span id="minimize_privileges"></span><span id="MINIMIZE_PRIVILEGES"></span>Réduire les privilèges
</dt> <dd>

En général, les processus doivent s’exécuter avec l’ensemble minimal de privilèges requis pour fonctionner. sur Windows Vista et Windows 7, cela s’effectue à l’aide du [contrôle de compte d’utilisateur](./user-account-control-for-game-developers.md), ce qui permet au jeu de s’exécuter en tant qu’utilisateur Standard plutôt qu’en tant qu’administrateur. pour Windows XP, les jeux sont généralement exécutés en tant qu’administrateur. même sur Windows Vista et Windows 7, il est parfois nécessaire d’élever à des droits d’administrateur complets pour certaines opérations spécifiques.

Dans les cas où le processus s’exécute avec des droits d’administration complets, en général, seuls quelques droits au-delà de ceux d’un utilisateur standard sont réellement requis. L’accès administratif comprend de nombreux droits qui ne sont pas requis par du code légitime, mais qui peuvent être utilisés par une personne malveillante dans le processus. voici quelques exemples de ces droits : SE appropriation \_ \_ , SE \_ DEBUG, SE \_ create \_ TOKEN, SE \_ ASSIGNPRIMARYTOKEN, SE \_ TCB, SE \_ SECURITY, SE \_ LOAD \_ DRIVER, SE \_ SYSTEMTIME, SE la \_ sauvegarde, SE \_ restore, SE \_ SHUTDOWN et SE \_ AUDIT (voir les [constantes de privilège](../secauthz/privilege-constants.md)).

Même si un processus ne peut pas obtenir plus de droits une fois démarré, il peut facilement accorder des droits. Au démarrage, le processus peut utiliser immédiatement les API Win32 pour supprimer les droits dont il n’a pas besoin.

</dd> <dt>

<span id="Utilize_Windows_Security_Features"></span><span id="utilize_windows_security_features"></span><span id="UTILIZE_WINDOWS_SECURITY_FEATURES"></span>utiliser les fonctionnalités de Sécurité Windows
</dt> <dd>

Windows Vista et Windows 7 incluent un certain nombre de nouvelles fonctionnalités qui améliorent la sécurité du code. Le [contrôle de compte d’utilisateur](./user-account-control-for-game-developers.md) est certainement le plus important à comprendre et à adopter, mais il existe également d’autres fonctionnalités. en plus des technologies Windows XP SP2, telles que le pare-feu Windows, la prévention de l’exécution des données, la vérification de la sécurité des mémoires tampons et la Coffre des gestionnaires d’exceptions qui sont également disponibles sur Windows Vista et Windows 7, il existe trois nouvelles fonctionnalités de sécurité à prendre en compte :

-   Fonctionnalité de randomisation du format d’espace d’adresse d’abonnement. cela est possible en établissant un lien avec l’option **/dynamicbase** sur Visual Studio 2005 Service Pack 1 ou Visual Studio 2008. Cela amène le système à randomiser les positions de nombreuses DLL système clés dans votre espace de processus, ce qui complique grandement l’écriture de programmes d’attaque exploitables qui se propagent largement sur Internet. cet indicateur de l’éditeur de liens est ignoré par Windows XP et les versions antérieures de Windows.
-   la corruption du tas peut mener à une classe entière d’attaques de sécurité. par conséquent, le système de mémoire de Windows Vista et Windows 7 prend désormais en charge un mode qui termine le processus si la corruption du tas est détectée. L’appel de [**HeapSetInformation**](/windows/win32/api/heapapi/nf-heapapi-heapsetinformation) avec **HeapEnableTermianteOnCorruption** va accepter ce comportement. cet appel échoue sur Windows XP et une version antérieure de Windows.
-   Lors de l’écriture de services, ils peuvent être configurés à l’aide d’une nouvelle fonctionnalité pour spécifier les privilèges qui sont réellement requis, ainsi que pour limiter l’accès aux ressources à un SID spécifique. Pour cela, vous devez utiliser [ChangeSeviceConfig2](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a), à l’aide de la configuration du service, informations sur \_ \_ \_ \_ les privilèges et \_ \_ informations SID du service de configuration de service \_ \_ .

</dd> </dl>

## <a name="summary"></a>Résumé

Le développement d’un jeu pour la place de marché actuelle et à venir est long et coûteux. La publication d’un jeu avec des problèmes de sécurité entraînera un coût supplémentaire et un temps de résolution correct. Ainsi, il est dans l’intérêt de tous les développeurs de jeux d’intégrer des outils et des techniques pour atténuer les attaques de sécurité avant leur publication.

Les informations contenues dans cet article sont simplement une introduction à ce qu’un studio de développement peut faire pour vous aider et leurs clients. Vous trouverez plus d’informations sur les pratiques de sécurité et les informations de sécurité générales dans le [Centre de développement Microsoft Security](https://technet.microsoft.com/security/).

 

 