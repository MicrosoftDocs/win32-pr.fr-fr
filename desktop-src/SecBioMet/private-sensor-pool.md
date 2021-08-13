---
title: Pool de capteurs privés
description: Collection d’unités biométriques réservée pour une utilisation exclusive par une application cliente. Les pools privés prennent en charge les méthodes d’authentification propriétaires et permettent à une application cliente d’accéder à une unité biométrique à l’aide de commandes de contrôle spécifiées par le fournisseur.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306f4e0d4e28cfb29dda694e835348721113a5c23ec51054169537282ae2c365
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480439"
---
# <a name="private-sensor-pool"></a>Pool de capteurs privés

Un pool de capteurs privé est une collection d’unités biométriques réservée pour une utilisation exclusive par une application cliente. Les pools privés prennent en charge les méthodes d’authentification propriétaires et permettent à une application cliente d’accéder à une unité biométrique à l’aide de commandes de contrôle spécifiées par le fournisseur. Unités biométriques dans un pool de capteurs privés :

-   Sont uniquement disponibles pour l’application cliente qui a créé le pool.
-   Envoyer des notifications d’événements générées par l’achèvement des opérations biométriques directement à l’application, sans tenir compte du focus de la fenêtre active.
-   Utilisez des GUID pour identifier les modèles biométriques.
-   Partager une base de données de modèle sélectionnée pour une application unique.

Les pools de capteurs privés doivent être utilisés si l’application cliente :

-   Gère une collection d’unités biométriques dédiées qui utilisent une base de données de modèle propre à l’application. Prenons l’exemple d’une application de participation des employés dans laquelle les employés signalent leur arrivée au travail en passant leur doigt sur un lecteur d’empreintes digitales. les employés n’ont pas de comptes de Windows sur l’ordinateur qui exécute l’application. Au lieu de cela, leurs empreintes digitales sont identifiées par des GUID gérés par l’application de présence.
-   Collecte des exemples biométriques plutôt que de mapper simplement des exemples à des SID.
-   Place le matériel d’unités biométriques en mode de maintenance pour mettre à jour le microprogramme.
-   Envoie des commandes de contrôle définies par le fournisseur au matériel ou au logiciel biométrique.
-   Tente de configurer une unité biométrique avec stockage intégré pour fonctionner en mode avancé, mais l’unité ne peut pas effectuer les opérations de hachage requises.
-   S’exécute à partir d’une session cliente Bureau à distance.

> [!Note]  
> Les applications peuvent créer des pools de capteurs privés pour l’identification biométrique uniquement. Si une application tente d’en créer une pour n’importe quel autre (par exemple, face), la demande échoue.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un pool de capteurs privé](creating-a-private-sensor-pool.md)
</dt> <dt>

[Pools de capteurs](sensor-pools.md)
</dt> <dt>

[Pool de capteurs système](system-sensor-pool.md)
</dt> </dl>

 

 




