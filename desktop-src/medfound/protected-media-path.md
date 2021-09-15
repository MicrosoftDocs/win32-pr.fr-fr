---
description: 'Cette rubrique présente trois rubriques connexes : environnement protégé, passerelle d’interopérabilité des médias, révocation et renouvellement.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Chemin du média protégé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7304edadf1623d41bc2f1f5c6b2b4cda2dd5f598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414036"
---
# <a name="protected-media-path"></a>Chemin du média protégé

Cette rubrique présente trois rubriques connexes : environnement protégé, passerelle d’interopérabilité des médias, révocation et renouvellement.

-   un environnement protégé (PE) est un ensemble de technologies qui permet de transmettre du contenu protégé depuis et vers Windows Vista de manière protégée. Tous les composants à l’intérieur d’un environnement protégé sont approuvés et le processus est protégé contre la falsification.
-   Le chemin d’accès au média protégé (PMP) est un fichier exécutable qui s’exécute dans un environnement protégé.
-   Si un composant approuvé dans le PE devient compromis, une fois le processus en cours, il est révoqué. Toutefois, Microsoft fournit un mécanisme de renouvellement pour installer une version fiable plus récente du composant lorsqu’il est disponible.

pour plus d’informations sur les composants multimédias protégés par la signature de code, consultez le livre blanc [signing for protected media components in Windows Vista](/windows-hardware/test/hlk/).

Cette rubrique contient les sections suivantes :

