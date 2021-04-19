---
title: Détails de l’implémentation DVC
description: Cette section contient des informations sur l’écriture d’un module client de canal virtuel dynamique (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508972"
---
# <a name="dvc-implementation-details"></a>Détails de l’implémentation DVC

Cette section contient des informations sur l’écriture d’un module client de canal virtuel dynamique (DVC).

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Écriture d’un module DVC client](writing-a-client-dvc-component.md)
</dt> <dd>

Pour écrire un module client de canal virtuel dynamique (DVC), vous devez d’abord implémenter et inscrire un plug-in client Connexion Bureau à distance (RDC).

</dd> <dt>

[Inscription du plug-in DVC](dvc-plug-in-registration.md)
</dt> <dd>

Décrit la syntaxe de l’entrée de plug-in de canal virtuel dynamique (DVC) pour le client Connexion Bureau à distance (RDC).

</dd> <dt>

[Démarrage d’un écouteur DVC](starting-a-dvc-listener.md)
</dt> <dd>

Pour établir une connexion réussie entre deux modules de canal virtuel dynamique (DVC) qui s’exécutent sur le client et le serveur Connexion Bureau à distance (RDC), un écouteur DVC doit être en cours d’exécution et dans un état d’écoute.

</dd> <dt>

[Acceptation d’une connexion](accepting-a-connection.md)
</dt> <dd>

À un moment donné, le client de canal virtuel dynamique (DVC) demande une connexion à l’écouteur DVC.

</dd> <dt>

[Écriture de données à l’aide d’un canal DVC](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

L’écriture de données de canal à l’aide d’un canal virtuel dynamique (DVC) est symétrique pour le serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance) et le client.

</dd> <dt>

[Test et débogage](testing-and-debugging.md)
</dt> <dd>

Il existe un écouteur « Echo » implémenté par le client Connexion Bureau à distance (RDC), qui est toujours présent et à l’écoute des connexions entrantes.

</dd> <dt>

[Exemple de plug-in client DVC](dvc-client-plug-in-example.md)
</dt> <dd>

Exemple de code C++ qui montre comment créer un plug-in de canal virtuel dynamique (DVC) de client Connexion Bureau à distance (RDC).

</dd> <dt>

[Exemple de module de serveur DVC](dvc-server-component-example.md)
</dt> <dd>

Exemple de code C++ qui montre comment créer le module de canal virtuel dynamique côté serveur (DVC).

</dd> </dl>

 

 




