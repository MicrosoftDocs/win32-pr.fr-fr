---
description: La plupart des opérations d’extraction et de définition traitent uniquement un composant d’informations. La fonction phoneGetStatus renvoie des informations d’État complètes sur un appareil téléphonique à une application.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: État (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864998"
---
# <a name="status-telephony-api"></a>État (API de téléphonie)

La plupart des opérations d’extraction et de définition traitent uniquement un composant d’informations. La fonction [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) renvoie des informations d’État complètes sur un appareil téléphonique à une application.

Comme mentionné précédemment, chaque fois qu’un élément d’état change sur le périphérique téléphonique, un message d' [**\_ État de téléphone**](phone-state.md) est envoyé à la fonction d’application. Les paramètres de ce message incluent un handle vers l’appareil téléphonique et une indication de l’élément d’État qui a changé.

Une application peut utiliser [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) pour sélectionner les modifications d’État spécifiques pour lesquelles elle souhaite être notifiée. En conséquence, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) retourne les modifications d’État pour lesquelles l’application souhaite être notifiée.

 

 



