---
title: Administration du serveur et du port RAS
description: Les fonctions d’administration du serveur RAS vous permettent d’obtenir des informations sur un serveur RAS spécifié et ses ports. Ces fonctions vous permettent également de mettre fin à une connexion sur un port de serveur RAS spécifié.
ms.assetid: 783b0ded-7c0e-49eb-8040-563d5dd675f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d09d683bf0850b5f51a5d9c1ac1aa21b25f2968ddedbed2d383d28dad7785f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028799"
---
# <a name="ras-server-and-port-administration"></a>Administration du serveur et du port RAS

Les fonctions d’administration du serveur RAS vous permettent d’obtenir des informations sur un serveur RAS spécifié et ses ports. Ces fonctions vous permettent également de mettre fin à une connexion sur un port de serveur RAS spécifié.

La fonction [**RasAdminServerGetInfo**](rasadminservergetinfo.md) retourne une structure du [**\_ serveur RAS \_ 0**](ras-server-0-str.md) qui contient des informations sur la configuration d’un serveur RAS. Les informations retournées incluent le nombre de ports actuellement disponibles pour la connexion, le nombre de ports en cours d’utilisation et le numéro de version du serveur.

La fonction [**RasAdminPortEnum**](rasadminportenum.md) récupère un tableau des structures [**du \_ port RAS \_ 0**](ras-port-0-str.md) qui contient des informations sur chacun des ports configurés sur un serveur RAS. Les informations de chaque port incluent :

-   Nom du port
-   Informations sur l’appareil attaché au port
-   si le serveur RAS associé au port est un serveur Windows NT/Windows 2000
-   Si le port est en cours d’utilisation et, si c’est le cas, des informations sur la connexion ;

Vous pouvez appeler la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) pour obtenir des informations supplémentaires sur un port spécifié sur un serveur RAS. Cette fonction retourne une structure de [**\_ port RAS \_ 1**](ras-port-1-str.md) qui contient une structure de [**\_ port RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) et des informations supplémentaires sur l’état actuel du port. La fonction **RasAdminPortGetInfo** retourne également un tableau de structures de [**\_ paramètres RAS**](ras-parameters-str.md) qui décrivent les valeurs de toutes les clés spécifiques au média associées au port. Une structure de **\_ paramètres RAS** utilise une valeur de l’énumération de [**\_ \_ format params**](ras-params-format-str.md) des paramètres d’accès distant pour indiquer le format de la valeur pour chaque clé spécifique au média.

La fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) retourne également une structure de [**\_ \_ statistiques de port RAS**](ras-port-statistics-str.md) qui contient différents compteurs de statistiques pour la connexion actuelle, le cas échéant, sur le port. Pour un port qui fait partie d’une connexion à liaisons multiples, **RasAdminPortGetInfo** retourne des statistiques pour le port individuel et des statistiques cumulatives pour tous les ports impliqués dans la connexion. Vous pouvez utiliser la fonction [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) pour réinitialiser les compteurs des statistiques du port. La fonction [**RasAdminPortDisconnect**](rasadminportdisconnect.md) déconnecte un port en cours d’utilisation.

Utilisez la fonction [**RasAdminFreeBuffer**](rasadminfreebuffer.md) pour libérer de la mémoire allouée par les fonctions [**RasAdminPortEnum**](rasadminportenum.md) et [**RasAdminPortGetInfo**](rasadminportgetinfo.md) . Utilisez la fonction [**RasAdminGetErrorString**](rasadmingeterrorstring.md) pour obtenir une chaîne qui décrit un code d’erreur RAS renvoyé par l’une des fonctions d’administration de serveur RAS (RasAdmin).

 

 




