---
title: Windows Classe d’assistance extensible de la plateforme de filtrage
description: la plateforme de filtrage de Windows (WFP) comprend une classe d’assistance de l’infrastructure de diagnostics du réseau (NDF), appelée classe d’assistance de la plateforme de filtrage (FPHC).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff972beffebb44b33eb68a0439193307639522738ac1f8766845404c03d3cd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065209"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Windows Classe d’assistance extensible de la plateforme de filtrage

la [plateforme de filtrage de Windows (WFP)](/windows/desktop/FWP/windows-filtering-platform-start-page) comprend une classe d’assistance de l’infrastructure de diagnostics du réseau (NDF), appelée classe d’assistance de la plateforme de filtrage (FPHC). FPHC peut aider à identifier les causes racines des problèmes de connectivité provoqués par la plateforme WFP. Les développeurs de pare-feu tiers peuvent implémenter leurs propres classes d’assistance NDF. L’extensibilité FPHC permet d’appeler ces classes d’assistance tierces pendant les Diagnostics.

Cette rubrique suppose que vous connaissez l' [API WFP](/windows/desktop/FWP/windows-filtering-platform-start-page).

## <a name="why-extend-the-fphc"></a>Pourquoi étendre le FPHC ?

Tous les développeurs qui écrivent des applications qui appellent l’API WFP doivent écrire une classe d’assistance NDF qui étend FPHC.

FPHC peut identifier la plateforme WFP comme étant la cause d’un problème de connectivité. S’il est disponible, FPHC peut également identifier le fournisseur qui a créé le filtre qui bloque le trafic réseau. FPHC transmet ces informations à NDF, qui à son tour peut informer l’utilisateur que WFP est à l’origine du problème de connectivité et lui attribuer le nom bloquant le trafic.

Toutefois, le FPHC ne peut pas suggérer une action corrective à l’utilisateur, ni fournir la raison pour laquelle le filtre bloque le trafic vers l’utilisateur. Seule une extension FPHC peut effectuer ces tâches.

Prenons l’exemple d’une application de pare-feu tierce qui appelle l’API WFP. Si le pare-feu tiers implémente une extension FPHC, des actions personnalisées peuvent être implémentées pour gérer les problèmes de connectivité identifiés par NDF. Lorsque NDF diagnostique qu’une application a été bloquée par le pare-feu tiers, l’extension FPHC peut gérer l’événement bloquant. L’une des méthodes permettant à l’extension FPHC de gérer un événement est de présenter à l’utilisateur une invite pour débloquer un programme à l’aide du pare-feu, puis débloquer le programme à la confirmation de l’utilisateur. L’extension FPHC peut également gérer un événement en notifiant à l’utilisateur la raison pour laquelle l’application a été bloquée, telle qu’une application a été bloquée, car elle a été considérée comme un programme malveillant par le pare-feu.

## <a name="about-wfp-diagnostics"></a>À propos des diagnostics WFP

