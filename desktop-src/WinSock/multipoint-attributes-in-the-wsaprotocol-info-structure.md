---
title: Attributs multipoint dans WSAPROTOCOL_INFO
description: Les attributs multipoint de la \_ structure WSAPROTOCOL info incluent XP1 \_ prennent en charge \_ multipoint, \_ \_ le plan de contrôle multipoint XP1 \_ et le plan de \_ données multipoint XP1 \_ \_ .
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751437"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Attributs multipoint dans WSAPROTOCOL_INFO

Trois paramètres d’attribut sont définis dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) afin de distinguer les différents schémas utilisés dans les plans de contrôle et de données, respectivement :

-   XP1 \_ support \_ multipoint avec une valeur de 1 indique que cette entrée de protocole prend en charge les communications multipoint et que les deux paramètres suivants sont significatifs.
-   XP1 \_ \_ plan de contrôle multipoint \_ indique si le plan de contrôle est rooté (valeur = 1) ou non racine (valeur = 0).
-   \_ \_ Le plan de données multipoint XP1 \_ indique si le plan de données est rooté (valeur = 1) ou non enraciné (valeur = 0).

Deux entrées d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sont présentes si un protocole multipoint prenait en charge les plans de données racines et autres, une entrée pour chacun.

 

 
