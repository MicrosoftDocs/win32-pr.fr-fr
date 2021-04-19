---
title: Mode de transport de la découverte de négociation
description: Le scénario de stratégie IPsec de mode de transport de la découverte de négociation nécessite la protection du mode de transport IPsec pour tout le trafic entrant correspondant et demande une protection IPsec pour le trafic sortant correspondant.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216fec869eca28dc0661a37d44cce3a1fd05b80a
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314812"
---
# <a name="negotiation-discovery-transport-mode"></a>Mode de transport de la découverte de négociation

Le scénario de stratégie IPsec de mode de transport de la découverte de négociation nécessite la protection du mode de transport IPsec pour tout le trafic entrant correspondant et demande une protection IPsec pour le trafic sortant correspondant. Par conséquent, les connexions sortantes sont autorisées à revenir en texte clair alors que les connexions entrantes ne le sont pas.

Avec cette stratégie, lorsque l’ordinateur hôte tente une nouvelle connexion sortante et qu’il n’existe aucune association de sécurité IPsec correspondant au trafic, l’hôte envoie simultanément les paquets en texte clair et démarre une négociation IKE ou AuthIP. Si la négociation s’effectue correctement, la connexion est mise à niveau vers protégé par IPsec. Dans le cas contraire, la connexion reste en texte clair. Une fois qu’il est protégé par IPsec, une connexion ne peut jamais être rétrogradée en texte clair.

Le mode de transport de la découverte de négociation est généralement utilisé dans les environnements qui incluent des ordinateurs prenant en charge IPsec et non-IPsec.

Un exemple de scénario de mode de transport de découverte de négociation possible est « sécuriser tout le trafic de données de monodiffusion, sauf ICMP, en utilisant le mode de transport IPsec et l’activation de la découverte de négociation ».

Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.

<dl>

**Au niveau de la couche FWPM, \_ \_ IKEEXT \_ V {4 \| 6} configurer la stratégie de négociation mm**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.  
    -   Pour IKE, contexte d’un fournisseur de stratégie de type **FWPM \_ IPSec \_ IKE \_ mm \_ Context**.
    -   Pour AuthIP, contexte du fournisseur de stratégie de type **FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**.

    > [!Note]  
    > Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée. AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.

     

2.  Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes. 

    | Filter (propriété)        | Valeur                                            |
    |------------------------|--------------------------------------------------|
    | Conditions de filtrage   | Vide. Tout le trafic correspond au filtre.        |
    | **providerContextKey** | GUID du contexte du fournisseur MM ajouté à l’étape 1. |

        

**Au niveau de la \_ couche FWPM \_ \_ , IPSec V {4 \| 6} configurez la stratégie de négociation QM et em**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de sécurité de l' [**\_ indicateur de stratégie IPSec \_ \_ ND \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   Pour IKE, contexte du fournisseur de stratégie de type FWPM le \_ \_ contexte de \_ transport QM IPsec IKE \_ \_ .
    -   Pour AuthIP, contexte du fournisseur de stratégie de type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context. Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).

    > [!Note]  
    > Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée. AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.

     

2.  Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes. 

    | Filter (propriété)        | Valeur                                            |
    |------------------------|--------------------------------------------------|
    | Conditions de filtrage   | Vide. Tout le trafic correspond au filtre.        |
    | **providerContextKey** | GUID du contexte du fournisseur QM ajouté à l’étape 1. |

        

**Au niveau du \_ transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet entrant**  

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
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | [**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**](filter-weight-identifiers.md)  |

        

**Au niveau du \_ transport sortant de la couche FWPM \_ \_ \_ V {4 \| 6} configurer les règles de filtrage par paquets sortants**  

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

        

**Au niveau de FWPM \_ couche \_ ALE \_ auth \_ recv \_ Accept \_ V {4 \| 6} configurer les règles de filtrage par connexion entrantes**  

1.  Ajoutez un filtre avec les propriétés suivantes. Ce filtre n’autorise que les tentatives de connexion entrante s’ils sont sécurisés par IPsec. 

    | Filter (propriété)                                                   | Valeur                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                  |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                        |
    | **action. calloutKey**                                             | **\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}** |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**                                   |

        

</dl>

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

 

