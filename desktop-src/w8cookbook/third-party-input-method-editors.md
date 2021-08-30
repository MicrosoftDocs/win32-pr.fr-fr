---
title: Éditeurs de méthode d’entrée tiers
description: Éditeurs de méthode d’entrée tiers
ms.assetid: 7FFD7210-2335-4499-A36A-ACFAECEB01F9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e12b2c2788ed95509b785dd7fc2c5ba3ec0a31ac46a736bc7dfdc92c7289f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815104"
---
# <a name="third-party-input-method-editors"></a>Éditeurs de méthode d’entrée tiers

## <a name="platforms"></a>Plateformes

**Clients** -Windows 8  
**serveurs** -Windows Server 2012  


## <a name="description"></a>Description

Les éditeurs de méthode d’entrée (IME) sont des composants logiciels qui permettent à un utilisateur de taper du texte dans une langue dont le nombre de caractères est supérieur à celui pouvant être représenté sur un clavier. (Il est courant, mais sans s’en limiter, aux langues d’Extrême-Orient.) Au lieu que chaque caractère unique apparaisse sur une clé unique, les utilisateurs tapent des combinaisons de clés qui sont ensuite interprétées par l’IME. L’IME génère le caractère qui correspond à l’ensemble des séquences de touches, ce qui présente parfois l’utilisateur avec une liste de caractères possibles à sélectionner, puis insère le caractère dans la fenêtre Modifier le contrôle de l’application de l’utilisateur.

dans le passé, Windows a autorisé l’exécution des éditeurs de logiciels tiers dans le système Windows, et cette fonctionnalité se poursuit pour Windows 8. Les utilisateurs peuvent installer un IME tiers et l’utiliser. En outre, nous sécurisons le système et les processus pour empêcher les éditeurs de logiciels malveillants, améliorer la sécurité et améliorer l’expérience utilisateur.

dans Windows 8, vous trouverez :

-   Prise en charge des éditeurs de logiciels tiers pour les claviers et claviers tactiles
-   Les fournisseurs d’éditeurs de logiciels indépendants tiers doivent suivre les instructions Microsoft pour développer leurs éditeurs IME pour Windows 8
-   Les éditeurs de logiciels tiers doivent être signés numériquement
-   Les éditeurs de logiciels tiers doivent être compatibles avec Text Services Framework (TSF) et les indicateurs IME appropriés doivent être configurés pour s’exécuter correctement dans Windows 8
-   les éditeurs de logiciels tiers hérités peuvent être exécutés dans les applications de bureau, mais ils seront bloqués dans les applications Windows du windows Store
-   les éditeurs de logiciels tiers peuvent utiliser la disposition de clavier tactile fournie par Windows pour lier leur ime, afin que les utilisateurs puissent utiliser leur ime avec des claviers tactiles. Toutefois, certaines fonctions des IME intégrés pour les claviers tactiles ne seront pas disponibles pour les éditeurs de logiciels tiers.
-   Windows Defender supprimera les éditeurs de logiciels malveillants du système Windows

## <a name="manifestation"></a>Manifestation

**Langue d’entrée et changement de méthode d’entrée**

Au lieu d’afficher toutes les icônes du mode IME avec l’icône de personnalisation de l’éditeur IME, une seule icône mode IME s’affiche avec l’icône de personnalisation de l’éditeur IME. les deux figures ci-dessous illustrent la Windows 8 menu volant d’entrée et le menu volant ime, avec l’ime japonais comme méthode d’entrée actuelle. Si vous cliquez sur l’icône de personnalisation de l’éditeur IME, vous pouvez basculer les méthodes d’entrée.

![changer de méthode d’entrée](images/inputindicator2.png)

Si vous cliquez sur l’icône mode IME, vous pouvez basculer vers un autre mode IME.

![changer les modes IME](images/inputindicator1.png)

si un ime s’appuie sur la barre de langue pour afficher ses icônes de mode dans Windows 7, l’ime doit être modifié afin de présenter son icône de personnalisation et son icône de mode dans l’indicateur d’entrée dans Windows 8.

