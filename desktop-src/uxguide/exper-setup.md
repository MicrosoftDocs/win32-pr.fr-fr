---
title: Programme d’installation
description: Les utilisateurs ne bénéficient pas de l’installation de logiciels, donc les expériences d’installation modernes doivent être simples, efficaces et sans problème.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4e5de6f15dd797dd1d1362d1b515122b78c770f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295998"
---
# <a name="setup"></a>Programme d’installation

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les utilisateurs ne bénéficient pas de l’installation de logiciels, donc les expériences d’installation modernes doivent être simples, efficaces et sans problème.

Le programme d’installation de se réfère généralement à l’expérience d’installation et de configuration initiale d’un programme. Toutefois, le programme d’installation peut également faire référence à un cycle de vie d’installation complet, y compris l’installation initiale, les mises à jour incrémentielles du programme (telles que les mises à niveau de version ou les service packs), la réparation et la désinstallation.

La plupart des utilisateurs considèrent la configuration comme un mal nécessaire, à effectuer aussi rapidement que possible. Le point d’installation du programme consiste à l’utiliser, et non à prendre des décisions incorrectes sur la configuration et l’utilisation, ou pire encore, à consacrer beaucoup de temps à répondre à des questions personnelles utilisées à des fins d’inscription ou de marketing.

![Capture d’écran montrant une boîte de dialogue de configuration avec quatre options.](images/exper-setup-image1.png)

Une expérience d’installation rationalisée.

L’expérience d’installation associée à la première utilisation du programme est connue sous le nom de première expérience. Votre programme doit fournir une première expérience rationalisée aux utilisateurs. Chaque question ou étape qui n’est pas nécessaire ou peut être ajournée les retarde de l’utilisation de votre programme. Les programmes d’installation trop complexes sont reliques à un âge différent.

**Remarque :** Les instructions relatives à la [première expérience](exper-first-exper.md) à l’aide d’un programme et d' [assistants](win-wizards.md) sont présentées dans des articles distincts.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

alors que tous les programmes Microsoft Windows ont besoin d’un programme d’installation, vous avez le choix entre l’emplacement des paramètres du programme :

-   Programme d’installation
-   Première utilisation du programme
-   Options de programme centralisées
-   Dans le contexte de l’utilisation de la fonctionnalité

**Paramétrage**

Présenter les paramètres dans le programme d’installation si :

-   Les paramètres corrects sont requis pour utiliser le programme et s’appliquent à tous les utilisateurs.
-   L’utilisation des paramètres par défaut n’est pas acceptable, soit parce qu’il n’existe pas de valeur par défaut sécurisée, les utilisateurs peuvent choisir des paramètres qui ne sont pas la valeur par défaut, ou les paramètres par défaut nécessitent le consentement de l’utilisateur.
-   Les utilisateurs doivent, mais ne sont pas susceptibles de modifier les paramètres importants après l’installation.

**Première utilisation du programme**

Présentez les paramètres de la première utilisation du programme dans les cas suivants :

-   Les paramètres corrects sont requis pour utiliser le programme et s’appliquent aux utilisateurs individuels.
-   L’utilisation des paramètres par défaut n’est pas acceptable, soit parce qu’il n’existe pas de valeur par défaut sécurisée, les utilisateurs peuvent choisir des paramètres qui ne sont pas la valeur par défaut, ou les paramètres par défaut nécessitent le consentement de l’utilisateur.
-   Les utilisateurs doivent, mais ne sont pas susceptibles de modifier des paramètres importants à l’aide des options du programme.
-   Les paramètres personnalisent une expérience de base ou un essentiel à l’identification personnelle d’un utilisateur avec le programme.

Pour ces paramètres, les utilisateurs sont susceptibles d’apporter de meilleurs choix dans le contexte du programme que dans le cadre de l’installation.

**Options de programme centralisées**

Présentez les paramètres de la [boîte de dialogue Options](win-property-win.md) du programme si toutes les conditions suivantes s’appliquent :

-   Il existe des paramètres par défaut qui fonctionnent bien pour la plupart des utilisateurs.
-   Il existe de nombreux paramètres et ils s’appliquent à l’ensemble des fonctionnalités et des tâches.
-   Les utilisateurs sont plus susceptibles de se attendre à trouver les paramètres dans un emplacement centralisé.

**Dans le contexte de l’utilisation de la fonctionnalité**

Présentez les paramètres dans le contexte approprié si toutes les conditions suivantes s’appliquent :

-   Il existe des paramètres par défaut qui fonctionnent bien pour la plupart des utilisateurs.
-   Il existe un petit nombre de paramètres autonomes pour une fonctionnalité spécifique.
-   Les utilisateurs sont plus susceptibles de s’attendre à trouver les paramètres avec la fonctionnalité associée qu’un emplacement centralisé.
-   L’interface utilisateur (IU) permet d’accéder aux paramètres de façon évidente.

En accordant une attention particulière à l’emplacement des paramètres de configuration, vous pouvez réduire la charge pesant sur les utilisateurs lors de leur première expérience avec votre programme.

## <a name="design-concepts"></a>Principes de conception

### <a name="design-a-lightweight-setup"></a>Concevoir une installation légère

Bienvenue, suivant, suivant, suivant, suivant, suivant, installer, terminer, félicitations ! Ce programme d’installation vous semble-t-il familier ? Historiquement, les programmes d’installation ont adopté ce type de conception inefficace : une longue séquence d’écrans, qui invite les utilisateurs à effectuer une séquence stupides de clics simplement pour l’utiliser.

Si les utilisateurs décrivent la configuration de votre programme avec des mots tels que rapide et simple, il est certainement louanges concernant certains de l’expérience. Ils préfèrent plutôt utiliser votre programme que de le configurer.

