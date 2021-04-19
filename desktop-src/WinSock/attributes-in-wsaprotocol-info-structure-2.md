---
description: XP1 \_ prennent en charge \_ multipoint, XP1 \_ plan de \_ contrôle multipoint \_ et \_ \_ \_ les paramètres d’attribut de plan de données multipoint XP1 dans la structure d’informations de WSAPROTOCOL Winsock \_ .
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Attributs dans la structure WSAPROTOCOL_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517497"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Attributs dans la \_ structure WSAPROTOCOL info

Pour la prise en charge de la taxonomie décrite ci-dessus, trois paramètres d’attribut dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sont utilisés pour distinguer les schémas utilisés dans les plans de contrôle et de données, respectivement :

-   XP1 \_ support \_ multipoint avec une valeur de 1 indique que cette entrée de protocole prend en charge les communications multipoint et que les deux paramètres suivants sont significatifs.
-   XP1 \_ \_ plan de contrôle multipoint \_ indique si le plan de contrôle est rooté (valeur = 1) ou non racine (valeur = 0).
-   \_ \_ Le plan de données multipoint XP1 \_ indique si le plan de données est rooté (valeur = 1) ou non enraciné (valeur = 0).

Notez que deux entrées d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sont présentes si un protocole multipoint prenait en charge les plans de données racines et autres, une entrée pour chacun.

L’application peut utiliser [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) pour déterminer si les communications multipoint sont prises en charge pour un protocole donné et, si c’est le cas, comment elles sont prises en charge par rapport aux plans de contrôle et de données, respectivement.

 

 
