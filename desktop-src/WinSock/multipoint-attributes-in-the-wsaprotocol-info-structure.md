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
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="36930-103">Attributs multipoint dans WSAPROTOCOL_INFO</span><span class="sxs-lookup"><span data-stu-id="36930-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="36930-104">Trois paramètres d’attribut sont définis dans la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) afin de distinguer les différents schémas utilisés dans les plans de contrôle et de données, respectivement :</span><span class="sxs-lookup"><span data-stu-id="36930-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="36930-105">XP1 \_ support \_ multipoint avec une valeur de 1 indique que cette entrée de protocole prend en charge les communications multipoint et que les deux paramètres suivants sont significatifs.</span><span class="sxs-lookup"><span data-stu-id="36930-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="36930-106">XP1 \_ \_ plan de contrôle multipoint \_ indique si le plan de contrôle est rooté (valeur = 1) ou non racine (valeur = 0).</span><span class="sxs-lookup"><span data-stu-id="36930-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="36930-107">\_ \_ Le plan de données multipoint XP1 \_ indique si le plan de données est rooté (valeur = 1) ou non enraciné (valeur = 0).</span><span class="sxs-lookup"><span data-stu-id="36930-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="36930-108">Deux entrées d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) sont présentes si un protocole multipoint prenait en charge les plans de données racines et autres, une entrée pour chacun.</span><span class="sxs-lookup"><span data-stu-id="36930-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
