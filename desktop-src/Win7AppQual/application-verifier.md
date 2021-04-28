---
description: Application Verifier (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac2a8bc900ea9d1f35ae228371226355657b930
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088687"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows XP, Windows Vista, Windows 7  
**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2  


## <a name="description"></a>Description

Promouvez et appliquez Application Verifier comme une porte de qualité pour tout le développement. Il comprend plusieurs améliorations :

-   Nous avons fourni des vérifications supplémentaires pour résoudre les problèmes rencontrés par l’équipe Rapport d’erreurs Windows lors de l’utilisation du pool de threads.
-   Nous avons combiné les versions 32 et 64 bits du package pour traiter les modifications apportées à Windows 7, y compris les besoins de test des composants 32 bits sous une version de 64 bits de Windows, ainsi que pour une simplification générale.
-   Nous avons inclus des vérifications supplémentaires pour les applications multithread, en exécutant des applications 32 bits sur Windows 64 bits, ainsi que de nombreux correctifs de bogues.

Ces modifications ne doivent pas avoir d’impact négatif sur les utilisateurs qui n’activent pas les vérifications de thread. ceux qui doivent bénéficier d’une prise en charge supplémentaire dans la découverte et le diagnostic des problèmes d’utilisation existants du pool de threads. Que vous activiez ou non des vérifications de thread, vous tirerez parti des autres améliorations et correctifs de bogues dans ce service.

Bien qu’il y ait une légère baisse des performances lors de l’utilisation de ce service, les niveaux de performances doivent rester acceptables, car ils ne sont généralement pas exécutés dans les environnements de vente au détail.

## <a name="usage"></a>Utilisation

**Informations générales**

Pour fournir des applications Windows fiables :

1.  Testez les applications écrites en code non managé (natif) avec Application Verifier sous le débogueur et avec le tas de pages entières avant de les publier auprès des clients.
2.  Suivez les étapes fournies par Application Verifier pour résoudre les conditions errantes.
3.  Une fois votre application publiée, surveillez régulièrement les rapports d’échec de l’application collectés par Rapport d’erreurs Windows.

Les vérifications de pool de threads sont activées par défaut sous l’en-tête de contrôle « notions de base ». Comme cela est inclus dans le paramètre par défaut, les utilisateurs doivent uniquement exécuter Application Verifier sur leur code avec les paramètres par défaut pour tirer parti des nouvelles vérifications.

**Détails**

Au minimum, vous devez exécuter Application Verifier avec le paramètre de base sélectionné. Cela est requis pour WinLogo et WinQual. Le paramètre de base vérifie les éléments suivants :

-   **Exceptions arrêter les détails** : garantit que les applications ne masquent pas les violations d’accès à l’aide de la gestion structurée des exceptions
-   **Gère les détails des arrêts** -tests pour vérifier que l’application n’essaie pas d’utiliser des handles non valides
-   **Détails** de l’arrêt des segments de mémoire-vérifications des problèmes d’altération de mémoire dans le tas
-   **Détails des arrêts d’entrée/sortie** : contrôle l’exécution des e/s asynchrones et effectue différentes validations
-   **Détails** de l’arrêt de fuite : détecte les fuites en effectuant le suivi des ressources effectuées par une dll qui ne sont pas libérées au moment où la dll a été déchargée.
-   **Verrous arrêter les détails** -vérifie l’utilisation correcte pour les sections critiques
-   **Détails** de l’arrêt de la mémoire-Assurez-vous que les API pour les manipulations d’espace virtuel sont utilisées correctement (par exemple, VirtualAlloc, MapViewOfFile)
-   **Détails des arrêts TLS** -garantit que les API de stockage local des threads sont utilisées correctement
-   **Détails des arrêts de ThreadPool** -garantit l’utilisation correcte des API ThreadPool et applique des vérifications de cohérence sur les États de thread de travail après un rappel

Si votre application effectue une migration à partir d’une application « pré-Vista », vous souhaiterez peut-être tirer parti de la « LuaPriv » (également appelée vérifications UAC). Le prédiction de privilège de compte d’utilisateur limité (LuaPriv) a deux objectifs principaux :

-   **Prédictif**: lors de l’exécution d’une application avec des privilèges d’administrateur, prédire si cette application fonctionne également si elle est exécutée avec moins de privilèges (en général, en tant qu’utilisateur normal). Par exemple, si l’application écrit dans des fichiers qui autorisent uniquement l’accès des administrateurs, cette application ne sera pas en mesure d’écrire dans le même fichier si elle est exécutée en tant que non-administrateur.
-   **Diagnostic**: en cas d’exécution avec des privilèges non-administrateurs, identifiez les problèmes potentiels qui peuvent exister déjà avec l’exécution actuelle. Dans l’exemple précédent, si l’application tente d’écrire dans un fichier qui accorde uniquement l’accès aux membres du groupe administrateurs, l’application obtiendra une erreur d’accès \_ refusé. Si l’application ne fonctionne pas correctement, cette opération peut être à l’origine du problème.

LuaPriv identifie les types de problèmes suivants :



| **Problème potentiel**       | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espaces de noms restreints     | La création d’un objet de synchronisation nommé (événement, sémaphore, mutex, etc.) sans espace de noms peut compliquer l’exécution sans privilège sur certains systèmes d’exploitation, car le système d’exploitation peut choisir de placer l’objet dans un espace de noms restreint. La création d’un tel objet dans un espace de noms restreint (tel que l’espace de noms global) requiert SeCreateGlobalPrivilege, qui est accordé uniquement aux administrateurs.<br/> LuaPriv signale ces deux problèmes s’ils sont détectés.<br/> |
| Vérifications de l’administrateur matériel | Certaines applications interrogent le jeton de sécurité de l’utilisateur pour déterminer le niveau de privilège dont il dispose. Dans ce cas, l’application peut modifier son comportement en fonction de la puissance que l’utilisateur estime avoir. <br/> LuaPriv signale les appels d’API qui retournent ces informations.<br/>                                                                                                                                                                                                |
| Privilèges de demande     | Une application peut tenter d’activer un privilège de sécurité (par exemple, SeTcbPrivilege ou SeSecurityPrivilege) avant d’effectuer une opération qui l’exige. <br/> LuaPriv Flags tente d’activer des privilèges de sécurité. <br/>                                                                                                                                                                                                                               |
| Privilèges manquants        | Si une application tente d’activer un privilège que l’utilisateur n’a pas, elle signale probablement que l’application attend le privilège, ce qui peut entraîner des différences de comportement. <br/> LuaPriv signale les demandes de privilèges ayant échoué. <br/>                                                                                                                                                                                                                                       |
| Opérations de INI-File       | Les tentatives d’écriture dans les fichiers INI mappés (WritePrivateProfileSection et les API similaires) peuvent échouer en tant qu’utilisateur non-administrateur. <br/> LuaPriv signale ces opérations.<br/>                                                                                                                                                                                                                                                                                                            |
| accès refusé             | Si l’application tente d’accéder à un objet (fichier, clé de Registre, etc.), mais que la tentative échoue en raison d’un accès insuffisant, l’application s’attend probablement à s’exécuter avec plus de privilèges que nécessaire. <br/> LuaPriv Flags Object : ouvre les tentatives qui échouent avec un accès \_ refusé et des erreurs similaires.<br/>                                                                                                                                                               |
| Refuser les ACE                 | Si un objet a des ACE de refus dans sa DACL, il refuse explicitement l’accès à des entités spécifiques. <br/> Cela est rare et complique la prédiction, de sorte que LuaPriv signale les ACE de refus lorsqu’il les trouve.<br/>                                                                                                                                                                                                                                                                     |
| Accès restreint         | Si une application tente d’ouvrir un objet pour des droits qui ne sont pas accordés à des utilisateurs normaux (par exemple, en tentant d’écrire dans un fichier qui peut être écrit uniquement par des administrateurs), l’application ne fonctionnera probablement pas de la même façon lorsqu’elle est exécutée en tant qu’utilisateur normal. <br/> LuaPriv signale ces opérations.<br/>                                                                                                                                                                      |
| MAXIMUM \_ autorisé          | Si une application ouvre un objet pour un MAXIMUM \_ autorisé, la vérification de l’accès sur l’objet se produit ailleurs. La plupart du code qui effectue cette opération ne fonctionne pas correctement et fonctionnera presque certainement différemment lorsqu’il est exécuté sans privilège. <br/> LuaPriv signale donc tous les incidents de MAXIMUM \_ autorisé. <br/>                                                                                                                                                            |



 

Les problèmes fréquemment négligés sont capturés dans les vérifications diverses floues :

-   Détails des arrêts des API dangereuses
-   Détails de l’arrêt des piles modifiées
-   Substitution temporelle

Nous avons ajouté un nouveau vérificateur d’impression. Cette couche permet de trouver et de résoudre les problèmes qui peuvent se produire lorsqu’une application appelle le sous-système d’impression. Le vérificateur d’impression cible les deux couches du sous-système d’impression, la couche PrintAPI et la couche PrintDriver.

*Couche API d’impression*

Le vérificateur d’impression teste l’interface entre un programme et winspool. drv et prntvpt.dll et teste les interfaces de ces dll. Vous pouvez passer en revue les règles d’appel des fonctions dans cette interface dans la section d’aide MSDN pour les API exportées par winspool. drv et prntvpt.dll.

*Couche du pilote d’impression*

Le vérificateur d’impression teste également l’interface entre un pilote d’impression principal tel que UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL ou MXDWDRV.DLL et les plug-ins de pilote d’impression. Vous trouverez des informations sur cette interface dans MSDN et le kit WDK.

Notez que certaines de ces vérifications concernent uniquement Windows 7, tandis que d’autres s’exécutent simplement sous Windows 7.

En règle générale, seules les versions de débogage exécutent le Application Verifier, donc les performances ne sont généralement pas un problème. En cas de problèmes de performances dus à l’utilisation de ce ou de tout autre Application Verifier vérification, exécutez un contrôle à la fois jusqu’à ce que vous ayez effectué toutes les vérifications nécessaires.

Près de 10% des blocages d’application sur les systèmes Windows sont dus à une altération du tas. Ces incidents sont presque impossibles à déboguer après le fait. La meilleure façon d’éviter ces problèmes consiste à effectuer des tests avec les fonctionnalités du tas de la page qui se trouvent dans Application Verifier. Il existe deux types de tas de page : « Full » et « Light ». Full est la valeur par défaut ; Il forcera un débogueur à s’arrêter instantanément lors de la détection de l’endommagement. Cette fonctionnalité doit être exécutée sous le débogueur. Toutefois, il s’agit également de la ressource la plus exigeante. Si un utilisateur rencontre des problèmes de synchronisation et qu’il a déjà exécuté un scénario sous le tas d’une page « complète », son affectation à la valeur « Light » est susceptible de résoudre ces problèmes. En outre, le segment de mémoire de la page Light ne se bloque pas tant que le processus n’est pas terminé. Il fournit une trace de la pile à l’allocation, mais peut prendre beaucoup plus de temps pour diagnostiquer l’utilisation de son équivalent complet.

Surveiller l’état de fiabilité des applications via le portail Web winqual. Ce portail affiche les rapports d’erreurs collectés via Rapport d’erreurs Windows. il est donc facile d’identifier les échecs les plus fréquents. Pour en savoir plus, consultez Rapport d’erreurs Windows : Prise en main. Microsoft n’effectue pas de facturation pour ce service.

Pour tirer parti de WinQual, vous devez :

1.  Inscrivez votre société à WinQual, ce qui nécessite un ID VeriSign. Vous trouverez des informations sur Windows 7 sur WinQual dans le portail des développeurs, regroupés sous Windows Vista SP1 \\ Windows Server 2008. Il aura bientôt un emplacement Windows 7.
2.  Mappez les applications ISV à un nom de produit et le nom de l’éditeur de logiciels, qui lie les rapports d’échec à l’entreprise. Les autres éditeurs de logiciels indépendants ne peuvent pas afficher vos rapports d’erreurs.
3.  Utilisez le portail pour identifier les principaux problèmes. Les éditeurs de logiciels indépendants peuvent également créer des réponses qui informent les clients des étapes à suivre après une défaillance. Le système de réponse prend en charge plus de 10 langues dans le monde.

Autre Remarque : Application Verifier est aussi efficace que les chemins de code sur lesquels vous l’exécutez. La valeur de la combinaison de cet outil avec un outil de couverture du code ne peut pas être surévaluée.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

**Outils de débogage pour Windows :**

-   [Vue d’ensemble et site de téléchargement](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [Documentation en ligne MSDN](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Vue d'ensemble](/previous-versions/ms220948(v=vs.80))
-   [Télécharger](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier pour Microsoft Visual Studio 2008/.NET Framework 3,5](/previous-versions/ms220948(v=vs.80))

    **Remarque :** la version de Application Verifier fournie dans Visual Studio est tout à fait datée. Si possible, utilisez le package autonome à la place. Pour cette raison, les futures versions de Visual Studio n’auront plus de Application Verifier incorporées.

**WinQual**

-   [Windows Quality Online Services (winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Rapport d’erreurs Windows : Prise en main](../wer/using-wer.md)

 

 
