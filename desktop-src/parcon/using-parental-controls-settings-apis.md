---
description: Utilisation des API de paramètres de contrôle parental
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Utilisation des API de paramètres de contrôle parental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dde4827dfe3ed5ee7eec6787744e6ff92f18775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757755"
---
# <a name="using-parental-controls-settings-apis"></a>Utilisation des API de paramètres de contrôle parental

Les paramètres sont traités avant la journalisation, car la journalisation est conditionnelle sur les paramètres de l’utilisateur.

## <a name="wmi-api-settings-writeread"></a>Paramètres d’API WMI en écriture/lecture

L’API WMI fournit un accès non abstrait (brut) à tous les paramètres instanciés par l’infrastructure de contrôle parental telle que définie dans le fichier de schéma Wpcsprov. mof. Le magasin de paramètres existe dans \\ l' \\ espace de noms WindowsParentalControls de l’application cimv2 racine \\ \\ , avec les définitions de classe suivantes qui définissent un schéma. Les éléments d’extensibilité sont notés.

Par ordinateur :

-   WpcSystemSettings (une instance)
    -   Les méthodes AddUser () et RemoveUser () pour créer et supprimer des paramètres de contrôle parental pour un SID donné, respectivement.
    -   Les propriétés du système actuel de classification des jeux en vigueur, ainsi que le suivi et la notification liés à la vérification des journaux par l’administrateur.
    -   Extensibilité : propriétés des listes d’exemption d’URL et d’application HTTP en lecture seule et en lecture/écriture pour le filtrage de contenu Web, l’ID de remplacement de filtre de contenu Web et le chemin d’accès et l’ID de DLL de ressource de nom, ainsi que le nombre d’événements de journal personnalisé et l’inscription de noms d’en-tête.
-   WpcRatingsSystem (une instance pour chaque système de classification installé)
    -   WpcRating (une instance par niveau de classification).
    -   WpcRatingDescriptor (une instance par descripteur d’évaluation).
-   Extensibilité : WpcExtension (une instance pour chaque lien d’extensibilité du panneau de contrôle parental ajouté).
    -   Propriétés du GUID, du sous-système, de l’ID, du chemin d’accès à la ressource d’image, du chemin d’accès de ressource d’image d’état désactivé, du chemin d’accès de l’exécutable, du nom complet DLL et de l’ID du chemin d’accès et de l’ID

Utilisateur par contrôle :

-   WpcUserSettings (une instance par utilisateur contrôlé)
    -   Propriétés du SID propriétaire, de l’indicateur de contrôle parental activé/désactivé, de l’indicateur d’ouverture/de désactivation, du délai d’activation/désactivation de l’indicateur, du remplacement de l’indicateur activé, du masque des heures d’ouverture de session et de l’indicateur d’activation/désactivation des restrictions d’application générales.
    -   Dans Windows 8, la propriété existante représente la première demi-heure pour chaque heure. Une nouvelle propriété de demi-heure a été ajoutée pour représenter la seconde moitié de chaque heure. Une nouvelle propriété supplémentaire a été introduite pour représenter le délai quotidien.

        **Windows 7 et Windows Vista :** Restrictions de minuterie prises en charge 1 heure.

-   WpcWebSettings (une instance par utilisateur contrôlé)
    -   Propriétés du SID propriétaire, de l’indicateur de filtre activé/désactivé, du niveau de filtre, de l’indicateur de téléchargement des fichiers bloqués, indicateur de sites bloqués non évalués.
-   WpcUrlOverride (une instance par URL explicitement autorisée ou refusée dans la liste de remplacement d’URL utilisée comme liste verte/rouge pour le filtrage de contenu Web)
    -   Propriétés du SID propriétaire, de l’URL affectée, de l’état autorisé/bloqué.
-   WpcAppOverride (une instance par chemin d’accès explicitement autorisée dans la liste des remplacements d’application des restrictions d’application générales)
    -   Propriétés du SID propriétaire. ID de règle plus SÉCURISÉe, chemin d’accès à l’application.
-   WpcGamesSettings (une instance par utilisateur contrôlé)
    -   Propriétés du SID propriétaire, indicateur des jeux autorisé, GUID du système de contrôle d’accès pour ces paramètres, autoriser les jeux non classés, ID de l’évaluation maximale autorisée sous système actuel, collection de descripteurs refusés.
-   WpcGameOverride (une instance par ID d’application explicitement autorisée ou refusée)
    -   Propriétés du SID propriétaire, ID d’application identifiant le jeu, état autorisé/refusé.

## <a name="data-representation-notes"></a>Remarques sur la représentation des données