> [!Note]  
> remarque : les détails sur la façon dont un IME peut afficher son icône de personnalisation et son icône de mode dans le SysTray de la barre des tâches du bureau seront documentés et publiés publiquement dans les instructions de Windows 8 IME.

 

**nouvel environnement de Windows**

l’environnement de Windows 8 modifie le paysage des ime. les concepts de Windows applications du Store, les conteneurs d’applications de contexte local et les restrictions d’API sur les éditeurs de logiciels n’étaient pas présents dans Windows 7. certains ime Windows 7 existants cessent de répondre lorsqu’ils sont exécutés dans une application Windows store et n’autorisent donc pas l’exécution d’ime hérités dans Windows applications du windows store. en outre, assurez-vous que les nouvelles versions des éditeurs ime sont validées pour s’assurer qu’elles sont compatibles avec le nouvel environnement d’interface utilisateur avant de les exécuter dans Windows applications du windows Store.

## <a name="mitigation"></a>Limitation des risques

Vous pouvez utiliser un IME compatible avec le Bureau sur le système. Il peut s’agir de votre meilleure option si vous utilisez principalement des applications de bureau et que vous souhaitez continuer à utiliser un IME hérité préféré pour l’entrée. nous vous recommandons d’utiliser un Windows 8 IME et de cesser d’utiliser des ime hérités/non certifiés. Les notifications sont fournies à la fois par le CPL de la langue et par le commutateur d’entrée pour vous avertir des effets de l’utilisation d’un IME compatible avec le bureau.

Vous verrez l’un des comportements ci-dessous si un IME compatible avec le Bureau ne fonctionne pas sur votre système :

-   Le panneau de l’interface utilisateur étiquette d’interface utilisateur des éditeurs de logiciels compatibles Desktop et affiche un message indiquant que les éditeurs de logiciels non compatibles fonctionnent uniquement dans les applications de bureau.
-   le menu volant d’entrée greys les ime compatibles avec le bureau lorsque l’utilisateur se trouve dans Windows applications du windows Store. Cela indique que l’IME ne fonctionne pas dans cette application. (Dans le bureau, les éditeurs de la compatibilité avec les ordinateurs de bureau ne sont pas grisés). si vous basculez vers Windows applications du Store avec un ime non compatible et que l’ime est désactivé, utilisez l’indicateur d’entrée pour passer à un ime compatible Windows avec les applications du windows Store.

Les IME hérités ou compatibles avec le bureau sont limités aux conditions suivantes :

-   mise à niveau de Windows 7 vers Windows 8, avec des éditeurs de logiciels tiers sur le système
-   le fournisseur n’a pas publié une version compatible avec Windows 8, et l’utilisateur tente d’utiliser une version existante de Windows 7 en attendant

## <a name="solution"></a>Solution

**Général**

utilisez l’infrastructure TSF (text services framework) existante pour implémenter votre logique IME et les contrôles communs de l’application Windows Store pour vos interfaces utilisateur. Créez des fenêtres détenues pour héberger votre interface utilisateur.

De nouvelles API de recherche sont ajoutées pour améliorer la prédiction de recherche et fournir une expérience de recherche plus propre dans l’interface utilisateur.

Des API sont également ajoutées pour notifier les éditeurs de logiciels tiers lorsqu’un clavier tactile est appelé pour empêcher l’interface utilisateur d’être couverte par le clavier tactile. Une disposition de clavier tactile classique par défaut est automatiquement chargée pour les éditeurs de logiciels tiers. Aucun travail supplémentaire n’est nécessaire pour l’intégration à cette disposition de clavier tactile classique. Toutefois, les éditeurs de logiciels tiers pourront demander une autre disposition tactile.

familiarisez-vous avec les instructions de Windows 8 IME pour pouvoir promouvoir les principes de l’expérience utilisateur de l’application key Windows Store dans votre IME. Les IME conformes aux indications doivent définir un indicateur pour indiquer que l’IME est compatible avec la conception Microsoft. Windows 8 empêche l’exécution de tous les éditeurs de logiciels compatibles avec le bureau dans Windows applications du windows Store.

