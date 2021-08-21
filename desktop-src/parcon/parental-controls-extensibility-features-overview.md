---
description: Les contrôles parentaux peuvent être étendus à l’aide des paramètres et des API de journalisation.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Vue d’ensemble des fonctionnalités d’extensibilité des contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf609c08a4114d7d96ae600744879bda53ac483d90bcd25def3dd0d5f9e3c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971718"
---
# <a name="parental-controls-extensibility-features-overview"></a>Vue d’ensemble des fonctionnalités d’extensibilité des contrôles parentaux

Les contrôles parentaux peuvent être étendus à l’aide des paramètres et des API de journalisation.

-   [Journalisation-arrière-plan](/windows)
-   [Extensibilité de la journalisation](#logging-extensibility)
-   [Ajout de liens d’extensibilité générale de l’interface utilisateur du panneau contrôle parental](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Remplacement du filtre de contenu Web](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Journalisation-arrière-plan

Microsoft a défini un certain nombre d’événements standard pour traiter les activités courantes :

-   Système : modifications des paramètres du contrôle parental, modifications du compte, changement de l’horloge système, échecs de tentatives de connexion.
-   Utilisateur :
    -   Limites du système/heure : heures d’ouverture de session, déconnexion, tentatives d’exécution de l’application et durée d’exécution de l’application (voir la remarque).
    -   Restrictions Web : sites Web visités et bloqués, tentatives de téléchargement de fichiers. Les navigateurs Web et les applications de type navigateur n’ont pas besoin de les consigner, car le filtre de contenu Web LSP le fait. Les filtres Web de remplacement doivent générer ces événements.
    -   Jeux : Jeux joués et bloqués, jeu (les événements fournissent une durée de lecture).
    -   Autoriser et bloquer des programmes spécifiques : tentative d’exécution, arrêt, bloqué par des restrictions d’application générales.
    -   Messagerie instantanée : tentative de conversion d’initiation, de tentative de jointure de conversation, de congé de conversation, de vidéo/audio, de jeu/de message de type short ou de transfert de fichiers/échange d’URL, tentative de modification de la liste de contacts.
    -   E-mail : reçu ou réception bloquée, tentative d’envoi, tentative de modification de la liste de contacts.
    -   Support : support lu et tenté.

Tous les événements précédents ne sont pas adaptés à une utilisation par les applications. Les modifications de compte, la modification de l’horloge système et la journalisation des événements de connexion et de déconnexion sont implémentées uniquement par le système d’exploitation et ne sont donc pas exposées publiquement.

> [!Note]  
> l’instrumentation des événements d’entrée et de sortie de l’application est disponible dans Windows Vista et est configurée par les contrôles de contrôle Parental pour consigner ces données.

 

## <a name="logging-extensibility"></a>Extensibilité de la journalisation

Un événement personnalisé générique est également défini avec 3 balises/valeurs disponibles, de sorte que les éditeurs de logiciels indépendants n’auront généralement pas besoin de définir leur propre valeur dans un manifeste. La visionneuse du journal reconnaît et affiche les en-têtes et les valeurs des balises si le nombre de champs utilisés (1 à 3) et les en-têtes de chaque champ sont enregistrés à l’aide de l’API WMI. Le observateur d’événements générique peut également être utilisé pour afficher des événements personnalisés.

Si l’événement personnalisé générique n’est pas approprié, un éditeur de logiciels indépendant peut définir son propre fichier à l’aide d’un manifeste d’application et il peut inscrire des en-têtes pour trois champs au maximum à l’aide de la même API WMI.

les éditeurs de logiciels indépendants peuvent choisir de définir leurs propres événements et de les utiliser indépendamment de la visionneuse du journal par le biais des api Windows publiques. Cela ne présente pas l’avantage d’une centralisation complète des journaux.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Ajout de liens d’extensibilité générale de l’interface utilisateur du panneau contrôle parental

Un lien d’extensibilité de l’interface utilisateur à usage général est exposé en accédant aux paramètres via WMI, en créant une instance d’extension à partir du chemin d’accès et de l’ID de la DLL de ressource de nom, du chemin d’accès à l’image (bitmap), du chemin d’accès à l’image de l’état désactivé, du chemin d’accès et de l’ID de la DLL une fois inscrite, le lien apparaît dans la zone plus Paramètres du panneau de contrôle Parental, et un clic sur celui-ci appellera l’exécutable spécifié.

La chaîne de chemin d’accès exécutable peut éventuellement inclure un jeton pour le SID de l’utilisateur actuel à substituer avant l’appel. Cela permet à l’exécution de la liaison de fonctionner dans le contexte de l’utilisateur pour lequel la page Hub est actuellement affichée, si l’exécutable doit connaître le SID.

## <a name="web-content-filter-replacement"></a>Remplacement du filtre de contenu Web

Comme indiqué dans la rubrique, le [contrôle Parental In-Box des restrictions et des interfaces utilisateur](parental-controls-in-box-restrictions-and-user-interfaces.md), le filtre de contenu Web intégré peut être remplacé par un filtre fourni par le fournisseur. Pour ce faire, accédez aux paramètres via WMI pour définir un GUID et un nom possédant le filtrage.

Le mécanisme d’extensibilité de l’interface utilisateur général est utilisé pour exposer un filtre tiers. il s’agit du même mécanisme que celui utilisé pour toute extension qui souhaite apparaître dans la section plus Paramètres du panneau de contrôle Parental de niveau supérieur. en effectuant une étape supplémentaire pour définir le même GUID et un chemin d’accès à la DLL de ressource de nom et un ID appropriés dans les paramètres de filtre au niveau du système, le lien de filtre affiché par la boîte est masqué et l’entrée tierce s’affiche en haut de la section plus Paramètres. Le nom enregistré pour le filtre s’affiche dans la section Résumé.

la réinitialisation du GUID de filtre et des paramètres de chemin d’accès/ID de nom entraîne la réinitialisation du filtre de contenu Web intégré en tant que filtre actif et son réaffichage dans la section Windows Paramètres.

notez que les filtres tiers ne sont pas limités dans les technologies utilisées pour se connecter à Windows communications. Un filtre doit simplement exposer ses paramètres à l’aide d’un lien d’extensibilité et honorer les paramètres de contrôle parental appropriés.

 

 