Plusieurs des paramètres dans le schéma sont limités par le fichier. mof avec l’attribut non \_ null. Ils ne peuvent pas être définis sur un variant null. Pour tous les types autres que les types tableau, le code de contrôle parental initialise les valeurs. Pour les tableaux, les États vides peuvent être écrits à l’aide d’une variante null, d’une variante vide ou d’un tableau de variants de taille zéro. Le fournisseur WMI normalise toutes ces valeurs dans une représentation d’état de variante null lors de la lecture.

## <a name="user-interface-extensibility-link-notes"></a>Notes de lien d’extensibilité de l’interface utilisateur

L’utilisation de WMI pour inscrire un lien d’extensibilité d’interface utilisateur requiert la spécification des informations suivantes :

-   GUID : plusieurs liens peuvent partager le même GUID s’ils font partie d’un package ou d’une suite commune.
-   Sous-système-conçu pour indiquer des classifications de types de liens, tels que des suites ou des applications conformes autonomes
-   Nom chemin d’accès de la DLL de ressource et ID-spécifie la ressource pour le nom complet à afficher pour le lien.
-   Chemin et ID de la DLL de ressource de sous-titre : spécifie la ressource pour le texte supplémentaire sous le nom.
-   Chemin d’accès de l’image : chemin d’accès complet d’une image bitmap de 24 × 24 pixels (BMP), avec une profondeur de couleur de 8 bits par pixel et un canal alpha de préférence. Cela est spécifié de manière cohérente avec les extensions de l’interpréteur de commandes : <file system path> , <negative resource ID> . Par exemple : C : \\ Windows \\ system32 \\Wpccpl.dll,-20.
-   Chemin de l’image désactivé-identique au chemin d’accès à l’image ci-dessus, à l’exception de la variante de bitmap présentant l’état désactivé. Cette image s’affiche lorsque le contrôle parental est désactivé.
-   Chemin d’accès exe-chemin d’accès complet à un fichier exécutable à appeler à l’aide de ShellExecute (). Ce chemin d’accès doit être spécifié avec des barres obliques inverses ou le lien n’appellera pas l’exécutable. L’ajout d’un jeton% SID% après le chemin d’accès exe entraîne le remplacement de l’exécution de la liaison par la chaîne SID pour l’utilisateur pour lequel la page Hub est actuellement affichée. L’exécutable peut ensuite utiliser la chaîne SID pour gérer les fonctionnalités de l’utilisateur spécifié.

La désinstallation de l’application doit supprimer une inscription de lien d’extensibilité.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Remarques sur le lien d’extensibilité Web et le filtre de contenu Web

En définissant la propriété FilterID sur le même GUID qu’un lien d’extensibilité d’interface utilisateur inscrit existant, le lien affiché sera promu d’un lien générique dans autres paramètres vers le lien restrictions Web exclusives. Il s’agit d’un paramètre à l’ensemble de l’ordinateur. par conséquent, le filtre de contenu Web en boîte LSP contourne tout le filtrage pour tous les utilisateurs contrôlés. Un nom descriptif doit également être défini dans la propriété FilterName, qui est spécifiée par un chemin d’accès à la DLL de ressource et à l’ID.

Le système de contrôle parental recommande ce qui suit à partir de n’importe quel filtre Web de remplacement :

-   Honorer l’état d’activation/désactivation du contrôle parental pour un utilisateur.
-   Honorez les paramètres de rapport d’activité d’un utilisateur.
-   Surveillez la propriété FilterID. S’il est modifié à partir du GUID spécifié par le fournisseur, un autre filtre a pris la propriété et le filtre du fournisseur doit se désactiver lui-même. Une interface COM a été ajoutée pour réduire la surcharge de vérification périodique de cette modification par rapport à un appel WMI.
-   Il est vivement recommandé d’honorer les entrées de liste d’exemptions d’URL et d’applications HTTP en lecture seule et en lecture/écriture.
-   Recommandé pour respecter la liste de remplacement d’URL par utilisateur (liste verte/rouge).
-   Soyez robuste pour le changement rapide d’utilisateur.

Le contrôle parental ne limite pas la manière dont un filtre Web ou un autre filtre de contenu se connecte à Windows pour l’implémentation du filtrage. Les fournisseurs peuvent tirer parti de leurs investissements actuels ou des technologies préférées (LSP, TDI, etc.).

La désinstallation du filtre du fournisseur doit annuler l’enregistrement des entrées FilterID et NomFiltre. Pour ce faire, affectez à FilterID \_ la valeur Guid null et FilterName à une variante null. Le filtre de contenu Web intégré sera ensuite réactivé.

Notez que la réactivation du filtre Web intégré filtrera uniquement les nouvelles sessions, et non les sessions actives avant le commutateur.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Filtre de contenu Web-autoriser/exporter la liste des formats d’exportation/importation

Cette fonctionnalité n’est pas prise en charge sur Windows 8.

