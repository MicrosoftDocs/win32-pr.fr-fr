---
description: La fonction phoneDevSpecific et son \_ message DEVSPECIFIC téléphone associé permettent à une application d’accéder à des fonctionnalités de téléphone spécifiques à l’appareil qui ne sont pas disponibles via les services de téléphonie courants pour les téléphones.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Fonctions et messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951963"
---
# <a name="functions-and-messages"></a>Fonctions et messages

La fonction [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) et son message [**\_ DEVSPECIFIC téléphone**](phone-devspecific.md) associé permettent à une application d’accéder à des fonctionnalités de téléphone spécifiques à l’appareil qui ne sont pas disponibles via les services de téléphonie courants pour les téléphones. En d’autres termes, **phoneDevSpecific** est la fonction d’échappement propre au périphérique qui autorise les extensions dépendantes du fournisseur, et Phone \_ DEVSPECIFIC est le message spécifique à l’appareil qui est envoyé à l’application.

Le profil de paramètre de la fonction [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) est générique dans cette légère interprétation des paramètres effectuée par l’interface TAPI. Au lieu de cela, l’interprétation des paramètres est définie par le fournisseur de services et doit être comprise par une application qui les utilise. Les paramètres sont simplement transmis par l’interface TAPI de l’application au fournisseur de services. Une application qui s’appuie sur des extensions spécifiques à l’appareil ne fonctionne généralement pas avec d’autres fournisseurs de services, mais les applications écrites dans les services téléphoniques courants fonctionnent avec le fournisseur de services étendu.

 

 



