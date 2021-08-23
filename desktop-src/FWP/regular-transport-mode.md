---
title: mode de transport
description: Le scénario de stratégie IPsec en mode de transport requiert la protection du mode de transport IPsec pour tout le trafic correspondant.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebfb6dad27340bfc72397307c58fddfe2bdf6eeadb65081faa0e1941de2c052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535889"
---
# <a name="transport-mode"></a>mode de transport

Le scénario de stratégie IPsec en mode de transport requiert la protection du mode de transport IPsec pour tout le trafic correspondant. Tout trafic en texte clair correspondant est supprimé jusqu’à ce que la négociation IKE ou AuthIP s’est terminée avec succès. Si la négociation échoue, la connectivité avec l’adresse IP correspondante reste ininterrompue.

Un exemple de scénario de mode de transport possible est « sécuriser tout le trafic de données monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec ».

Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.

<dl>

**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**  

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

        

**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux.  
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

    | Filter (propriété)                                                   | Valeur                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **action. type**                                                   | fin de l’appel à l' \_ action fwp \_ \_                             |
    | **action. calloutKey**                                             | FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}             |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                  | Valeur                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                               |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**            | IPPROTO \_ ICMP {V6} ces constantes sont définies dans Winsock2. h.<br/>    |
    | **action. type**                                                  | \_autorisation d’action fwp \_                                                       |
    | **weight**                                                       | [**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**](filter-weight-identifiers.md) |

        

**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**  

1.  Ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                        |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**              |
    | **action. calloutKey**                                             | FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6} |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                            |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | IPPROTO \_ ICMP {V6} ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | \_autorisation d’action fwp \_                                                    |
    | **weight**                                                        | \_ \_ \_ exemptions IKE de la plage de poids FWPM \_                                   |

        

</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code : utilisation du mode de transport](using-transport-mode.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Types de contexte du fournisseur**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Conditions de filtrage](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Identificateurs de légende intégrés**](built-in-callout-identifiers.md)
</dt> </dl>

 

