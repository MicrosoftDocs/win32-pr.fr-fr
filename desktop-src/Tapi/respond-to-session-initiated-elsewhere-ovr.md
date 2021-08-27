---
description: Quand une nouvelle session de communication arrive, les applications TAPI qui ont inscrit un intérêt pour l’adresse et le type de média reçoivent une notification d’événement.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Répondre à une session lancée ailleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74554b48919f7532561bfdf0bab7a163a58fbeb3734dc15e4a8d7e0869dad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072849"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Répondre à une session lancée ailleurs

Quand une nouvelle session de communication arrive, les applications TAPI qui ont inscrit un intérêt pour l' [adresse](address-ovr.md) et le [type de média](media-type-ovr.md) reçoivent une [notification d’événement](event-notification.md). Une seule application recevra [des privilèges](privilege-ovr.md) de propriété sur la session. Cette application ne peut pas refuser la session.

L’état d’appel initial d’une session entrante offre. Lorsque l’appel est dans l’état d’offre, une application peut obtenir des informations telles que le mode de support et la raison de l’appel, si les fournisseurs de services ont fourni ces informations et qu’elles sont disponibles. Certaines informations sur les appels peuvent ne pas être disponibles immédiatement, telles que l’ID de l’appelant.

Il existe six réponses de base à une session proposée : [réponse](answer-ovr.md), [acceptation](accept-ovr.md), [remise](handoffs-ovr.md), [supprimer](drop-ovr.md), [transférer](forward-ovr.md)et [Rediriger](redirect-ovr.md). En fonction du fournisseur de services, l’ensemble complet de ces opérations peut ne pas être disponible.

 

 



