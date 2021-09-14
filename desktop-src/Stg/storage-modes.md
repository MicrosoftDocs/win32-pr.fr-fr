---
title: Stockage Façons
description: Le stockage asynchrone prend en charge deux modes de stockage bloquant et non bloquant, qu’un client (un navigateur ou l’objet lui-même) peut spécifier en retournant BINDF \_ ASYNCSTORAGE à partir de l’appel du moniker à IBindStatusCallback GetBindInfo.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827e893f5077a64485251111837e6b56657756f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013540"
---
# <a name="storage-modes"></a>Stockage Façons

Le stockage asynchrone prend en charge deux modes de stockage : le blocage et le non-blocage, qu’un client (un navigateur ou l’objet lui-même) peut spécifier en retournant BINDF \_ ASYNCSTORAGE à partir de l’appel du moniker à [**IBindStatusCallback :: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)). Si un client spécifie BINDF \_ ASYNCSTORAGE, il reçoit un pointeur vers un stockage asynchrone non bloquant. Dans le cas contraire, elle reçoit un pointeur vers un stockage asynchrone bloquant. Même si le client ne demande pas une opération de liaison asynchrone (en n’inscrivant pas [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) avec le contexte de liaison), le moniker retourne toujours un stockage asynchrone bloquant, ce qui permet le chargement progressif pour les applications héritées.

En mode non bloquant, un stockage asynchrone retourne E \_ en attente lorsque les données ne sont pas disponibles. Lors de la réception de ce message, le client attend une notification indiquant que des données supplémentaires sont disponibles avant de réessayer de le télécharger.

En mode blocage, au lieu de retourner E \_ en attente, le stockage asynchrone bloque l’appel jusqu’à ce que de nouvelles données soient disponibles, puis débloque l’appel et retourne les nouvelles données. Le client doit être prêt à recevoir les données. Pendant que le thread est bloqué, les données déjà transmises au client sont entièrement disponibles pour l’utilisateur.

Le mode blocage est nécessaire, car les clients ne connaissant pas le stockage asynchrone ne reconnaissent pas E \_ en attente et supposent qu’une erreur irrécupérable s’est produite. Le blocage du stockage asynchrone permet aux clients existants d’effectuer un rendu progressif.

 

 