-   [Environnement protégé](#protected-environment)
-   [Conception de l’environnement protégé](#design-of-the-protected-environment)
-   [Chemin du média protégé](#protected-media-path)
    -   [Autorités d’approbation d’entrée](#input-trust-authorities)
    -   [Autorités de confiance de sortie](#output-trust-authorities)
    -   [Objets de stratégie](#policy-objects)
    -   [Création d’objets dans l’PMP](#creating-objects-in-the-pmp)
-   [Vue d’ensemble de la négociation de stratégie](#overview-of-policy-negotiation)
-   [Révocation et renouvellement](#revocation-and-renewal)
-   [Protection des liens de sortie](#output-link-protection)
-   [Rubriques connexes](#related-topics)

## <a name="protected-environment"></a>Environnement protégé

La protection du contenu englobe plusieurs technologies, chacune essayant de s’assurer que le contenu ne peut pas être utilisé d’une manière qui n’est pas cohérente avec l’intention du propriétaire ou du fournisseur du contenu. Ces technologies incluent la protection contre la copie, la protection des liens, l’accès conditionnel et la gestion des droits numériques (DRM). La Fondation de chaque est approuvée : l’accès au contenu est accordé uniquement aux composants logiciels qui adhèrent aux conditions d’utilisation affectées à ce contenu.

pour réduire les menaces contre le contenu protégé, Windows Vista et Media Foundation logiciel autorisent l’exécution de code de confiance dans un environnement protégé. Un PE est un ensemble de composants, de recommandations et d’outils conçus pour améliorer la protection contre le piratage de contenu.

Avant d’examiner le PE plus en détail, il est important de comprendre les menaces qu’il est prévu de réduire. Supposons que vous exécutez une application multimédia dans un processus en mode utilisateur. L’application est liée aux différentes bibliothèques de liens dynamiques (dll) qui contiennent des plug-ins multimédias, tels que des décodeurs. D’autres processus sont également exécutés en mode utilisateur et différents pilotes sont chargés dans le noyau. Si aucun mécanisme d’approbation n’est en place, les menaces suivantes existent :

-   L’application peut accéder directement à des médias protégés ou pirater la mémoire de processus.
-   Les plug-ins peuvent accéder directement au contenu ou pirater la mémoire du processus.
-   D’autres processus peuvent pirater la mémoire du processus multimédia soit directement, soit en injectant du code.
-   Les pilotes de noyau peuvent pirater la mémoire du processus multimédia.
-   Le contenu peut être envoyé à l’extérieur du système via un support non protégé. (La protection de la liaison est conçue pour atténuer cette menace.)

## <a name="design-of-the-protected-environment"></a>Conception de l’environnement protégé

Un environnement protégé s’exécute dans un processus protégé distinct de l’application multimédia. la fonctionnalité de processus protégé de Windows Vista empêche d’autres processus d’accéder au processus protégé.

Lorsqu’un processus protégé est créé, les principaux composants du noyau identifient les composants non fiables et les plug-ins afin que l’environnement protégé puisse refuser de les charger. Un composant approuvé est un composant qui a été correctement signé par Microsoft. Le noyau effectue également le suivi des modules qui s’y chargent, ce qui permet à l’environnement protégé d’arrêter la lecture du contenu protégé si un module non approuvé est chargé. Avant le chargement d’un composant de noyau, le noyau vérifie s’il est approuvé. Si ce n’est pas le cas, les composants de confiance déjà présents dans le PE refusent de traiter le contenu protégé. Pour ce faire, les composants PE effectuent périodiquement une liaison sécurisée par chiffrement avec le noyau. Si un composant en mode noyau non fiable est présent, le protocole de transfert échoue et indique au PE qu’il existe un composant non approuvé.

Si un composant approuvé devient compromis, une fois le processus en retard, il peut être révoqué. Microsoft fournit un mécanisme de renouvellement pour installer une nouvelle version approuvée quand elle est disponible.

## <a name="protected-media-path"></a>Chemin du média protégé

Le chemin d’accès au média protégé (PMP) est le fichier exécutable PE principal pour Media Foundation. Le PMP est extensible, de sorte que les mécanismes de protection de contenu tiers peuvent être pris en charge.

Le PMP accepte le contenu protégé et les stratégies associées de toute source de Media Foundation à l’aide d’un système de protection du contenu, y compris ceux fournis par des tiers. Il envoie le contenu à n’importe quel récepteur de Media Foundation, à condition que le récepteur soit conforme aux stratégies spécifiées par la source. Il prend également en charge les transformations entre la source et le récepteur, y compris les transformations tierces, à condition qu’elles soient approuvées.

Le PMP s’exécute dans un processus protégé isolé de l’application multimédia. L’application a uniquement la possibilité d’échanger des messages de commande et de contrôle avec l’PMP, mais elle n’a pas accès au contenu une fois qu’elle est passée à l’PMP. Le diagramme suivant illustre ce processus.

![diagramme du chemin d’accès du média protégé](images/pmp04.png)

Les zones ombrées représentent des composants qui peuvent être fournis par des tiers. Tous les composants créés à l’intérieur du processus protégé doivent être signés et approuvés.

L’application crée une instance de la session multimédia à l’intérieur du processus protégé et reçoit un pointeur vers une session de média proxy, qui marshale les pointeurs d’interface à travers la limite de processus.

La source du média peut être créée dans le processus d’application, comme illustré ici, ou à l’intérieur du processus protégé. Si la source du média est créée à l’intérieur du processus d’application, la source crée un proxy pour lui-même dans le processus protégé.

Tous les autres composants de pipeline, tels que les décodeurs et les récepteurs multimédias, sont créés dans le processus protégé. Si ces objets exposent des interfaces personnalisées pour les applications, ils doivent fournir un proxy/stub DCOM pour marshaler l’interface.

Pour appliquer la stratégie au contenu protégé lorsqu’il transite par le pipeline, le PMP utilise trois types de composants : les autorités d’approbation d’entrée (ITAs), les autorités de confiance de sortie (OTAs) et les objets de stratégie. Ces composants fonctionnent ensemble pour accorder ou limiter les droits d’utilisation du contenu, et pour spécifier les protections de liaison qui doivent être utilisées lors de la diffusion de contenu, telles que la fonction de protection du contenu numérique à bande passante élevée (HDCP).

### <a name="input-trust-authorities"></a>Autorités d’approbation d’entrée

Un ITA est créé par une source multimédia approuvée et exécute plusieurs fonctions :

-   Spécifie les droits d’utilisation du contenu. Les droits peuvent inclure le droit de lire le contenu, le transférer vers un appareil, et ainsi de suite. Il définit une liste triée des systèmes de protection de sortie approuvés et les stratégies de sortie correspondantes pour chaque système. L’ITA stocke ces informations dans un objet de stratégie.
-   Fournit le déchiffreur nécessaire pour déchiffrer le contenu.
-   Établit une relation de confiance avec le module de noyau dans l’environnement protégé pour s’assurer que l’ITA s’exécute dans un environnement approuvé.

Une ITA est associée à un flux individuel contenant du contenu protégé. Un flux ne peut avoir qu’un seul ITA, et une instance d’ITA ne peut être associée qu’à un seul flux.

### <a name="output-trust-authorities"></a>Autorités de confiance de sortie

Un OTA est associé à une sortie approuvée. Le OTA expose une action que la sortie approuvée peut effectuer sur le contenu, par exemple la lecture ou la copie. Son rôle consiste à appliquer un ou plusieurs systèmes de protection de sortie requis par l’ITA. Le OTA interroge l’objet de stratégie fourni par ITA pour déterminer le système de protection qu’il doit appliquer.

### <a name="policy-objects"></a>Objets de stratégie

Un objet de stratégie encapsule les exigences de protection de contenu d’un ITA. Il est utilisé par le moteur de stratégie pour négocier la prise en charge de la protection du contenu avec un OTA. OTAs les objets de stratégie de requête pour déterminer les systèmes de protection qu’ils doivent appliquer à chaque sortie du contenu actuel.

### <a name="creating-objects-in-the-pmp"></a>Création d’objets dans l’PMP

Pour créer un objet dans le chemin d’accès de média protégé (PMP), [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) appelle [**IMFPMPHostApp :: ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid), avec le **IStream** d’entrée spécifié de la façon suivante :

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Vue d’ensemble de la négociation de stratégie

Trois exigences fondamentales doivent être respectées pour que le contenu protégé puisse être traité dans le PMP. Tout d’abord, le contenu protégé doit être envoyé uniquement aux sorties approuvées. Deuxièmement, seules les actions autorisées doivent être appliquées à un flux. Troisièmement, seuls les systèmes de protection de sortie approuvés doivent être utilisés pour lire un flux. Le moteur de stratégie coordonne entre ITAs et OTAs pour s’assurer que ces exigences sont satisfaites.

le moyen le plus simple de comprendre le processus consiste à parcourir un exemple simplifié qui identifie les étapes nécessaires pour lire le contenu ASF protégé par Windows Media Digital Rights Management (WMDRM).

Quand un utilisateur lance une application de lecteur et ouvre un fichier ASF avec un flux audio protégé et un flux vidéo protégé, les étapes suivantes doivent être effectuées :

1.  L’application crée la source de média ASF et la session de chemin d’accès de média protégée (PMP). Media Foundation crée un processus PMP.
2.  L’application crée une topologie partielle qui contient un nœud source audio connecté au convertisseur audio, et un nœud source vidéo connecté au convertisseur vidéo amélioré (EVR). Pour les convertisseurs, l’application ne crée pas directement le convertisseur. Au lieu de cela, l’application crée dans le processus non protégé un objet appelé *objet d’activation*. Le PMP utilise l’objet d’activation pour créer les convertisseurs dans le processus protégé. (Pour plus d’informations sur les objets d’activation, consultez [objets d’activation](activation-objects.md).)
3.  L’application définit la topologie partielle sur la session PMP.
4.  La session PMP sérialise la topologie et la transmet à l’hôte PMP dans le processus protégé. L’hôte PMP envoie la topologie au moteur de stratégie.
5.  Le chargeur de topologie appelle [**IMFInputTrustAuthority :: GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) sur le ITAS et insère les déchiffreurs dans la topologie immédiatement en aval des nœuds sources correspondants.
6.  Le chargeur de topologie insère les décodeurs audio et vidéo en aval des nœuds Decrypter.
7.  Le moteur de stratégie analyse les nœuds insérés pour déterminer s’ils implémentent l’interface [**IMFTrustedOutput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) . Le EVR et le convertisseur audio implémentent tous deux **IMFTrustedOutput**, car ils envoient des données en dehors du PMP.
8.  Chaque ITA confirme qu’il s’exécute dans un processus protégé en effectuant une négociation de chiffrement avec un module noyau de l’environnement protégé.
9.  Pour chaque flux, le moteur de stratégie négocie la stratégie en obtenant un objet de stratégie de l’ITA et en le passant à OTA. Le OTA fournit une liste des systèmes de protection qu’il prend en charge, et l’objet de stratégie indique les systèmes de protection qui doivent être appliqués, ainsi que les paramètres corrects. Le OTA applique ensuite ces paramètres. Si ce n’est pas le cas, le contenu est bloqué.

## <a name="revocation-and-renewal"></a>Révocation et renouvellement

Un composant approuvé peut être révoqué s’il est compromis ou s’il est découvert comme violant les contrats de licence dans lesquels il a été initialement approuvé. Il existe un mécanisme de renouvellement pour installer une version plus récente et plus fiable du composant.

Les composants approuvés sont signés à l’aide d’un certificat de chiffrement. Microsoft publie une liste de révocation globale (GRL) qui identifie les composants qui ont été révoqués. Le GRL est signé numériquement pour garantir son authenticité. Les propriétaires de contenu peuvent garantir, par le biais du mécanisme de stratégie, que la version actuelle du GRL est présente sur l’ordinateur de l’utilisateur.

## <a name="output-link-protection"></a>Protection des liens de sortie

Quand le contenu vidéo Premium est affiché, les images déchiffrées et non compressées se déplacent sur un connecteur physique du périphérique d’affichage. Les fournisseurs de contenu peuvent exiger que les images vidéo soient protégées à ce stade, lors de leur déplacement sur le connecteur physique. Il existe différents mécanismes de protection à cet effet, y compris High-Bandwidth Digital protection du contenu (HDCP) et DisplayPort protection du contenu (DPCP). La vidéo OTA applique ces protections à l’aide du [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM). Le gestionnaire de protection de sortie envoie des commandes au pilote Graphics, et le pilote Graphics applique tous les mécanismes de protection de liaison requis par la stratégie.

![diagramme qui montre la relation entre la vidéo OTA et OPM.](images/pmp05.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[protection du contenu basé sur GPU](gpu-based-content-protection.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> <dt>

[Session média PMP](pmp-media-session.md)
</dt> </dl>

 

 