la signature numérique, en plus de la révocation par Windows Defender, empêche l’installation d’éditeurs ime sur le système Windows 8. Lors de la vérification d’identité, le .dll d’un IME tiers est signé numériquement. Seuls les IME qui ont cette signature numérique peuvent être installés sur le système sans qu’un message d’avertissement critique ne s’affiche pour l’utilisateur. Les utilisateurs peuvent signaler des éditeurs de logiciels malveillants. une fois qu’un IME a été identifié comme malveillant, Windows Defender le supprime du système Windows.

**Text Services Framework**

L’IME doit être sensible à TSF pour pouvoir s’exécuter dans Windows 8. Windows 8 empêche les ime non sensibles à TSF de s’exécuter Windows dans les applications du windows Store. Quand une application est démarrée, TSF charge l' .dll IME pour l’éditeur de méthode d’entrée que l’utilisateur a sélectionné dans le processus d’application.

> [!Note]  
> pour fournir des fonctionnalités ou des interfaces utilisateur distinctes entre Windows applications du windows Store et les applications de bureau, le .dll chargé par TSF peut vérifier le type d’application dans lequel il est chargé. L’IME appelle la méthode [ITfThreadMgrEx :: GetActiveFlags](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags) et vérifie l' \_ indicateur TF TMF \_ IMMERSIVEMODE et peut déclencher une logique d’application différente en fonction du résultat.

 

quand un IME est chargé dans une application Windows Store, il est soumis aux mêmes restrictions de conteneur d’application que l’application elle-même. ce comportement garantit que les ime ne sont pas en mesure de violer Windows les contrats de sécurité des applications du store, même si vous avez accès au kit de développement logiciel (SDK) du bureau (car ils ne sont pas distribués ou certifiés par le Windows Store). Certaines fonctions actuellement exécutées par les IME sont affectées dans un conteneur d’application. Ces fonctions sont les suivantes :

-   Fichiers de dictionnaire
-   Mise à jour Internet
-   Apprentissage à la volée
-   Partage d’informations entre les processus

pour plus d’informations, consultez les instructions relatives à l’Windows 8 IME.

les éditeurs ime hérités ne fonctionnent pas dans les applications Windows store afin d’éviter le risque d’expériences utilisateur incorrectes, notamment les arrêts du système. les éditeurs de logiciels compatibles compatibles avec les applications du Windows Store doivent être déclarés automatiquement en définissant un indicateur qui indique cette compatibilité. Cet indicateur est fourni par TSF dans la \_ structure INPUTPROCESSORPROFILE TF. pour plus d’informations sur l’utilisation de cet indicateur afin de déclarer un IME tiers en tant que Windows Store compatible avec l’application, vous devez le documenter et le publier publiquement dans les instructions Windows 8 IME.

les éditeurs de logiciels compatibles compatibles avec les applications Windows store sont autorisés à s’exécuter dans les applications de bureau ou les applications du windows store Windows. Les IME qui ne sont pas compatibles peuvent uniquement s’exécuter dans les processus de bureau.

**Interface utilisateur**

Bien que les éditeurs de logiciels tiers aient accès aux API de fenêtrage de bureau, ils doivent suivre les mêmes restrictions d’API de fenêtre que l’application dans laquelle ils s’exécutent. par exemple, un IME ne peut pas être dessiné en plus d’une application Windows Store, alors qu’elle est active dans une application de bureau. Les restrictions d’API sont destinées à éviter les scénarios suivants :

-   applications de bureau qui se concentrent sur les applications Windows store
-   dessin d’applications de bureau dans l’application Windows Store
-   applications de bureau interférant avec les applications du windows Store Windows

**Prise en charge du clavier tactile**

Bien que la prise en charge du clavier tactile (TKB) soit toujours disponible pour les fournisseurs d’éditeurs de logiciels indépendants tiers, une expérience de clavier tactile entièrement personnalisable et intégrée n’est pas fournie dans Windows 8. Toutefois, les éditeurs de logiciels tiers peuvent mapper leurs IME avec la disposition de clavier optimisée pour la saisie tactile. le panneau SIP de Windows fournit une disposition de clavier classique par défaut pour les éditeurs de logiciels tiers. Étant donné que le clavier classique génère des événements clés similaires à ceux d’un clavier matériel, il n’existe actuellement aucune exigence particulière d’implémentation spéciale pour que les éditeurs de logiciels tiers fonctionnent avec un clavier tactile. La gestion des entrées pour les événements de clé matérielle traitera également les événements clés des dispositions tactiles classiques.

