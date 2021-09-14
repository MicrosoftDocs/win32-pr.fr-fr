---
title: Modification d’une interface existante
description: Dans la mesure du possible, implémentez une nouvelle interface pour votre application, au lieu d’apporter des modifications à une interface existante.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- modification des interfaces existantes 64-bit Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a656ee768dcc2e88725d2cff0ddc5604fd771f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008302"
---
# <a name="changing-an-existing-interface"></a>Modification d’une interface existante

Dans la mesure du possible, implémentez une nouvelle interface pour votre application, au lieu d’apporter des modifications à une interface existante. Si vous ne pouvez pas éviter de modifier une interface existante, utilisez de nouveaux types de données uniquement dans les nouvelles méthodes. L’introduction d’un nouveau type de données ou la modification d’un type existant est la source la plus courante de problèmes d’incompatibilité. Le modèle d’exécution RPC suppose que l’application réceptrice connaît les types de données qu’elle reçoit, de sorte que les données sont placées sur le réseau sans une description de données générique. Lorsque le destinataire attend un type de données différent de celui que l’expéditeur a placé sur le câble, le stub lève une exception (ou la transmission échoue de manière moins appropriée).

Une interface RPC est définie par son UUID et ses numéros de version majeure et mineure. Lorsque vous modifiez une interface existante, vous devez ajouter les nouvelles méthodes à la fin de l’interface et modifier le numéro de version mineure. Si vous ajoutez des méthodes ailleurs ou apportez d’autres modifications à l’interface, vous devez également modifier le numéro de version principale.

En réalité, il existe des cas où vous ne pouvez pas modifier même le numéro de version mineure, car un nouveau client ne pourra pas communiquer avec un ancien serveur et vous ne pourrez pas mettre à jour le serveur. Le temps d’exécution RPC lève une exception, \_ RPC \_ S \_ PROCNUM \_ hors \_ limites, lorsqu’un client appelle une méthode au-delà de celles spécifiées pour son interface avec le serveur. La solution de contournement consiste à ne pas modifier les numéros de version et à écrire votre code client pour gérer cette exception de manière appropriée, par le client dégrader ses performances, par exemple, ou par n’importe quel moyen adapté à votre application.

Il existe une solution de contournement similaire pour un cas particulier de modification d’un type de données dans une méthode existante. Si vous avez une [**Union**](/windows/desktop/Midl/union) dont les branches sont des pointeurs et que n’a pas de branche par défaut pour les types non reconnus, vous pouvez ajouter une nouvelle branche qui utilise le nouveau type de données. Cela ne modifie pas la taille de la structure de données. Lorsque votre client parle à un nouveau serveur, il peut utiliser le nouveau type de données. Toutefois, lorsque votre client parle à un ancien serveur, le temps d’exécution génère la balise d’exception RPC \_ \_ non valide \_ . Là encore, vous devrez écrire votre code client pour gérer cette exception de manière appropriée.

Une interface DCOM est identifiée par son GUID. Dans DCOM, les interfaces sont considérées comme immuables et vous pouvez apporter des modifications uniquement en créant une nouvelle interface qui hérite de l’ancienne. Ces règles garantissent que les clients et les serveurs restent compatibles.

 

 