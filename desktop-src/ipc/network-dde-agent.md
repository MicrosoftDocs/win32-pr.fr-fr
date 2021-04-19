---
description: L’agent DDE réseau démarre le DDE réseau s’il détecte une activité DDE de réseau local.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Agent DDE réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516820"
---
# <a name="network-dde-agent"></a>Agent DDE réseau

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

L’agent DDE réseau démarre le DDE réseau s’il détecte une activité DDE de réseau local. Il ne détecte pas un client distant tentant de se connecter. Par conséquent, avant qu’un client puisse se connecter, DDE réseau doit être démarré sur l’ordinateur serveur. Notez que le DDE réseau n’est pas démarré par défaut. Pour démarrer le DDE réseau, exécutez NETDDE.EXE. Ce fichier se trouve dans votre répertoire Windows.

L’agent DDE réseau démarre également les applications nécessaires pour DDE réseau. Une fois le DDE réseau démarré, les conversations DDE sont contrôlées via une fenêtre DDE réseau associée à l’une des applications DDE réseau. Cette application agit comme un proxy. Il communique avec toutes les applications DDE locales et distantes.

 

 