> [!Note]  
> Remarque : les éditeurs de données peuvent devoir commencer à gérer les événements d’entrée Unicode si la prise en charge de TKB est étendue pour inclure également des dispositions de clavier optimisées.

 

Un éditeur IME tiers peut choisir d’utiliser la disposition de clavier optimisée pour son IME. Pour plus d’informations, consultez les instructions relatives aux éditeurs de logiciels tiers.

Assurez-vous que l’interface utilisateur de votre volet candidat (et les autres éléments d’interface utilisateur) ne sont pas dessinés sous le clavier tactile. Dans la plupart des cas, l’application doit redimensionner sa fenêtre pour tenir compte du clavier tactile. Toutefois, si une application ne le fait pas, les éditeurs IME peuvent toujours utiliser l’API InputPaneFramework pour apprendre la position du clavier tactile. Les éditeurs de logiciels indépendants peuvent utiliser cette API pour récupérer l’espace à l’écran utilisé par le clavier tactile avant de dessiner des interfaces utilisateur candidates (ou autres) et redistribuer leur interface utilisateur pour éviter le dessin sous le clavier tactile.

**Dans**

dans Windows 8, les applications du Store Windows peuvent facilement fournir à leurs utilisateurs des fonctionnalités de recherche en implémentant le [contrat de recherche](/previous-versions/windows/apps/hh464906(v=win.10)) et en les intégrant au volet de recherche. Le volet de recherche est un emplacement central où les utilisateurs peuvent effectuer des recherches dans toutes leurs applications. Windows permet aux applications qui utilisent le volet de recherche d’obtenir la valeur la plus rapide possible pour les utilisateurs. en particulier, pour les utilisateurs de l’IME, il fournit une expérience de recherche unique qui permet d’intégrer les éditeurs de données compatibles avec les Windows 8 pour une efficacité et une convivialité accrues.

Un IME est compatible avec l’expérience de recherche intégrée s’il répond aux critères suivants :

-   est compatible avec l’environnement de l’application du Store Windows
-   Implémente les API de mode UILess TFS
-   Implémente les API d’intégration de recherche TFS :
-   -   ItfSearchCandidateProvider
    -   ItfSearchHardwareKeyboardBehaviors

Lorsqu’il est activé dans le volet de recherche, l’IME compatible est placé en mode UILess et ne peut pas afficher son interface utilisateur. au lieu de cela, il envoie des candidats de conversion à Windows, qui les affiche ensuite dans le contrôle de liste de candidat en ligne.

l’IME envoie également Windows candidats qui doivent être utilisés pour exécuter la recherche actuelle. ces candidats peuvent être les mêmes que les candidats à la conversion, ou peuvent être personnalisés pour la recherche. Les bons candidats à la recherche répondent à ces critères :

-   Aucun chevauchement de préfixe
-   Aucun candidat de prédiction (uniquement la saisie semi-automatique)

les ime qui ne satisfont pas aux critères et qui ne sont pas compatibles avec la recherche sont affichés de la même façon que dans d’autres contrôles de l’application Windows Store et ne peuvent pas tirer parti de l’intégration de l’interface utilisateur et des candidats à la recherche. (Les applications reçoivent des requêtes uniquement une fois que l’utilisateur a terminé la composition.)

Lorsqu’une application qui prend en charge le contrat de recherche reçoit une requête, l’événement de requête inclut un tableau « queryTextAlternatives » contenant toutes les alternatives connues, classées du plus pertinent au moins pertinent (improbable). Chaque fois que des alternatives sont fournies, l’application doit traiter chaque alternative comme une requête et retourner tous les résultats qui correspondent à l’une des alternatives (comme si l’utilisateur avait émis plusieurs requêtes en même temps), en émettant une requête « ou » au service qui fournit les résultats. Pour améliorer les performances, les applications limitent souvent les correspondances aux 10 alternatives les plus pertinentes.

