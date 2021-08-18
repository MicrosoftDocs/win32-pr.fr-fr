---
title: Réautorisation ALE
description: le trafic réseau au niveau des couches de mise en œuvre de la couche application (ALE) de la plateforme de filtrage de Windows (WFP) est filtré par les flux ALE.
ms.assetid: 3cc7f78e-3f9d-4a91-8ea0-9b64c299068a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850cd7f789c1fb1222a0d6820e84a42cf41763dac4e57b96667e7feda364374c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582689"
---
# <a name="ale-reauthorization"></a>Réautorisation ALE

le trafic réseau au niveau des couches de mise en œuvre de la couche application (ALE) de la plateforme de filtrage de Windows (WFP) est filtré par les [flux ALE](ale-stateful-filtering.md). Une fois qu’un flux ALE est autorisé, tout le trafic qui fait partie du flux ALE est autorisé. La réautorisation est une demande de validation des autorisations du fluide ALE, généralement en raison d’une modification de la stratégie réseau.

Les flux ALE se voient attribuer une direction, entrante ou sortante, en fonction de la direction du premier paquet qui a déclenché la création et l’autorisation du flux. Les flux ALE entrants sont créés et autorisés au niveau de la couche [**FWPM d' \_ authentification ALE de la couche \_ ALE \_ \_ reçues \_ Accept \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) . Les flux ALE sortants sont créés et autorisés au niveau de la couche **FWPM d' \_ authentification ALE de couche \_ ALE \_ \_ \_ V {4 \| 6}** . La direction du fluide ALE ne limite pas la direction des paquets qui appartiennent au Flow. Les flux ALE contiennent des paquets entrants et sortants, quelle que soit la direction du flux ALE lui-même.

La réautorisation d’un fluide ALE est déclenchée par :

-   Une modification de stratégie au niveau de la couche où le Flow ALE était autorisé ou créé à l’origine.
-   Interface d’arrivée différente de l’interface dans laquelle le Flow ALE a été initialement autorisé ou créé.
-   Connexion en attente.

La réautorisation est distinguée de l’autorisation initiale par la présence de l' [**indicateur de condition fwp est l’indicateur de \_ \_ \_ \_ réautorisation**](filtering-condition-flags-.md) .

La réautorisation ne peut être effectuée qu’au niveau des couches FWPM d’authentification ALE de la couche ALE **\_ \_ \_ \_ - \_ \|** accepter les niveaux [**\_ \_ \_ \_ \_ \_ {4 \| 6}**](management-filtering-layer-identifiers-.md) et FWPM.

### <a name="policy-change-reauthorization"></a>Stratégie-réautorisation des modifications

Une modification de stratégie est implémentée sous la forme d’un ajout ou d’une suppression de filtre au niveau d’une couche ALE. Une fois qu’une modification de stratégie est détectée, le premier paquet qui traverse un workflow ALE créé dans la couche affectée sera spécifié pour la réautorisation dans la couche. Par conséquent, pour la réautorisation, il est tout à fait possible qu’un paquet sortant soit classé au niveau de la couche [**FWPM d' \_ \_ \_ authentification \_ \_ \_ \| ALE**](management-filtering-layer-identifiers-.md) de la couche ALE et qu’un paquet entrant soit classé au niveau de la couche **FWPM \_ \_ ALE \_ auth \_ Connect Connect \_ v {4 \| 6}** .

L’une des raisons de cette classification à sens mixte est qu’il n’y a peut-être pas de trafic réseau à partir de la direction d’origine (par exemple, le paquet entrant pour le flux ALE entrant). Un exemple de ce type est le streaming UDP unidirectionnel après une négociation bidirectionnelle initiale. Dans ce cas, il est plus souhaitable de détruire la diffusion le plus rapidement possible.

### <a name="arrival-interface-reauthorization"></a>Réautorisation de l’interface d’arrivée

la réautorisation de l’interface d’arrivée est disponible à partir de Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

Les paquets appartenant au même flot ALE peuvent arriver à partir de plusieurs interfaces. Le premier paquet à venir sur une interface différente de l’interface d’origine du fluide ALE est réautorisé.

Dans un modèle d’hôte fort, qui est le modèle de sécurité par défaut pour la pile TCP/IP, une connexion sur une interface réseau accepte uniquement les paquets qui arrivent sur la même interface. Par conséquent, la réautorisation de l’interface de réception n’est pas utilisée sur un ordinateur hôte fort.

Dans un modèle d’hôte faible, une connexion sur une interface réseau autorise les paquets entrants sur n’importe quelle autre interface réseau. La réautorisation de l’interface d’arrivée est utilisée sur un ordinateur hôte faible pour implémenter des stratégies spécifiques à l’interface. Pour plus d’informations, consultez [« the Cable Guy : forts et faibles des modèles d’hôte ».](/previous-versions/technet-magazine/cc137807(v=msdn.10))

Certains [champs classés](filtering-conditions.md) peuvent être inconnus lors de la réautorisation. Par exemple, si un paquet sortant est en cours de réautorisation au niveau de la couche FWPM d’authentification ALE de la [**\_ couche \_ ALE \_ \_ \_ \_ \|**](management-filtering-layer-identifiers-.md) , les champs relatifs à l’interface d’arrivée sont inconnus. Dans ce cas, les valeurs des champs inconnus sont indiquées sous la forme [**fwp \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

Les champs de type [**fwp \_ Empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) peuvent être mis en correspondance avec l’équivalent de la [**\_ correspondance \_ fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type). Par conséquent, une stratégie peut être définie de façon à bloquer les réautorisations et à détruire un fluide ALE lorsque les demandes de réautorisation du flot ALE arrivent.

## <a name="pending-connection-reauthorization"></a>Réautorisation de connexion en attente

Un pilote de légende peut reporter une opération de classification à des couches ALE et le terminer ultérieurement, lorsque la décision de filtrage peut être effectuée en toute sécurité. La fonctionnalité de report/final ALE est prise en charge via les fonctions en mode noyau [FwpsPendOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpspendoperation0) et [FwpsCompleteOperation0](/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscompleteoperation0).

La réautorisation est déclenchée immédiatement après l’appel FwpsCompleteOperation0 et permet au pilote de légende d’autoriser ou de bloquer le Workflow.

Seule une autorisation initiale peut être reportée. Un appel à FwpsPendOperation0 échoue si l’indicateur de condition fwp est défini sur l’indicateur de [**\_ \_ \_ \_ réautorisation**](filtering-condition-flags-.md) .

pour plus d’informations, consultez la documentation du [Kit de pilotes Windows](/windows-hardware/drivers/ddi/_netvista/) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Application de la couche application (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[Filtrage avec état ALE](ale-stateful-filtering.md)
</dt> <dt>

[Trafic de diffusion/multidiffusion ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[personnalisation de la Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 