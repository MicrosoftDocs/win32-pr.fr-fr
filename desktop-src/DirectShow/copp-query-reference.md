---
description: Informations de référence sur les requêtes COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Informations de référence sur les requêtes COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413998"
---
# <a name="copp-query-reference"></a>Informations de référence sur les requêtes COPP

Cette section décrit les requêtes d’État prises en charge par le protocole COPP (Certified Output Protection Protocol). Pour chaque requête, le GUID qui définit la requête est listé, avec les données d’entrée et les données de retour.



| Requête                   | GUID                                     |
|-------------------------|------------------------------------------|
| Données de bus                | **\_COPPQUERYBUSDATA DXVA**               |
| Type de connecteur          | **\_COPPQUERYCONNECTORTYPE DXVA**         |
| Afficher les données            | **\_COPPQUERYDISPLAYDATA DXVA**           |
| Données de clé HDCP           | **\_COPPQUERYHDCPKEYDATA DXVA**           |
| Niveau de protection global | **\_COPPQUERYGLOBALPROTECTIONLEVEL DXVA** |
| Niveau de protection local  | **\_COPPQUERYLOCALPROTECTIONLEVEL DXVA**  |
| Type de protection         | **\_COPPQUERYPROTECTIONTYPE DXVA**        |
| Signalisation               | **\_COPPQUERYSIGNALING DXVA**             |



 

Requête de données de bus

Retourne le type de bus d’e/s utilisé par la carte graphique.

-   **GUID**: DXVA \_ COPPQueryBusData
-   **Données d’entrée**: aucune.
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Le type de bus est retourné dans le membre **dwData** en tant qu’indicateur de l’énumération [**Copp \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .

Requête de type de connecteur

Retourne le type de connecteur physique.

-   **GUID**: DXVA \_ COPPQueryConnectorType
-   **Données d’entrée**: aucune.
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Le type de connecteur est retourné dans le membre **dwData** en tant qu’indicateur de l’énumération [**Copp \_ ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .

Afficher la requête de données

Retourne une description du signal vidéo qui est transmis sur le connecteur.

Le signal vidéo transmis sur le connecteur n’a pas nécessairement le même format que le mode d’affichage du bureau. Par exemple, le mode d’affichage du Bureau peut être de 1024 x 768 pixels à 85 Hz, tandis que le connecteur peut être un connecteur S-Video qui transmet un signal vidéo à 720 x 480 pixels, 60/1.01 Hz entrelacé. Dans ce cas, le pilote retourne la résolution du signal S-Video, et non la résolution du bureau.

-   **GUID**: DXVA \_ COPPQueryDisplayData
-   **Données d’entrée**: aucune.
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .

Requête de données de clé HDCP

Retourne le vecteur de sélection de clé HDCP de l’appareil (B-KSV).

KSV est un identificateur fourni au fabricant de l’appareil et est utilisé dans le processus d’authentification et d’installation HDCP. L’application doit vérifier cette valeur par rapport à la liste des KSVs révoqués. Le mécanisme d’obtention de la liste de révocation KSV est en dehors de l’étendue du protocole COPP. Pour plus d’informations, consultez la spécification HDCP.

Cette requête détermine également si l’appareil HDCP connecté est une analyse ou un répéteur HDCP. L’application ne doit pas lire de contenu protégé si l’appareil HDCP est un répétiteur HDCP, car ceux-ci ne sont pas pris en charge par COPP.

-   **GUID**: DXVA \_ COPPQueryHDCPKeyData
-   **Données d’entrée**: aucune.
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .

Requête de niveau de protection global

Retourne le niveau de protection global pour un mécanisme de protection spécifié.

Le niveau de protection global est le niveau de protection en cours d’application sur le connecteur, quelle que soit la façon dont le pilote Graphics a été invité à appliquer la protection. Par exemple, une application peut définir le niveau de protection ACP en appelant la fonction **ChangeDisplaySettingsEx** . Dans ce cas, le niveau de protection global reflète ce paramètre, même s’il n’a pas été demandé via COPP.

-   **GUID**: DXVA \_ COPPQueryGlobalProtectionLevel
-   **Données d’entrée**: mécanisme de protection à interroger, spécifié sous la forme d’un entier 32 bits. Voir [indicateurs de type de protection Copp](copp-protection-type-flags.md).
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Le niveau de protection actuel est retourné dans le membre **dwData** . La signification de cette valeur dépend du mécanisme de protection qui est interrogé. Pour chaque mécanisme de protection, la valeur du membre **dwData** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.

    | Mécanisme de protection | Énumération                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Niveau de protection de l’ACP de COPP \_ \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_Niveau de \_ protection \_ CGMSA de Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**\_Niveau de \_ protection du HDCP Copp \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Requête de niveau de protection local

Retourne le niveau de protection local pour un mécanisme de protection spécifié.

Le niveau de protection local est le niveau de protection qui a été demandé via la session COPP actuelle. Le pilote peut définir un niveau de protection supérieur.

-   **GUID**: DXVA \_ COPPQueryLocalProtectionLevel
-   **Données d’entrée**: mécanisme de protection à interroger, en tant qu’entier 32 bits. Voir [indicateurs de type de protection Copp](copp-protection-type-flags.md).
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Le niveau de protection actuel est retourné dans le membre **dwData** . La signification de cette valeur dépend du mécanisme de protection qui est interrogé. Pour chaque mécanisme de protection, la valeur du membre **dwData** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.

    | Mécanisme de protection | Énumération                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | ACP                  | [**Niveau de protection de l’ACP de COPP \_ \_ \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | CGMS-A               | [**\_Niveau de \_ protection \_ CGMSA de Copp**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | HDCP                 | [**\_Niveau de \_ protection du HDCP Copp \_**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

Requête de type de protection

Retourne les mécanismes de protection disponibles pour le connecteur.

-   **GUID**: DXVA \_ COPPQueryProtectionType
-   **Données d’entrée**: aucune.
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) . Les mécanismes de protection sont retournés dans le membre **dwData** comme une combinaison de zéro ou plusieurs indicateurs. Voir [indicateurs de type de protection Copp](copp-protection-type-flags.md). Si plusieurs mécanismes de protection sont disponibles, les indicateurs sont combinés avec **une opération or** au niveau du bit.

Requête de signalisation

Retourne une liste de toutes les normes de protection prises en charge par le pilote, la norme actuellement active et les proportions actuelles ou autres données de signalisation.

-   **GUID**: DXVA \_ COPPQuerySignaling
-   **Données d’entrée**: aucune.
-   **Return Data**: retourne une structure [**DXVA \_ COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



