---
description: Quand une nouvelle session de communication arrive, les applications TAPI qui ont inscrit un intérêt pour l’adresse et le type de média reçoivent une notification d’événement.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Répondre à une session lancée ailleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529499"
---
# <a name="respond-to-session-initiated-elsewhere"></a>Répondre à une session lancée ailleurs

Quand une nouvelle session de communication arrive, les applications TAPI qui ont inscrit un intérêt pour l' [adresse](address-ovr.md) et le [type de média](media-type-ovr.md) reçoivent une [notification d’événement](event-notification.md). Une seule application recevra [des privilèges](privilege-ovr.md) de propriété sur la session. Cette application ne peut pas refuser la session.

L’état d’appel initial d’une session entrante offre. Lorsque l’appel est dans l’état d’offre, une application peut obtenir des informations telles que le mode de support et la raison de l’appel, si les fournisseurs de services ont fourni ces informations et qu’elles sont disponibles. Certaines informations sur les appels peuvent ne pas être disponibles immédiatement, telles que l’ID de l’appelant.

Il existe six réponses de base à une session proposée : [réponse](answer-ovr.md), [acceptation](accept-ovr.md), [remise](handoffs-ovr.md), [supprimer](drop-ovr.md), [transférer](forward-ovr.md)et [Rediriger](redirect-ovr.md). En fonction du fournisseur de services, l’ensemble complet de ces opérations peut ne pas être disponible.

 

 



