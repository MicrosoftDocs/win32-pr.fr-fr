---
description: L’arrêt correct des sessions de communication et d’une application complète est nécessaire pour empêcher les ressources de rester liées dans les appels ou les applications qui n’en ont plus besoin.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Arrêt de l’interface TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416307"
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



 

 

 