**Signature numérique IME**

tous les éditeurs de logiciels tiers doivent être signés numériquement afin d’être installés sur le système Windows 8 en tant qu’éditeur IME. À l’aide de SmartScreen, les utilisateurs peuvent voir un message d’avertissement lors du téléchargement d’un IME non signé à partir du Web. Pour obtenir un certificat et signer vos fichiers :

-   **Utiliser une signature Authenticode pour signer numériquement des programmes**
    -   Obtenez un certificat de signature de code Authenticode valide à partir de l’une des nombreuses autorités de certification prises en charge par Windows
    -   Utiliser les outils de développement (tels que [signtool.exe](../seccrypto/signtool.md)) pour signer les applications avant la distribution
    -   Pour plus d’informations et pour obtenir une description pas à pas du processus de signature de code, consultez l’entrée de blog [tout ce que vous devez savoir sur la signature de code Authenticode](/archive/blogs/ieinternals/everything-you-need-to-know-about-authenticode-code-signing)
-   **S’assurer que les téléchargements ne sont pas détectés en tant que programmes malveillants**
    -   Les programmes téléchargés qui sont détectés et confirmés comme logiciels malveillants affectent la réputation du téléchargement et la réputation du certificat numérique utilisé pour signer ce fichier
-   **demander une certification Windows**
    -   visitez la page de Certification de l’application Windows sur MSDN

Pour plus d’informations, consultez les articles suivants sur les signatures numériques et la signature de code :

-   [Vue d’ensemble d’Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantie de l’intégrité et de l’authenticité](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Meilleures pratiques pour la signature de code](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [Que sont les certificats numériques ?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

Si un IME **n’est pas** signé, l’utilisateur reçoit ce message d’avertissement lorsqu’il tente de télécharger l’IME :

![le message d’avertissement IME n’est pas signé](images/downloadwarning02-fhu-ivu.png)

Si un IME est signé, les utilisateurs voient ce message à la place :

![message signé avec l’IME](images/downloadwarning01-fhu-vcu.png)

En fonction de ces notifications, les utilisateurs peuvent choisir de supprimer le fichier ou d’ignorer l’avertissement et d’exécuter le programme téléchargé.

**Révocation IME**

les éditeurs de logiciels malveillants qui sont malveillants ou qui ne suivent pas les instructions de Windows 8 IME peuvent être supprimés du système à l’aide de Windows Defender. Pour plus d’informations sur les éditeurs de logiciels indépendants malveillants, consultez l’article sur les [éditeurs de logiciels tiers dans Windows 8](/previous-versions/windows/apps/hh967426(v=win.10)).

## <a name="resources"></a>Ressources

-   [ITfThreadMgrEx :: obtient la méthode Flags active](/windows/win32/api/msctf/nf-msctf-itfthreadmgrex-getactiveflags)
-   [SignTool](../seccrypto/signtool.md)
-   [Tout ce que vous devez savoir sur la signature de code Authenticode](https://blogs.msdn.com/b/ieinternals/archive/2011/03/22/authenticode-code-signing-for-developers-for-file-downloads-building-smartscreen-application-reputation.aspx)
-   [Windows les contrats et les extensions d’application](/previous-versions/windows/apps/hh464906(v=win.10))
-   [conditions de Certification pour les applications de bureau Windows 8](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [conditions de Certification pour les applications Windows](https://msdn.microsoft.com/library/windows/apps/51A7C609-94AB-49ab-B8E0-F26FF776DDB4.aspx)
-   [Utilisation du Kit de certification des applications Windows](../win_cert/using-the-windows-app-certification-kit.md)
-   [Vue d’ensemble d’Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537359(v=vs.85))
-   [Garantie de l’intégrité et de l’authenticité](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)#Ensuring_Integrity_a)
-   [Meilleures pratiques pour la signature de code](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
-   [Que sont les certificats numériques ?](/previous-versions/office/developer/office2000/aa190113(v=office.10))

 

 