**Passez en revue la conception de votre configuration pour les questions, les options, les pages et les chemins d’accès non essentiels, et soyez Ruthless à les éliminer.** Effectuez des recherches utilisateur pour découvrir les options dont les utilisateurs ont vraiment besoin et assurez-vous qu’ils ne sont pas mindlessly en cliquant sur le bouton suivant dans toutes les pages. Reportez toutes les options ou questions qui sont mieux résolues dans le contexte du programme en cours d’exécution.

De nombreux programmes d’installation proposent des pages standard non, car ils sont nécessaires ou utiles, mais parce qu’ils sont standard. Par exemple, les pages d’accueil, les pages de résumé et les pages félicitations sont souvent des clics. Au lieu de cela, votre programme d’installation doit ajouter des pages uniquement s’ils sont nécessaires pour terminer la tâche d’installation. Pour obtenir des instructions sur les types de pages d’installation et leur évaluation, consultez [types de page](#page-types) plus loin dans cet article.

![capture d’écran de la première page du programme d’installation de ProClarity ](images/exper-setup-image2.png)

Dans cet exemple, le programme d’installation élimine la page d’accueil traditionnelle et passe directement à l’entreprise.

Même s’il peut être nécessaire d’offrir différentes branches de configuration (une expérience rapide, une expérience classique et une expérience plus contrôlable et personnalisée), assurez-vous que vous disposez de suffisamment d’options personnalisées pour justifier une complexité supplémentaire. N’ajoutez pas de branches, sauf si vous en avez besoin. Certaines options sans importance dans une branche personnalisée suggèrent la nécessité de réorganiser la conception de la configuration.

Une autre raison pour simplifier l’installation est que les utilisateurs inexpérimentés surveillent parfois les options, en craignant qu’un mauvais choix soit irréversible ou destructif. Le fait de forcer les utilisateurs à prendre des décisions sur les choses qu’ils ne comprennent pas ou ne se soucie pas peut les faire ressentir de manière soucieuse, non compétente et même frustré. Ce n’est pas une bonne impression. Il est préférable de les faire passer rapidement, de vous sentir à l’aise et de vous assurer qu’ils explorent les fonctionnalités de votre programme et de prendre de meilleures décisions concernant les options de fonctionnalités à ce moment-là. Pour plus d’instructions, consultez rationalisation de l' [installation](#streamlining-setup) plus loin dans cet article.

Efforcez-vous de rendre l’expérience d’installation aussi [simple que possible, mais pas plus simple](/previous-versions//dn742474(v=vs.85)). Les programmes destinés aux utilisateurs hautement techniques peuvent nécessiter une configuration complexe. par exemple, l’équipe de Microsoft SQL Server a découvert que les administrateurs de base de données préfèrent conserver le contrôle de nombreuses options d’installation, telles que les emplacements de fichiers. en outre, SQL Server est une application métier de grande taille, avec un certain nombre de composants qui diffèrent largement et en fonction des fonctionnalités. Donc, bien que nous souhaitons simplifier les choses, le programme d’installation doit refléter la complexité du produit et les attentes et les besoins de ses utilisateurs.

Toutefois, ces programmes d’installation complexes doivent être l’exception, et non la règle. la plupart des programmes Windows doivent s’efforcer de démarrer le processus d’installation en une seule étape.

### <a name="setup-phases"></a>Phases de configuration

Les programmes d’installation bien conçus permettent aux utilisateurs d’effectuer d’autres activités pendant la tâche fastidieuse de téléchargement et de copie des fichiers. Pour s’exécuter sans assistance, les programmes d’installation sont conçus pour comporter quatre phases distinctes :

-   **Phase de décision.** Les utilisateurs indiquent comment ils veulent installer et configurer le programme.
-   **Phase de téléchargement.** Pour les programmes téléchargés à partir d’Internet. Si le programme possède plusieurs applications ou versions, les utilisateurs indiquent ce qu’il faut télécharger au cours de la phase de décision.
-   **Phase d’installation.** Le programme d’installation copie les fichiers et effectue les modifications de configuration appropriées.
-   **Phase d’achèvement.** Les détails, les étapes ou les problèmes restants sont traités.

Étant donné que la phase d’installation peut prendre un certain temps, cette phase doit être conçue pour s’exécuter jusqu’à la fin sans intervention de l’utilisateur. Cela signifie que toutes les questions doivent être posées au cours de la phase de décision et que tous les problèmes qui se posent doivent être mis en file d’attente et traités lors de la phase d’achèvement. **Si la phase d’installation prend plus d’une minute, supposons que les utilisateurs effectuent d’autres opérations pendant les phases de téléchargement et d’installation.**

**Incorrect :**

![capture d’écran de l’installation automatique des rapports d’installation ? dialogue ](images/exper-setup-image3.png)

Dans cet exemple, le programme d’installation interrompt la progression pour poser une question qui devrait avoir été posée au cours de la phase de décision.

### <a name="present-helpful-progress"></a>Présenter la progression utile

Si les utilisateurs patientent au cours de la phase d’installation de l’expérience d’installation, en observant peut-être une barre de progression jusqu’à son achèvement apparent, uniquement pour assister la réinitialisation et le redémarrage de la barre de progression, il y a un vrai sens pour les bacs. La progression signalée était trompeuse et sans utilité.

L’une des variantes de ce scénario pénible est l’installation « brinksmanship » : les utilisateurs voient la portée de la progression, par exemple, à 99% de l’achèvement, qui sont encore obligés d’attendre un laps de temps disproportionné avant d’atteindre 100%. Par conséquent, en termes de ce qui est le plus important pour l’utilisateur, une promesse implicite sur le délai d’attente, la revendication de 99% effectuée est trompeuse.

Pendant les phases de téléchargement et d’installation, les utilisateurs ont généralement deux choses à savoir : ils doivent attendre ou faire autre chose, et le programme d’installation va être bientôt terminé. Bien qu’il y ait suffisamment de variables dans le processus d’installation pour vous empêcher de fournir des informations de progression parfaitement précises, les commentaires de progression doivent être suffisamment précis pour répondre à ces deux questions et définir les attentes appropriées. En plus d’une barre de progression, vous pouvez inclure une brève instruction sur le temps global attendu pour le processus.

![capture d’écran de la boîte de dialogue montrant la progression de l’installation ](images/exper-setup-image4.png)

Dans cet exemple, la page de progression contient une brève déclaration générale sur le temps nécessaire à l’installation.

Les bons programmes d’installation utilisent efficacement des barres de progression pour fournir aux utilisateurs des informations utiles sur la progression du programme d’installation. Pour plus d’instructions, consultez [barres de progression](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Conception pour tous les scénarios d’installation

Les programmes d’installation modernes doivent être conçus pour gérer un large éventail de scénarios d’installation :

-   L’utilisateur du programme l’installe à partir d’un disque ou d’un partage de fichiers réseau.
-   L’utilisateur du programme le télécharge à partir du Web.
-   Un fabricant OEM (Original Equipment Manufacturer) inclut le programme sur l’ordinateur en usine.
-   Un professionnel de l’informatique installe le programme sur un grand nombre d’ordinateurs au sein d’une organisation.
-   Une personne autre que l’utilisateur installe le programme (par exemple, un parent pour le compte d’un enfant ou un collègue qui utilise le même ordinateur qu’un autre collègue).

Étant donné ces scénarios, vous ne devez pas supposer que les utilisateurs installent toujours le programme pour eux-mêmes (en rendant les options personnalisées inappropriées), en surveillant le processus en détail (ce qui fait que l’installation sans assistance est importante) ou même qu’une interface utilisateur graphique pour la tâche.

### <a name="dont-forget-the-uninstall-experience"></a>N’oubliez pas l’expérience de désinstallation

Pour terminer le cycle de vie de l’installation du logiciel, les utilisateurs doivent être en mesure de supprimer les logiciels qu’ils ne souhaitent pas ou dont ils n’ont plus besoin. Cela est particulièrement important s’ils n’ont pas installé le programme proprement dit (par exemple, s’il est déjà chargé sur l’ordinateur).

### <a name="handle-technical-support-strategically"></a>Gérez le support technique de manière stratégique

L’installation de votre programme est l’une des tâches que tous les utilisateurs doivent effectuer avec succès. Si les utilisateurs ne parviennent pas à installer votre programme, vous devez leur fournir un support technique coûteux ou ils ne sont plus vos utilisateurs.

Concevez votre programme d’installation pour fournir à votre équipe de support technique les fonctionnalités et les informations dont elles ont besoin pour aider les utilisateurs à s’installer correctement. En règle générale, ces informations ne doivent pas être exposées aux utilisateurs, mais elles doivent être facilement accessibles en cas de besoin.

**Incorrect :**

![capture d’écran de l’étiquette montrant le nom du serveur com ](images/exper-setup-image5.png)

Dans cet exemple, la barre de progression présente des détails qui ne sont significatifs que pour le support technique.

Conservez l’expérience utilisateur simple, ne l’encombrez pas avec des informations qui n’ont qu’une valeur pour le support technique. Enregistrez plutôt les informations de prise en charge dans un fichier journal d’installation. Et plus important encore, aidez les utilisateurs à éviter le besoin de support technique avec des messages d’erreur clairs et concis qui décrivent les problèmes et fournissent des solutions pratiques. Fournissez des liens vers des articles d’aide si nécessaire. Envisagez de fournir une option de réparation à votre programme d’installation pour réparer des fichiers ou des paramètres manquants ou endommagés.

**Si vous ne faites que trois choses...**

1.  1. Rendez le programme d’installation aussi simple et léger que possible. N’oubliez pas que les utilisateurs ne bénéficient pas de la configuration. Examinez attentivement chaque question, option, page et chemin d’accès, et supprimez tout ce qui n’est pas essentiel pour terminer l’installation.
2.  2. Conception pour tous les scénarios d’installation, y compris les installations sans assistance, les installations par script et la désinstallation. Pour les installations sans assistance efficaces, assurez-vous qu’il existe une séparation nette entre les phases d’installation.
3.  3. Concevez votre programme d’installation afin que les utilisateurs puissent résoudre eux-mêmes les problèmes d’installation, mais également consigner les informations nécessaires pour le support technique, le cas échéant. Gardez à l’esprit que le programme d’installation est l’une des tâches que tous les utilisateurs doivent effectuer avec succès.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   **Appliquez les instructions standard de l’Assistant pour les programmes d’installation basés sur des assistants.** Utilisez ces instructions pour déterminer une bonne conception de page, une navigation efficace, des étiquettes de contrôle correctes, l’utilisation d’instructions principales et l’utilisation de l’aide.
-   **Autorisez les utilisateurs à redémarrer le programme d’installation là où ils se sont arrêtés s’ils ont besoin d’une grande quantité d’entrées utilisateur ou qu’ils mettent beaucoup de temps à se terminer.** Si les utilisateurs redémarrent le programme après l’avoir fermé avant l’achèvement, restaurez l’entrée d’utilisateur précédente et redémarrez l’emplacement d’arrêt de l’installation.
-   **N’affiche pas les fenêtres d’installation optimisées.** L’affichage d’une fenêtre d’installation agrandie suppose que les utilisateurs feront une attention non divisée, ce qui est peu probable. Au lieu de cela, choisissez une taille appropriée au contenu pour conserver une apparence simple.

### <a name="windows-integration"></a>intégration de Windows

-   **Nommez le fichier d’installation « Setup.exe ».** « Install.exe » est une alternative acceptable. cela permet à Windows (et aux utilisateurs) de reconnaître le fichier en tant que programme d’installation.
    -   **Exception :** Pour les programmes téléchargés à partir d’Internet, aidez les utilisateurs à gérer et à organiser leur dossier téléchargements en incluant le nom du programme dans le nom du fichier d’installation. Par exemple, SetupVisualStudioExpress2008.exe.
-   **Copiez les fichiers programme vers les emplacements de système de fichiers appropriés.** cela permet aux utilisateurs et aux Windows de rechercher et d’organiser les fichiers mieux. pour plus d’informations, consultez les instructions d’utilisation de l' [espace de noms du système de fichiers Windows](../fileio/naming-a-file.md#namespaces).

### <a name="user-account-control"></a>Contrôle de compte d'utilisateur

-   **Signez numériquement le fichier exécutable d’installation.** Les exécutables signés présentent de nombreux avantages, notamment l’utilisation d’une interface utilisateur d’élévation de contrôle de compte d’utilisateur plus spécifique. Pour plus d’informations sur la signature des fichiers, consultez [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).
-   **Si une installation peut nécessiter une élévation, élever le plus tard possible.** Affichez l’interface utilisateur d’élévation uniquement une fois que l’utilisateur s’est engagé à une option qui requiert une élévation. En règle générale, l’interface utilisateur d’élévation s’affiche pendant la phase d’installation, et non la phase de décision. Toutefois, si un programme d’installation requiert toujours une élévation, élever son point d’entrée.
-   **Nécessite toujours une élévation pour la désinstallation.** Cela empêche les logiciels malveillants de désinstaller les logiciels critiques sans que les utilisateurs ne les sachent.
-   **Une fois élevé, restez élevé jusqu’à ce que les privilèges élevés ne soient plus nécessaires.** Les utilisateurs ne doivent pas avoir à élever plusieurs fois pour effectuer une installation de programme complète.
-   **Si des privilèges spéciaux sont requis pour l’installation, vérifiez les informations d’identification de l’utilisateur et signalez les problèmes éventuels sur la première ou la deuxième page.** N’autorisez pas les utilisateurs à effectuer beaucoup de travail uniquement pour déterminer qu’ils n’ont pas les bonnes informations d’identification pour terminer l’installation.
-   **Exiger le moins de privilèges possible.** Par exemple, les administrateurs hésitent à installer des logiciels qui nécessitent des informations d’identification d’administrateur de domaine.

Pour plus d’instructions, consultez [contrôle de compte d’utilisateur](winenv-uac.md).

### <a name="restarting-windows"></a>Redémarrage de Windows

-   **Évitez de redémarrer Windows.** La plupart des programmes doivent s’installer sans redémarrer Windows. La raison principale pour laquelle les installations ou les mises à jour du programme nécessitent un redémarrage du système est que certains des fichiers impliqués sont actuellement utilisés par un programme en cours d’exécution. Dans ce cas, une meilleure solution consiste à rendre les utilisateurs informés de la situation, à autoriser les utilisateurs à fermer ces programmes et à réessayer l’action. Pour plus d’informations sur l’évitement des redémarrages, consultez [restart Manager](../rstmgr/restart-manager-portal.md).
-   **Si votre programme d’installation doit redémarrer Windows :**
    -   **Utilisez un redémarrage unique.** Retardez le redémarrage requis par les conditions préalables jusqu’à ce que le programme et ses mises à jour soient entièrement installés.
    -   **Permet aux utilisateurs de déterminer quand ils se produisent.** ne redémarrez pas Windows automatiquement, car les utilisateurs risquent de perdre leur travail. Assurez-vous qu’il est clair pour les utilisateurs qu’ils ont le choix.

        **Incorrect :**

        ![capture d’écran de la boîte de dialogue avec restart and Cancel ](images/exper-setup-image6.png)

        Dans cet exemple, les utilisateurs n’ont pas la possibilité de redémarrer Windows.

    -   **si l’utilisateur choisit de ne pas redémarrer Windows immédiatement, présentez tous les commentaires finaux en cas de réussite, et non pas un échec.** Bien que l’installation ne soit pas terminée tant que le redémarrage n’est pas effectué, le point de vue de l’utilisateur a été correctement effectué.

### <a name="streamlining-setup"></a>Rationalisation de la configuration

-   **Chaque fois que cela est possible, démarrez le processus d’installation en une seule étape.** Par exemple, au lieu d’ajouter une page distincte dans le programme d’installation pour les termes du contrat de licence, vous pouvez lui fournir un lien à la place. Si vous êtes lié aux termes :
    -   Phrase le bouton valider « accepter et installer » pour exiger le consentement explicite pour accepter les termes du contrat de licence.
    -   Assurez-vous que le lien du contrat de licence ne peut pas être rompu en établissant un lien vers un fichier local au programme d’installation au lieu d’une page Web.
    -   Permet d’imprimer le contrat de licence à partir de sa fenêtre d’affichage.
-   **Éliminez les options et les questions inutiles.**
    -   Différer les options qui conviennent à la première utilisation du programme ou de la fonctionnalité.

        ![capture d’écran de l’option paramètres personnalisés ](images/exper-setup-image7.png)

        dans cet exemple, Lecteur Windows Media présente des options de confidentialité par utilisateur lors de la première utilisation du programme.

    -   Ne posez pas des questions aux utilisateurs sur l’état du système. Détectez ces informations automatiquement à la place et demandez aux utilisateurs de vérifier uniquement s’il existe une raison de modification.
    -   Ne posez pas de questions sur les détails non importants. par exemple, pour les programmes de Windows standard, il est possible de supposer que vous devez copier les fichiers programme dans le dossier program files.

        **Incorrect :**

        ![capture d’écran de la boîte de dialogue avec emplacement d’installation ](images/exper-setup-image8.png)

        Dans cet exemple, le programme d’installation doit être rationalisé en éliminant la demande d’entrée d’emplacement de fichier. Étant donné la taille du programme, la plupart des utilisateurs ne se soucient pas et cliquent simplement sur suivant.

    -   Ne demandez pas l’autorisation de faire ce que vous ne devriez pas faire de toute façon. Par exemple, la plupart des programmes ne doivent pas inclure une option permettant de placer l’icône du programme sur le bureau.
    -   Ne confirmez pas l’annulation de l’installation. Si les utilisateurs cliquent sur Annuler pendant l’installation, supposez que l’annulation était intentionnelle et fermez le programme sans confirmation. Si cela risque de perdre du temps ou des efforts significatifs, autorisez les utilisateurs à redémarrer votre programme d’installation et à reprendre là où ils se sont arrêtés.

-   **Optimiser pour une installation sans assistance.**
    -   Présentez toutes les options et toutes les questions au cours de la phase de décision.
    -   Pour les phases de téléchargement et d’installation, Retardez la saisie de l’utilisateur pour les problèmes rencontrés jusqu’à la fin de la phase. En procédant ainsi, les utilisateurs peuvent conserver l’installation sans assistance jusqu’à ce qu’ils retournent à leur convenance.
-   **Éliminez les pages inutiles.** Si la plupart des utilisateurs cliquent toujours sur la page suivante, pensez à vous débarrasser de la page. Pour obtenir des instructions sur l’élimination de certains types de pages, consultez [types de page](#page-types).
-   **Éliminez le texte inutile.**
    -   Supprimez le texte redondant des instructions et des étiquettes.
    -   n’expliquez pas les concepts de base de l’utilisation de Windows, tels que :
        -   Comment interagir avec les contrôles (exemples : pour commencer, cliquez sur suivant ; Pour plus d’options, cliquez sur options. Pour plus d’informations, cliquez sur aide).
        -   Fonctionnement des assistants (exemple : Si vous souhaitez vérifier ou modifier des paramètres, cliquez sur précédent).
        -   Fonctionnement du programme d’installation (exemple : ce programme copie les fichiers programme sur votre disque dur...).
-   **Éliminez les efforts inutiles.**
    -   Fournissez les valeurs par défaut correctes :
        -   En règle générale, sélectionnez la réponse la plus sécurisée et la plus privée par défaut.
        -   Si la sécurité et la confidentialité ne sont pas des facteurs, sélectionnez la réponse la plus probable ou la plus pratique.

            ![capture d’écran de la boîte de dialogue avec le nom et la société affichés ](images/exper-setup-image9.png)

            Dans cet exemple, le nom d’utilisateur et l’organisation fournis par défaut sont obtenus à partir du Registre.

        -   Si une option est fortement recommandée, vous pouvez la sélectionner par défaut ou ajouter « (recommandé) » à son étiquette.

    -   Avancer automatiquement les pages quand une page n’a aucune entrée et que la tâche est effectuée avec succès, par exemple avec les pages de téléchargement, d’installation, de progression et de mise à jour. Une fois l’étape terminée, restez sur ces pages uniquement pour afficher les problèmes.
    -   Quand cela est possible, démarrez le programme automatiquement une fois l’installation terminée, au lieu d’ouvrir une page de félicitations ou de fin. Lorsque l’installation est exécutée de manière interactive, supposons que l’utilisateur installe votre programme afin de l’exécuter immédiatement. l’exécution du programme est donc le meilleur commentaire pour montrer que l’installation est terminée. L’exécution automatique du programme n’est pas pratique quand le programme d’installation de installe plusieurs programmes (par exemple, une suite composée de nombreux programmes), lorsque l’installation n’est pas exécutée de manière interactive ou lorsque le processus d’installation n’est pas terminé après l’installation.

### <a name="page-types"></a>Types de pages

**Pages d’accueil et de Prise en main**

-   **Éliminez les pages d’accueil.** Bien qu’il soit très utile de le faire, les utilisateurs cliquent généralement sur suivant sans lire. En outre, étant donné que les utilisateurs ignorent ces pages sans les lire, le texte n’a guère plus d’État évident, de par sa conception.

    **Incorrect :**

    ![capture d’écran de l’écran d’accueil avec Next et Cancel ](images/exper-setup-image10.png)

    Dans cet exemple, il n’y a rien à faire pour l’utilisateur, mais je clique sur suivant.

-   **Utilisez une page de Prise en main uniquement si vous devez informer les utilisateurs de la configuration requise pour l’installation de.** Ces conditions préalables incluent l’installation d’un logiciel ou d’un matériel requis, l’exécution de modifications de configuration système requises et de mises à jour, l’exécution d’une sauvegarde du système pour se protéger contre la perte de données ou l’obtention des informations requises que l’utilisateur n’a probablement pas déjà.
-   **Dans la mesure du possible, fournissez la possibilité d’effectuer les conditions préalables directement à partir du programme d’installation.** Les utilisateurs doivent avoir à exécuter les étapes manuellement uniquement s’il n’existe pas d’alternative.
-   Si une page d’accueil ou une page de Prise en main n’est pas utilisée, **incluez le nom et la description du programme sur la première page du programme d’installation.** Vous pouvez utiliser la langue d’accueil comme texte d’introduction, à condition que l’objectif de la page soit clair.

**Pages termes du contrat de licence**

-   **Écrivez les termes du contrat de licence à l’aide de texte clair et concis.** Utilisez un langage simple. Évitez « conditions ».
-   **Présente un format facile à lire et à analyser.** N’utilisez pas de longs passages de texte en majuscules.

    **Incorrect :**

    ![capture d’écran des termes du contrat de licence en majuscules ](images/exper-setup-image11.png)

    Dans cet exemple, le texte en majuscules et la grande taille de police rendent les termes difficiles à lire, ce qui oblige les utilisateurs à faire défiler plus que nécessaire.

-   **Exiger un consentement explicite pour accepter les termes du contrat de licence.** L’acceptation de la licence ne doit jamais être sélectionnée par défaut. Si des cases d’option sont utilisées pour indiquer l’acceptation, laissez les options désactivées par défaut et demandez aux utilisateurs d’accepter les conditions préalables avant d’activer le bouton suivant.

    ![capture d’écran de la boîte de dialogue avec le bouton suivant grisé ](images/exper-setup-image12.png)

    Dans cet exemple, le bouton suivant est désactivé jusqu’à ce que les utilisateurs aient explicitement accepté les termes du contrat de licence.

-   **Ne demandez pas aux utilisateurs de faire défiler le texte des termes du contrat de licence avant d’activer le bouton suivant.** Cela impose aux utilisateurs une charge inutile pour comprendre pourquoi le bouton suivant est désactivé.
-   **Fournissez une commande d’impression,** à l’aide d’un bouton de commande ou d’un menu contextuel. Présentez les termes dans un format optimisé pour l’impression.

**Pages d’inscription du produit**

-   **Obligez les utilisateurs à s’inscrire uniquement s’ils doivent utiliser le programme.** Expliquez clairement pourquoi les utilisateurs doivent s’inscrire.
-   **Fournissez l’inscription facultative uniquement s’il existe un avantage évident pour l’utilisateur,** par exemple pour avertir les utilisateurs des mises à jour du produit. Laissez cette option désactivée par défaut.
-   **Autoriser les utilisateurs à s’inscrire ultérieurement.** Fournissez un maximum de trois rappels et autorisez les utilisateurs à ignorer les rappels en un seul clic.

**Pages d’étendue (standard, personnalisée ou minimale)**

-   **Préférez supprimer cette page.** Supposons que la plupart des utilisateurs veulent une expérience d’installation par défaut (et qu’ils conçoivent cette expérience pour qu’ils fonctionnent bien pour la plupart des utilisateurs).
-   Si vous devez inclure une page d’étendue :
    -   **Expliquez les différences entre les options en termes de fonctionnalités et d’espace disque.** Les utilisateurs s’appuient sur la clarté des informations de la page étendue pour s’assurer qu’ils font le bon choix.
    -   **Assurez-vous que les options personnalisées sont nécessaires uniquement pour un petit pourcentage d’utilisateurs, tandis que la plupart des utilisateurs peuvent les ignorer en toute sécurité.** Si ce n’est pas le cas, les options doivent être dans le chemin d’installation par défaut.
    -   **Si les utilisateurs choisissent des options personnalisées, les options d’installation standard sont sélectionnées par défaut.** Les utilisateurs considèrent l’installation par défaut comme la ligne de base et souhaitent personnaliser en ajoutant ou en supprimant des options de cette ligne de base.
-   Si vous devez utiliser une option d’installation personnalisée, **envisagez d’utiliser le dimensionnement et le positionnement du bouton relatif pour guider la plupart des utilisateurs vers l’installation par défaut.**

    ![capture d’écran de la boîte de dialogue avec un grand bouton installer ](images/exper-setup-image13.png)

    Dans cet exemple, la conception de la page renforce visuellement le fait que la plupart des utilisateurs doivent s’abonner à l’installation par défaut.

**Pages d’entrée**

-   **Réduisez le nombre d’options d’installation par défaut.** Pour plus d’options, consultez [rationalisation](#streamlining-setup)de l’installation.
-   **Fournissez des valeurs par défaut acceptables dans la mesure du possible.** Choisissez les valeurs par défaut qui sont sécurisées et privées, et qui sont acceptables pour la plupart des utilisateurs sans modification.
-   **À moins que votre programme n’ait des exigences inhabituelles, efforcez-vous de disposer d’une seule page de questions et d’options.** Toutefois, si votre programme nécessite plusieurs pages de questions et d’options, affichez-les dans le déroulement de la page principale de l’Assistant. N’essayez pas de réduire le nombre de pages techniquement en plaçant des options dans des boîtes de dialogue ou en utilisant des onglets.
-   ![capture d’écran de la boîte de dialogue de configuration avec quatre options ](images/exper-setup-image14.png)
-   Dans cet exemple, les options sont limitées à une seule page.
-   **Valider l’entrée dès que possible :**
    -   Interdit les caractères non valides à l’entrée.
    -   Utilisez des [bulles](ctrl-balloons.md) pour signaler des problèmes avec des zones de texte non valides.
    -   Valider les champs associés sur une page lorsque les utilisateurs cliquent sur suivant.
    -   Validez les champs associés dans les pages d’entrée dès que des problèmes peuvent être détectés.
-   **Donnez à tous les chemins d’accès aux fichiers modifiables un bouton Parcourir.** Autorisez les utilisateurs à spécifier des chemins d’accès réseau.
-   **Pour la page d’entrée finale, étiquetez le bouton de validation installer, et non suivant.** Les utilisateurs ne doivent pas être surpris par le moment où l’installation démarre. Avant le point de validation, assurez-vous que les utilisateurs peuvent facilement modifier les paramètres.

**Pages de démarrage de l’installation**

-   **Éliminez cette page si elle n’a pas d’autre fonction que de résumer les choix précédents et de commencer l’installation.** Si les pages d’entrée sont claires et peu nombreuses, il ne devrait pas être nécessaire de les résumer. Au lieu de cela, la page d’entrée finale doit comporter le bouton installer, qui mène directement à la page progression.
-   **Pour les installations complexes destinées aux professionnels de l’informatique, indiquez une page d’installation avec une liste complète des modifications effectuées par le programme d’installation.** De nombreux professionnels de l’informatique disposent d’un contrôle strict sur la gestion des changements. ils doivent donc connaître l’impact de l’installation du programme.

**Pages de progression**

-   **Fournissez toujours une page de progression,** même si le programme s’installe rapidement. Fournissez une page de progression distincte pour [la phase de téléchargement, le](#setup-phases) cas échéant. Désactivez les boutons précédent (ou précédent) et suivant pendant que l’installation est en cours, mais laissez le bouton Annuler activé et réactif.

    ![capture d’écran de la boîte de dialogue avec la barre de progression ](images/exper-setup-image15.png)

    Page de progression classique.

-   **Utilisez une barre de progression unique et arrêtée.** Suivez les [instructions relatives à la barre de progression déterminées](progress-bars.md), notamment :
    -   Indiquez clairement la fin de l’opération. Ne laissez pas une barre de progression aller à 100%, sauf si l’opération est terminée.
    -   Ne pas redémarrer la progression. Une barre de progression perd sa valeur si elle redémarre (peut-être parce qu’une étape de l’opération se termine), car les utilisateurs n’ont aucun moyen de savoir à quel moment l’opération se termine. Au lieu de cela, vous devez faire en sorte que toutes les étapes de l’opération partagent une partie de la progression et que la barre de progression passe à l’achèvement une fois.
-   **Fournissez une description concise de l’étape actuelle au-dessus de la barre de progression.** Pour les installations rapides, un tel texte est inutile. la barre de progression seule est suffisante. Pour les installations nécessitant une minute ou plus, le texte peut être utile pour les utilisateurs qui assistent à la configuration.
    -   **Utilisez des fragments de phrase, qui commencent généralement par un verbe, et se terminent par des points de suspension.** Exemples : copie de fichiers..., installation des composants requis...
    -   **Placez le texte au-dessus de la barre, et non ci-dessous.**

        **Incorrect :**

        ![capture d’écran du texte affiché sous la barre de progression ](images/exper-setup-image16.png)

        Dans cet exemple, le texte explicatif doit apparaître au-dessus de la barre de progression.

    -   **Évitez d’encombrer la page de progression avec des détails inutiles.** Cette page n’est pas destinée au [support technique](#handle-technical-support-strategically). il n’est donc pas nécessaire d’afficher les GUID d’inscription ou les fichiers spécifiques copiés.

        **Incorrect :**

        ![capture d’écran du GUID affichée sur la barre de progression ](images/exper-setup-image17.png)

        Dans cet exemple, les détails techniques, tels que les GUID, ne sont pas compréhensibles pour les utilisateurs.

**Pages d’erreur**

-   **Si le programme d’installation échoue avec un problème important, affichez une page d’erreur qui explique les problèmes, ainsi que les étapes pratiques à suivre pour les résoudre.** Affichez la page avec une icône d’erreur. N’utilisez pas de boîte de dialogue à cet effet.

    ![capture d’écran de la page et de l’icône d’erreur ](images/exper-setup-image18.png)

    Dans cet exemple, l’échec du programme d’installation est expliqué sur une page d’erreur, ainsi que certaines étapes pour résoudre le problème.

-   **Si le programme d’installation se termine avec un problème récupérable mineur, présentez le problème en tant que tâche supplémentaire au lieu d’une erreur.** Utilisez un langage positif, orienté réussite et encourageant, et non des termes tels que l’erreur, l’échec ou le problème. N’utilisez pas d’icône d’erreur.

**Félicitations/pages de fin**

-   **Lorsque vous installez un seul programme de manière interactive, démarrez le programme (et fermez l’Assistant Installation) pour indiquer la réussite de l’installation, au lieu d’afficher une page de fin. Exceptions**
    -   Les configurations exécutées à partir de la ligne de commande ne doivent pas démarrer de programmes.
    -   les mises à jour automatiques (par exemple, Windows Update) ne doivent pas démarrer de programmes.
    -   L’installation de la stratégie de groupe ne doit pas démarrer les programmes.
    -   Tous les scénarios d’installation professionnels de l’informatique (parce qu’ils n’installent pas pour leur propre usage).
-   **Si le programme d’installation a effectué des étapes de suivi après l’installation, répertoriez-les sur une page d’achèvement.** Toutefois, pour justifier une page d’achèvement, assurez-vous que les utilisateurs sont susceptibles d’effectuer les étapes et que les étapes doivent être formulées de manière réelle (c’est-à-dire qu’elles ne sont pas évidentes).

    **Incorrect :**

    ![capture d’écran de la page montrant que l’installation est terminée ](images/exper-setup-image19.png)

    Dans cet exemple, une page de saisie semi-automatique inutile indique la évidente. Windows La mise à jour s’exécute automatiquement, de sorte que les utilisateurs n’ont aucune raison de l’exécuter manuellement.

-   **Lors de l’installation d’une suite de programmes, affichez une page de fin pour indiquer la réussite et les étapes de suivi qui peuvent être nécessaires.**

    ![capture d’écran de la dernière page du programme d’installation de la suite Office ](images/exper-setup-image20.png)

    Dans cet exemple, le programme d’installation a installé plusieurs programmes. il n’est donc pas judicieux de démarrer un programme spécifique automatiquement. Une page de saisie semi-automatique est plus appropriée.

### <a name="leaving-users-in-control"></a>Laisser les utilisateurs dans le contrôle

-   **Ne collectez pas d’informations personnelles, telles que celles utilisées à des fins de marketing.** Le programme d’installation ne permet pas de pousser votre propre agenda, de vendre plusieurs autres offres de programmes ou d’effectuer des recherches sur le marché. vous pouvez endommager la relation d’approbation avec vos utilisateurs de cette façon.
-   **Ne forcez pas les utilisateurs à refuser l’installation des fonctionnalités facultatives.** Autorisez- [le à la place.](glossary.md) par exemple, les utilisateurs doivent choisir explicitement d’installer un Gadget Windows Desktop.
-   **Autorisez les utilisateurs à ajouter ou supprimer des fonctionnalités facultatives à l’aide du programme d’installation après l’installation initiale.** Les utilisateurs peuvent effectuer cette tâche à l’aide de l’élément **désinstaller ou modifier un programme** du panneau de configuration.
-   **Pour les initiatives d’amélioration de l’expérience utilisateur, expliquez quelles sont les données transmises, comment elles sont utilisées et combien de temps elles sont conservées.** Utilisez un lien vers une rubrique d’aide relative à la déclaration de confidentialité à cet effet.
-   **Évitez d’utiliser le son,** car de nombreux scénarios d’installation sont sans assistance et, car le son peut être inutilement gênant, même pendant les installations avec assistance.

### <a name="security"></a>Sécurité

-   **Pour une configuration basée sur Internet, fournissez toutes les mises à jour de sécurité automatiquement lors de la configuration initiale.** Les utilisateurs ne doivent pas avoir à effectuer une mise à jour en tant qu’étape distincte.
-   **Évitez de recommander que les utilisateurs désactivent les pare-feu comme condition préalable à l’installation de votre programme.**
-   Si un pare-feu doit être désactivé, procédez comme suit :
    -   **Limitez la durée de cette condition à l’heure la plus brève possible.**
    -   **Indiquez explicitement quand les utilisateurs peuvent réactiver le pare-feu.**

### <a name="uninstall"></a>Désinstaller l’interface

-   **La désinstallation doit supprimer toutes les traces d’un programme, y compris les éléments suivants :**
    -   Fichiers programme, y compris le programme d’installation.
    -   entrées de menu Démarrer.
    -   Icônes de bureau et icônes de lancement rapide (le cas échéant).
    -   Paramètres de registre.
    -   Associations de fichiers.
-   **La désinstallation doit être laissée derrière les éléments suivants :**
    -   Les fichiers créés par l’utilisateur, tels que les fichiers de document.
    -   Bibliothèques de liens dynamiques partagées stockées dans le dossier système.

### <a name="help-and-support"></a>Aide et support

-   **Concevez votre programme d’installation pour ne pas avoir besoin d’aide en posant des questions claires et explicites.** Réservez de l’aide pour les questions avancées qui tirent vraiment parti d’explications supplémentaires.
-   **N’utilisez pas de fichiers Lisez-moi.** Ces fichiers sont désormais obsolètes et les utilisateurs ne les lisent pas quand même. Au lieu de cela, fournissez du contenu en ligne si nécessaire.
-   **Lien vers les rubriques d’aide appropriées ou résolution des problèmes liés aux messages d’erreur d’installation.** Assurez-vous que le contenu d’aide fournit un chemin d’accès clair pour résoudre le problème. Pour plus d’informations, consultez [messages d’erreur](mess-error.md).
-   **Créer des fichiers journaux pour capturer des informations utiles au support technique.** N’encombrez pas l’interface utilisateur du programme d’installation avec des détails liés au support technique qui n’ont pas de sens pour la plupart des utilisateurs. Utilisez à la place les fichiers journaux à cet effet.

### <a name="text"></a>Texte

-   **Soyez concis.** Les assistants d’installation décrivent souvent les fonctionnalités et les options, à l’aide de blocs de texte difficiles à analyser rapidement. **Exceptions :**
    -   Épelez tous les acronymes. Le programme d’installation est souvent la première expérience des utilisateurs avec votre programme, donc ne supposez pas qu’ils comprennent le jargon comme les acronymes.
    -   Décrivez la terminologie et les concepts inconnus, de préférence en place, mais en utilisant les rubriques d’aide si nécessaire.
-   **Préférer un ton convivial et professionnel ; Évitez les tonalités trop techniques.**

**Incorrect :**

Limitez l’installation par utilisateur.

**Correct :**

Installer uniquement pour moi.

-   N’utilisez pas maintenant dans les étiquettes de bouton de commande car le caractère immédiat de la commande peut être pris pour l’autorisation.
    -   **Exception :** Si nécessaire, utilisez-les maintenant pour différencier les commandes qui démarrent une tâche des commandes qui exécutent immédiatement une tâche.

![capture d’écran du bouton Télécharger ](images/exper-setup-image21.png)

Dans cet exemple, le fait de cliquer sur le bouton de commande permet d’accéder à une fenêtre ou une page qui permet aux utilisateurs de télécharger.

![capture d’écran du bouton Télécharger maintenant ](images/exper-setup-image22.png)

Dans cet exemple, le fait de cliquer sur le bouton de commande effectue le téléchargement immédiatement.

Une seule commande dans un workflow de tâches doit être étiquetée avec maintenant. Ainsi, par exemple, une commande **Download Now** ne doit jamais être suivie d’une autre commande **Download Now** .

-   Utilisez les termes du contrat de licence, non le contrat de licence, contrat de licence, contrat de licence utilisateur final ou CLUF.

Pour plus d’instructions, consultez [style et Tone](text-style-tone.md).

## <a name="documentation"></a>Documentation

-   En tant que verbe, la configuration est constituée de deux mots ; comme un adjectif ou un substantif, le programme d’installation est un mot.
-   Le programme d’installation est en majuscules et n’est pas coupé.
-   Utilisez installer pour faire référence à l’ajout de matériel ou logiciel à un système informatique.
-   N’utilisez pas installer comme nom. Utilisez plutôt l’installation.
-   Utilisez Restart, not reboot. Indique qu’il s’agit de l’ordinateur, et non d’un programme, qui redémarre.

 

 