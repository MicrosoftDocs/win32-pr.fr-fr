---
description: L’arrêt correct des sessions de communication et d’une application complète est nécessaire pour empêcher les ressources de rester liées dans les appels ou les applications qui n’en ont plus besoin.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Arrêt de l’interface TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88303d2475a2ce0a21478575483c0fd93e44e96b71efa83790b7973343d6d9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080439"
---
# <a name="tapi-shutdown"></a>Arrêt de l’interface TAPI

L’arrêt correct des sessions de communication et d’une application complète est nécessaire pour empêcher les ressources de rester liées dans les appels ou les applications qui n’en ont plus besoin.

L’interface TAPI fournit une série de fonctions et de méthodes pour vous aider dans le processus. Évidemment, l’application doit également prendre la responsabilité de libérer correctement la mémoire allouée, que ce soit sous la forme de structures de données ou de références COM.



| Fonctions TAPI 2. x                                                            | Description                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Annule l’inscription de l’application en tant que gestionnaire pour les appels de téléphonie assistés. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Déconnecte l’application en tant que responsable des appels sur la ligne donnée.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Arrête l’utilisation de l’application de l’abstraction de ligne.            |



 



| Interfaces ou méthodes TAPI 3. x                                            | Description                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Supprime toutes les inscriptions de notifications d’événements effectuées par l’application. |
| [**ITTAPI :: Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Déconnecte l’application en tant que gestionnaire d’appels.                             |



 

 

 