Quand NDF est appelé pour diagnostiquer un problème réseau, les classes d’assistance sont contactées pour déterminer la cause du problème. Si une classe d’assistance de niveau supérieur détermine qu’une défaillance réseau peut être provoquée par WFP, elle génère une hypothèse pour FPHC en fonction des informations disponibles. NDF passe cette hypothèse, sous la forme de plusieurs attributs d’événement, à FPHC. Ces attributs sont décrits en détail dans la section [attributs d’événement fphc](#windows-filtering-platform-extensible-helper-class) ci-dessous.

Un problème réseau peut être décrit comme un problème de connectivité affectant une tentative de connexion particulière. Par exemple, l’utilisateur a peut-être bloqué accidentellement une application en cliquant par inadvertance sur **ne pas autoriser**. Le pare-feu empêchera ensuite la liaison de l’application à n’importe quel port. L’utilisateur ne connaissant pas la raison pour laquelle l’application est bloquée peut tenter de diagnostiquer le problème via un point d’entrée proposé par l’application. FPHC examine les journaux et, s’il trouve une correspondance, il récupère l’ID de filtre et l’ID de fournisseur de ce filtre particulier. À ce stade, FPHC sait qui est le propriétaire du filtre, et il passe par le processus de diagnostic à la classe d’assistance appropriée pour un diagnostic plus approfondi.

L’événement le plus récent dans les journaux des événements WFP pour qu’il corresponde aux attributs est sélectionné comme étant pertinent pour le problème réseau. Si aucun événement correspondant n’est trouvé et que l’heure à laquelle l’événement s’est produit est couverte dans le journal WFP, FPHC indique à NDF qu’il est sain. Si aucun événement correspondant n’est trouvé et que les journaux WFP n’incluent pas l’heure à laquelle l’événement s’est produit, FPHC renvoie un état indéterminé à NDF.

Si un événement correspondant est trouvé, FPHC utilise l’ID du fournisseur du filtre qui a provoqué l’événement pour identifier le fournisseur de la règle de sécurité qui a bloqué la connectivité. FPHC vérifie ensuite s’il existe une extension de classe d’assistance pour ce fournisseur. Si une hypothèse est trouvée, FPHC génère une hypothèse pour ce fournisseur, puis l’objet NDF appelle l’extension. L’extension doit retourner des informations de diagnostic et de réparation utiles à l’utilisateur.

## <a name="helper-class-registration"></a>Inscription de la classe d’assistance

Une extension FPHC doit être inscrite comme décrit dans [inscription des extensions de classe d’assistance NDF](registering-ndf-helper-class-extensions.md). Les développeurs qui implémentent une classe d’assistance doivent inscrire leurs extensions pour s’assurer que l’extension est appelée par NDF, le cas échéant. L' *attribut correspondant* décrit ci-dessous doit être stocké dans le Registre sous **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *NomFournisseur* \\ **HostDLLs** \\ *Helper Class dll* \\ **HelperClasses** \\ *Helper Class Name* \\ **MatchAttributes**.

Le tableau suivant présente l’attribut correspondant utilisé pour identifier l’hypothèse à utiliser dans les diagnostics dans le journal des événements WFP. 

| Nom       | Type    | Description                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | SZ de REG \_ | GUID de l’extension FPHC. Cette valeur doit être identique à celle du GUID du fournisseur WFP. <br/> Cette chaîne respecte la casse. Elle doit être stockée dans le registre en majuscules avec des accolades et des traits d’Union. Par exemple, {C200E360-38C5-11CE-AE62-08002B2B79EF} est un ProviderID valide.<br/> |



 

Lorsque le ProviderID d’un filtre bloquant correspond à celui d’une classe d’assistance inscrite, FPHC informe NDF d’appeler cette classe d’assistance, étendant ainsi la fonctionnalité de diagnostic de FPHC.

## <a name="fphc-event-attributes"></a>Attributs d’événement FPHC

Le tableau suivant répertorie les attributs d’événement associés à chaque événement correspondant. Chaque attribut d’événement est stocké dans une structure d' [**\_ attribut d’assistance**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Ces attributs sont passés par NDF à FPHC lorsqu’un événement correspondant est trouvé. Elles peuvent à leur tour être passées aux extensions FPHC.



| Attribut     | [**Attribut \_**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) Valeur de type | Description                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID du fournisseur | AU \_ GUID                                        | GUID du fournisseur associé au filtre.                                                                                      |
| Timestamp     | à \_ la \_ chaîne d’octets                               | Mémoire tampon de type FILETIME qui spécifie l’heure à laquelle l’événement s’est produit. Cet horodatage peut être utilisé pour identifier un événement de manière unique. |
| ipProtocol    | À \_ UInt32                                      | Protocole de couche de transport, au format UINT8.                                                                                            |
| LocalAddr     | SUR \_ sockaddr                                    | L’adresse IP et le port locaux, stockés dans une structure [**\_ sockaddr de diagnostic**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                             |
| RemoteAddr    | SUR \_ sockaddr                                    | L’adresse IP et le port distants, stockés dans une structure [**\_ sockaddr diag**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                            |
| userId        | à \_ la \_ chaîne d’octets                               | Mémoire tampon de type SID qui représente l’userid. Si userId a une longueur de 0, le SID n’est pas disponible.                                        |
| appId         | au niveau de la \_ chaîne                                      | Mémoire tampon qui stocke l’identificateur d’application récupéré. Si appId a la valeur L "", l’identificateur d’application n’est pas disponible.        |



 

## <a name="handling-fphc-events"></a>Gestion des événements FPHC

Avant de suggérer des informations de diagnostic et de réparation à l’utilisateur, une extension FPHC doit collecter plus de données que ce qui est fourni par les notifications FPHC. Ces données peuvent être obtenues à partir des [fonctions de gestion des événements WFP](/windows/desktop/FWP/fwp-mgmt-functions). Ces fonctions sont illustrées dans l’exemple [affichage des événements .net](/windows/desktop/FWP/displaying-net-events) .

Un exemple de gestion des événements plus détaillé est inclus dans le kit de développement logiciel (SDK). le code source de l’exemple se trouve dans l’emplacement d’installation du kit de développement logiciel (sdk) sous C : \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ samples \\ NetDs \\ WFP \\ DiagEvents. le kit de développement logiciel (SDK) Windows Vista est disponible dans le [centre de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

## <a name="built-in-fphc-diagnostics"></a>Diagnostics FPHC intégrés

En l’absence d’une extension FPHC, FPHC peut diagnostiquer les scénarios listés ci-dessous. La plupart des échecs de connectivité diagnostiqués par FPHC sont dus au fait que les pare-feu bloquent le trafic. Les scénarios IPsec sont moins courants.

Le tableau suivant présente certains scénarios provoquant des échecs de connectivité qui peuvent être diagnostiqués par FPHC, ainsi que la description et les informations de réparation transmises à NDF.



| Scénario                   | Description de l’intégrité faible                                                                                                               | Informations de réparation                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Suppression du pare-feu              | Les paramètres de pare-feu sur cet ordinateur bloquent la connexion.                                                                  | Vérifiez les paramètres de votre pare-feu.       |
| Échec du mode principal          | Vous ne pouvez pas vous connecter en raison d’une incompatibilité de stratégie de sécurité IPsec.                                                                     | Contactez le propriétaire de la stratégie IPsec.      |
| Échec du mode rapide         | Vous ne pouvez pas vous connecter en raison d’une incompatibilité de stratégie de sécurité IPsec.                                                                     | Contactez le propriétaire de la stratégie IPsec.      |
| Échec du mode utilisateur          | Vous ne pouvez pas vous connecter en raison d’une incompatibilité de stratégie de sécurité IPsec.                                                                     | Contactez le propriétaire de la stratégie IPsec.      |
| Échec des informations d’identification         | Vous ne pouvez pas vous connecter, car l’autorité de certification racine de cet ordinateur ne correspond pas à l’autorité de certification racine sur l’ordinateur distant. | Mettez à jour le certificat racine approuvé. |
| Certificat expiré        | Le certificat utilisé pour l’authentification IPsec est arrivé à expiration.                                                                           | Demander un certificat.               |
| Autres échecs de certificat | Aucun certificat valide n’a été trouvé pour l’authentification IPsec.                                                                          | Demander un certificat.               |
| Échec de Kerberos           | L’ordinateur ne fait pas partie de ce domaine.                                                                                             | Joindre cet ordinateur à un domaine.      |
| Clé prépartagée              | Réinitialisez les clés prépartagées.                                                                                                            | Réinitialisez les clés prépartagées.            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Plateforme de filtrage Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Conception des extensions de classe d’assistance NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Inscription des extensions de classe d’assistance NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Exemples de classes d’assistance NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

