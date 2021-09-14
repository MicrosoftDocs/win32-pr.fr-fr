---
title: À propos de l’administration du serveur et du port RAS
description: Les fonctions d’administration du serveur RAS obtiennent des informations sur un serveur RAS spécifié et ses ports. Ces fonctions sont également utilisées pour mettre fin à une connexion sur un port de serveur RAS spécifié.
ms.assetid: eedac23e-d716-451e-b08b-594398656bb5
keywords:
- Administration RAS RRAS, administration du serveur et du port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb9d3cc520efa6bbb492e8d9e967d423548f96a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007063"
---
# <a name="about-ras-server-and-port-administration"></a>À propos de l’administration du serveur et du port RAS

Les fonctions d’administration du serveur RAS obtiennent des informations sur un serveur RAS spécifié et ses ports. Ces fonctions sont également utilisées pour mettre fin à une connexion sur un port de serveur RAS spécifié.

La fonction [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) retourne une structure [**MPR \_ Server \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_server_0) qui contient des informations sur la configuration d’un serveur RAS. Les informations retournées incluent le nombre de ports actuellement disponibles pour les connexions, le nombre de ports en cours d’utilisation et le numéro de version du serveur.

La fonction [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) récupère un tableau de structures [**du \_ port RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) . Chaque structure contient des informations sur l’un des ports configurés sur un serveur RAS. Les informations de chaque port incluent :

-   Nom du port
-   Informations sur l’appareil attaché au port
-   si le serveur RAS associé au port est un serveur Windows NT/Windows 2000
-   Si le port est en cours d’utilisation et, si c’est le cas, des informations sur la connexion ;

Pour obtenir les ports utilisés par une connexion spécifique, transmettez [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) un handle à cette connexion dans le paramètre *hConnection* . Pour obtenir un descripteur d’une connexion, utilisez la fonction [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum) . Sinon, si vous avez implémenté une [dll d’administration RAS](ras-administration-dll.md), les fonctions [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection) et [**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2) reçoivent un handle pour chaque nouvelle connexion au moment où la connexion est établie.

Vous pouvez appeler la fonction [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) pour obtenir des informations supplémentaires sur un port spécifié sur un serveur RAS. Cette fonction retourne une structure de [**\_ port RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) qui contient une structure de [**\_ port RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) et des informations supplémentaires sur l’état actuel du port. La fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) retourne également un tableau de structures de [**\_ paramètres RAS**](ras-parameters-str.md) qui décrivent les valeurs de toutes les clés spécifiques au média associées au port. Une structure de **\_ paramètres RAS** utilise une valeur de l’énumération de [**\_ \_ format params**](ras-params-format-str.md) des paramètres d’accès distant pour indiquer le format de la valeur pour chaque clé spécifique au média.

La fonction [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) retourne également une structure de [**\_ \_ statistiques de port RAS**](ras-port-statistics-str.md) qui contient différents compteurs de statistiques pour la connexion actuelle, le cas échéant, sur le port. Pour un port qui fait partie d’une connexion à liaisons multiples, **MprAdminPortGetInfo** retourne des statistiques pour le port individuel et des statistiques cumulatives pour tous les ports impliqués dans la connexion. Vous pouvez utiliser la fonction [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) pour réinitialiser les compteurs des statistiques du port. La fonction [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) déconnecte un port en cours d’utilisation.

Utilisez la fonction [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) pour libérer de la mémoire allouée par les fonctions [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) et [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) . Utilisez la fonction [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) pour obtenir une chaîne qui décrit un code d’erreur RAS renvoyé par l’une des fonctions d’administration de serveur RAS (RasAdmin).

 

 