**Windows 7 et Windows Vista :** Cette fonctionnalité est prise en charge.

<WebAddresses>

<URL AllowBlock="1">https://alloweddomain.com/</URL>

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html</URL>

<URL AllowBlock="2">https://blockeddomain.com/</URL>

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html</URL>

</WebAddresses>

## <a name="application-restrictions-override-notes"></a>Remarques sur les restrictions d’application

Les remplacements de restrictions d’application sont définis par utilisateur pour autoriser des fichiers binaires ou des chemins d’accès spécifiques. Si un nouvel utilisateur contrôlé par le parent est configuré et que des remplacements de restrictions d’application sont nécessaires pour cet utilisateur, il est recommandé d’utiliser la clé d’exécution Windows dans le Registre avec une petite application marquée comme nécessitant une élévation déployée pour écrire les remplacements. En conséquence, une invite d’informations d’identification unique est générée pour configurer les remplacements de l’utilisateur, après quoi les fichiers binaires cibles pour les remplacements ne seront pas inopportuns pour les utilisateurs en raison d’autres invites de remplacement par l’administrateur.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Actions requises pour que les modifications de paramètres prennent effet

Si un administrateur modifie les paramètres d’un utilisateur standard connecté, un message d’avertissement est généré. Elle indique que les modifications des paramètres peuvent ne pas prendre effet tant que l’utilisateur contrôlé n’est pas déconnecté et reconnecté. Il s’agit d’une conception conservatrice. La plupart des paramètres prennent effet presque immédiatement, pendant que l’utilisateur contrôlé est connecté. L’une des exceptions concerne les jeux, où les paramètres prendront effet lors de la prochaine exécution de l’Explorateur de jeux ou l’appel du jeu.

## <a name="sample-code"></a>Exemple de code

Des exemples C++ sont fournis dans le kit de développement logiciel (SDK) illustrant l’utilisation des fonctionnalités d’extensibilité des paramètres. Veuillez consulter la section des exemples de contrôle parental.

## <a name="independent-test-tools"></a>Outils de test indépendants

L’inspection des classes et des instances est facilitée par le plug-in wmimgmt. msc et l’outil Wbemtest.exe.

## <a name="64-bit-considerations"></a>64-considérations sur les bits

les versions 64 bits du système d’exploitation Windows ont actuellement un fournisseur WMI 32 bits et un fournisseur 64 bits installés.

## <a name="general-code-development-and-debugging"></a>Développement et débogage de code général

Si Visual Studio est utilisé pour le développement de code de gestion des paramètres, le débogage local nécessite l’exécution de Visual Studio avec des droits d’administrateur (appel de la commande exécuter en tant qu’administrateur à l’aide de la ligne de commande ou de l’option de clic droit). Cela est dû à l’isolation des processus et des messages implémentée par le contrôle de compte d’utilisateur.

## <a name="minimum-compliance-api-settings-read"></a>Lecture des paramètres de l’API de conformité minimale

### <a name="interfaces-and-methods"></a>Interfaces et méthodes

L’API de conformité contrôlée par le fichier d’en-tête Wpcapi. h fournit un accès en lecture seule simplifié aux paramètres suivants à l’aide des interfaces COM.

Les méthodes d’interface racine [**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) fournissent l’accès aux éléments suivants :

-   Méthodes IWPCSettings :
    -   IsLoggingRequired () : le rapport d’activité est-il configuré comme étant activé pour l’utilisateur ?
    -   GetLastSettingsChangeTime () : l’application peut savoir si des stratégies de paramètres ont changé depuis une vérification précédente.
    -   GetRestrictions () : indique si les restrictions Web, les limites de temps, les restrictions de jeu ou les restrictions d’application sont définies sur on.
-   Méthodes IWPCWebSettings :
    -   GetSettings () : récupère les indicateurs pour le filtre activé ou désactivé et les téléchargements bloqués.
    -   RequestURLOverride () : entrez une demande dans le mécanisme de remplacement de l’administrateur (approbation par le biais de l’épaule) qui présentera une boîte de dialogue contenant les URL à approuver.
-   Méthodes IWPCGamesSettings :
    -   IsBlocked () : pour un ID d’application de jeu donné, est le jeu bloqué par le contrôle parental et pour quelle raison.
-   GetVisibility () : fournit des informations indiquant si l’interface utilisateur du contrôle parental est actuellement masquée.
-   GetWebFilterInfo () : fournit une interface pour l’obtention de l’ID du filtre de contenu Web actuellement actif.

### <a name="sample-code"></a>Exemple de code

Des exemples C++ sont fournis dans le kit de développement logiciel (SDK) illustrant l’utilisation de l’API de conformité. Veuillez consulter la section des exemples de contrôle parental.

 

 



