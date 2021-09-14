---
title: Critères pour les entrées de service de nom
description: Critères pour les entrées de service de nom avec appel de procédure distante (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229199"
---
# <a name="criteria-for-name-service-entries"></a>Critères pour les entrées de service de nom

Les critères suivants sont utilisés lors du traitement des entrées de service de nom :

-   Si vous fournissez un nom d’entrée non **null** pour [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), cette entrée sera la seule entrée recherchée pour les handles de liaison. Si vous transmettez la **valeur null**, toutes les entrées de votre domaine d’ouverture de session sont recherchées. Notez que cela n’inclut pas les domaines approuvés.
-   Si vous fournissez un handle d’interface, les handles de liaison sont retournés à partir d’une entrée uniquement si la section d’interface de l’entrée contient une version compatible de cet UUID d’interface. Autrement dit, le numéro de version principale doit être identique à celui de l’interface UUID, tandis que le numéro de version mineure doit être supérieur ou égal au vôtre.
-   Si vous fournissez un UUID d’objet, les handles de liaison sont retournés à partir d’une entrée uniquement si la section UUID de l’objet de l’entrée contient cet UUID d’objet particulier.

Si une entrée de service de noms survit aux critères décrits ci-dessus, tous les descripteurs de liaison de ces entrées sont collectés. Les handles avec une séquence de protocole qui n’est pas prise en charge par le client sont ignorés et les descripteurs restants sont retournés en tant que sortie de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).

 

 




