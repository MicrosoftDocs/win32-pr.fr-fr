---
description: Dans certains cas, les sockets joints à une session multipoint peuvent présenter des différences de comportement par rapport aux sockets point-à-point.
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Bits d’indicateur pour WSASocket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515239"
---
# <a name="flag-bits-for-wsasocket"></a>Bits d’indicateur pour WSASocket

Dans certains cas, les sockets joints à une session multipoint peuvent présenter des différences de comportement par rapport aux sockets point-à-point. Par exemple, un \_ Socket de feuille d dans un schéma de plan de données enraciné peut uniquement envoyer des informations au \_ participant racine d. Cela crée un besoin pour que l’application soit en mesure d’indiquer que l’utilisation prévue d’un socket coïncide avec sa création. Pour ce faire, vous pouvez utiliser des bits à quatre indicateurs qui peuvent être définis dans le paramètre *dwFlags* sur [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):

-   La \_ \_ racine multipoint \_ c \_ de l’indicateur WSA, pour la création d’un socket agissant comme \_ racine c, et autorisée uniquement si un plan de contrôle enraciné est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.
-   La \_ \_ feuille multipoint \_ c de l’indicateur WSA \_ , pour la création d’un socket agissant comme une \_ feuille c, et autorisée uniquement si XP1 \_ prend en charge \_ multipoint, est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.
-   La \_ \_ racine multipoint \_ d de l’indicateur WSA \_ , pour la création d’un socket agissant comme \_ racine d, et autorisée uniquement si un plan de données enraciné est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.
-   \_Nœud WSA \_ multipoint \_ D \_ , pour la création d’un socket agissant comme une feuille D \_ , et autorisé uniquement si XP1 \_ prend en charge \_ multipoint, est indiqué dans l’entrée [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondante.

Notez que lorsque vous créez un socket multipoint, l’un des deux indicateurs de plan de contrôle, et l’un des deux indicateurs de plan de données, doivent être définis dans le paramètre *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Ainsi, les quatre possibilités de création de sockets multipoint sont les suivantes :

-   « racine c \_ / \_ racine »
-   « \_ racine c/d \_ »
-   « \_ racine de feuille/d \_ »
-   "c \_ feuille/d \_ feuille"

 

 
