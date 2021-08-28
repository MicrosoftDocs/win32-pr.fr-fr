---
title: Mode de transport de la découverte de négociation en mode limite
description: Le mode de transport de la découverte de négociation dans le scénario de stratégie IPsec en mode limite demande la protection du mode de transport IPsec pour tout le trafic correspondant.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b647f7a4ddf7b50131d6f84e09bf9fc6dce8f13a8575c6971d65be7caa7464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068859"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a>Mode de transport de la découverte de négociation en mode limite

Le mode de transport de la découverte de négociation dans le scénario de stratégie IPsec en mode limite demande la protection du mode de transport IPsec pour tout le trafic correspondant. Si la négociation IKE/AuthIP échoue, les connexions entrantes et sortantes sont autorisées à revenir en texte clair.

Cette stratégie IPsec est généralement utilisée sur les ordinateurs qui sont accessibles à la fois par les ordinateurs prenant en charge IPsec et non-IPsec.

Un exemple de scénario potentiel de mode de transport de la découverte de négociation consiste à sécuriser tout le trafic de données de monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec et à activer la détection de négociation en mode limite.

Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.

<dl>

**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.  
    -   Pour IKE, contexte d’un fournisseur de stratégie de type FWPM \_ IPSec \_ IKE \_ mm \_ Context.
    -   Pour AuthIP, contexte du fournisseur de stratégie de type FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.

    > [!Note]  
    > Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée. AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.

     

2.  Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)        | Valeur                                            |
    |------------------------|--------------------------------------------------|
    | Conditions de filtrage   | Vide. Tout le trafic correspond au filtre.        |
    | **providerContextKey** | GUID du contexte du fournisseur MM ajouté à l’étape 1. |

        

**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de [**\_ \_ \_ \_ limite ND de l’indicateur de stratégie IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   Pour IKE, contexte du fournisseur de stratégie de type **FWPM le \_ \_ \_ \_ \_ contexte de transport QM IPsec IKE**.
    -   Pour AuthIP, contexte du fournisseur de stratégie de **type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context**. Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).

    > [!Note]  
    > Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée. AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.

     

2.  Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)        | Valeur                                            |
    |------------------------|--------------------------------------------------|
    | Conditions de filtrage   | Vide. Tout le trafic correspond au filtre.        |
    | **providerContextKey** | GUID du contexte du fournisseur QM ajouté à l’étape 1. |

        

**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**  

1.  Ajoutez un filtre avec les propriétés suivantes. 

    | Filter (propriété)                                                   | Valeur                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                                                              |
    | **action. calloutKey**                                             | **FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                    | [**\_sécurité de \_ \_ connexion entrante IPSec de \_ \_ contexte FWPM \_**](filter-context-identifiers.md) |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | \_autorisation d’action fwp \_                                                        |
    | **weight**                                                        | [**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**](filter-weight-identifiers.md)  |

        

**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**  

1.  Ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                               |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                                                     |
    | **action. calloutKey**                                             | **FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**                                    |
    | **rawContext**                                                    | [**\_détection de \_ \_ négociation sortante \_ IPSec \_ du contexte FWPM**](filter-context-identifiers.md) |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**                                   |

        

</dl>

> [!Note]  
> Par opposition au mode de transport de la découverte de négociation, pour le mode de transport de la découverte de négociation en mode de limite, il n’est pas nécessaire d’ajouter un filtre aux couches **FWPM d' \_ authentification ALE de la couche \_ ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}** car cette stratégie autorise les connexions entrantes non protégées en texte clair.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code : utilisation du mode de transport](using-transport-mode.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[**Identificateurs de légende intégrés**](built-in-callout-identifiers.md)
</dt> <dt>

[Conditions de filtrage](filtering-conditions.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**\_type de \_ contexte du fournisseur FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

