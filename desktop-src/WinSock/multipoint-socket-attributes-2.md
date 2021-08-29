---
description: attributs de socket Multipoint dans Windows sockets (Winsock).
ms.assetid: f6e779c6-dd9d-470e-aad9-715b69ad8c5f
title: Attributs de socket multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992f574420743ec8e6a339fe14a29accb68beff2c416de0dde19c0fafc707acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858149"
---
# <a name="multipoint-socket-attributes"></a>Attributs de socket multipoint

Dans certains cas, les sockets joints à une session multipoint peuvent présenter des différences de comportement par rapport aux sockets point-à-point. Par exemple, un \_ Socket de feuille d dans un schéma de plan de données enraciné peut uniquement envoyer des informations au \_ participant racine d. Cela crée un besoin pour que le client soit en mesure d’indiquer que l’utilisation prévue d’un socket coïncide avec sa création. Cela s’effectue par le biais de quatre indicateurs d’attribut multipoint qui peuvent être définis par le biais du paramètre *dwFlags* dans [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket):

-   La \_ \_ racine multipoint \_ c \_ de l’indicateur WSA, pour la création d’un socket agissant comme \_ racine c, et autorisée uniquement si un plan de contrôle enraciné est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.
-   La \_ \_ feuille multipoint \_ c de l’indicateur WSA \_ , pour la création d’un socket agissant comme une \_ feuille c, et autorisée uniquement si XP1 \_ prend en charge \_ multipoint, est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.
-   La \_ \_ racine multipoint \_ d de l’indicateur WSA \_ , pour la création d’un socket agissant comme \_ racine d, et autorisée uniquement si un plan de données enraciné est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.
-   \_Nœud WSA \_ multipoint \_ D \_ , pour la création d’un socket agissant comme une feuille D \_ , et autorisé uniquement si XP1 \_ prend en charge \_ multipoint, est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.

Lorsque vous créez un socket multipoint, l’un des deux indicateurs du plan de contrôle, et l’un des deux indicateurs du plan de données, doivent être définis dans le paramètre *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Par conséquent, les quatre possibilités pour la création de sockets multipoint sont : "c \_ racine/d racine \_ ", "c \_ racine/d \_ feuille", "c \_ feuille/d \_ racine" ou "c \_ feuille/d \_ feuille".

 

 
