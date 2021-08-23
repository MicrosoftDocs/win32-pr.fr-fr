---
title: Gestion des objets
description: cette section décrit l’utilisation correcte des types d’objets de l’API de la plateforme de filtrage Windows (WFP).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cb51d4e78049d7911a4a5ed265091e05bc1cbb00ce470e332d59dd23c6026d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068849"
---
# <a name="object-management"></a>Gestion des objets

cette section décrit l’utilisation correcte des types d’objets de l’API de la plateforme de filtrage Windows (WFP).

## <a name="sessions"></a>Sessions

L’API WFP est orientée session, et la plupart des appels de fonction sont effectués dans le contexte d’une session. Une nouvelle session cliente est créée en appelant [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La session se termine lorsque le client appelle [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) ou que le processus client se termine. Lorsqu’une session est détruite, soit à des fins, soit par l’arrêt RPC, le moteur de filtrage de base (BFE) abandonne tout d’abord toute transaction existante.

Lors de la création d’une nouvelle session, l’appelant peut créer une session dynamique en passant l’indicateur dynamique de l' [**\_ \_ indicateur \_ de session FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) à [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Tout objet ajouté au cours d’une session dynamique est automatiquement supprimé à la fin de la session.

## <a name="transactions"></a>Transactions

L’API WFP est transactionnelle, et la plupart des appels de fonction sont effectués dans le contexte d’une transaction. Les appelants peuvent utiliser [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0), [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)et [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) pour contrôler explicitement les transactions. Toutefois, si un appel de fonction est effectué en dehors d’une transaction explicite, il est exécuté dans une transaction implicite. Si une transaction est en cours, lorsqu’une session se termine, elle est automatiquement abandonnée. Les transactions implicites ne sont jamais abandonnées de force.

Les transactions sont en lecture seule ou en lecture/écriture et appliquent une sémantique rigoureusement fiable, à durabilité atomique ([acid](../cossdk/acid-properties.md)).

Chaque session cliente ne peut avoir qu’une seule transaction en cours à la fois. Si l’appelant tente de commencer une deuxième transaction avant de valider ou d’abandonner le premier, BFE renvoie une erreur.

Si une opération échoue au cours d’une transaction, elle n’affecte pas l’état global de la transaction. Par exemple, supposons que le client commence une transaction et appelle [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) trois fois avant l’échec d’un quatrième appel. Le client a désormais la possibilité de :

-   Abandon de la transaction, auquel cas aucun des filtres ne sera ajouté.
-   La validation de la transaction, auquel cas les trois premiers filtres sont ajoutés.
-   Poursuivre avec davantage d’opérations, y compris une nouvelle tentative potentielle d’échec de [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

Au début d’une transaction, BFE attend que le [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) de la session expire pour acquérir le verrou. Si le verrou n’est pas acquis dans ce délai, l’acquisition de verrou (et l’appel [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) ) échoue. Cela évite que les clients ne parviennent pas indéfiniment à répondre. Si le client n’a pas spécifié de délai d’attente de verrouillage, sa valeur par défaut est de 15 secondes.

Chaque transaction a également un délai de verrouillage. Il s’agit de la durée maximale pendant laquelle il peut être propriétaire du verrou. Si le propriétaire ne libère pas le verrou dans ce délai, la transaction est abandonnée de force, ce qui entraîne la libération du verrou. Le délai d’attente de verrouillage n’est pas configurable. Elle est infinie pour les appelants en mode noyau et une heure pour les appelants en mode utilisateur. Si une transaction est abandonnée de force, l’appel suivant effectué dans la transaction échoue avec l' **abandon de l' \_ \_ TXN \_ fwp E**.

## <a name="object-lifetimes"></a>Durées de vie des objets

Les objets peuvent avoir l’une des quatre durées de vie possibles :

-   Dynamique : un objet est dynamique uniquement s’il est ajouté à l’aide d’un handle de session dynamique. Objets dynamiques en direct jusqu’à ce qu’ils soient supprimés ou que la session propriétaire se termine.
-   Statiques : les objets sont statiques par défaut. Objets statiques actifs jusqu’à ce qu’ils soient supprimés, BFE s’arrête ou le système est arrêté.
-   Persistants : les objets persistants sont créés en passant l’indicateur **\_ \* \_ \_ persistant de l’indicateur FWPM** approprié à une fonction **FWPM \* Add0** . Objets persistants en direct jusqu’à ce qu’ils soient supprimés.
-   Intégré : les objets intégrés sont prédéfinis par BFE et ne peuvent pas être ajoutés ou supprimés. Ils vivent toujours.

Les filtres des couches en mode noyau peuvent être marqués comme filtres au moment du démarrage en passant l’indicateur approprié à [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). Les filtres au moment du démarrage sont ajoutés au système lorsque le pilote TCP/IP démarre et supprimés lors de la fin de l’initialisation de BFE. Les objets persistants sont ajoutés au démarrage de BFE.

Dans de nombreux cas, il est possible qu’un fournisseur de stratégie ne souhaite pas que sa stratégie persistante soit appliquée si le fournisseur a été désactivé. lorsque vous ajoutez un fournisseur, l’appelant peut spécifier un nom de service Windows facultatif. Lors de l’ajout d’objets persistants, l’appelant peut éventuellement spécifier le fournisseur qui « possède » cet objet. au démarrage du service, BFE ajoute uniquement les objets persistants au système s’ils ne sont pas associés à un fournisseur, ou si le fournisseur associé n’a pas de nom de service Windows, ou si le service de Windows associé est configuré pour démarrer automatiquement.

## <a name="object-associations"></a>Associations d’objets

Certains objets comportent des références à d’autres objets. Par exemple, un filtre fait toujours référence à une couche et peut faire référence à une légende et à un contexte de fournisseur. Les objets ne peuvent pas faire référence à des objets qui peuvent avoir une durée de vie plus réduite. Ainsi, un objet dynamique ne peut pas faire référence à un objet dynamique à partir d’une autre session. Un objet statique ne peut pas faire référence à un objet dynamique. Un objet persistant ne peut pas faire référence à un objet dynamique, à un objet statique ou à un objet persistant appartenant à un autre fournisseur.

Un objet ne peut pas être supprimé tant que tous les objets qui y font référence n’ont pas été supprimés.

## <a name="luids-and-guids"></a>LUID et GUID

Tous les objets API WFP en mode utilisateur (FWPM) sont identifiés par un identificateur global unique (**GUID**) et font référence à d’autres objets par leur **GUID**. Le **GUID** doit uniquement être unique dans le type d’objet. Par exemple, un filtre et un contexte de fournisseur peuvent avoir le même **GUID**, mais deux filtres ne le peuvent pas. Lors de l’ajout d’un nouvel objet, les appelants peuvent assigner le **GUID** de l’objet ou le laisser initialisé à zéro et laisser BFE attribuer le **GUID**.

Tous les objets API WFP en mode noyau (FWPS) sont identifiés par un identificateur unique local (**LUID**) et référencent d’autres objets par leur LUID. Le passage du **GUID** au **LUID** permet à WFP de conserver les pools non paginés et d’optimiser le traitement au moment de l’exécution. La largeur du **LUID** dépend du type d’objet et des plages d’un **UINT16** à un **UINT64**. Les **LUID** s sont toujours attribuées par BFE.

 

 