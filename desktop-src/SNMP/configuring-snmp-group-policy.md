---
title: Configuration de stratégie de groupe SNMP
description: Si vous utilisez le composant logiciel enfichable MMC (Microsoft Management Console) pour stratégie de groupe d’administrer les paramètres de stratégie basés sur le Registre qui s’appliquent à SNMP, une ou plusieurs des sous-clés suivantes peuvent exister.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e17bc3b1bac886a19791f57903920a11062072a81577a0a78ab01d461709ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009657"
---
# <a name="configuring-snmp-group-policy"></a>Configuration de stratégie de groupe SNMP

Si vous utilisez le composant logiciel enfichable MMC (Microsoft Management Console) pour stratégie de groupe d’administrer les paramètres de stratégie basés sur le Registre qui s’appliquent à SNMP, une ou plusieurs des sous-clés suivantes peuvent exister.

**HKEY \_ \_** \\  \\  \\  \\ **Paramètres** SNMP des stratégies \\  de logiciel de l’ordinateur local ValidCommunities

**HKEY \_ \_** \\  \\  \\  \\ **Paramètres** SNMP des stratégies \\  de logiciel de l’ordinateur local PermittedManagers

**HKEY \_ \_** \\  \\  \\  \\ **Paramètres** SNMP des stratégies \\  de logiciel de l’ordinateur local TrapConfiguration

En règle générale, seuls les membres du groupe local administrateurs peuvent accéder aux sous-clés de Registre suivantes qui stockent les données de configuration du service SNMP :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** SNMP des services \\  de CurrentControlSet de système d’ordinateur local ValidCommunities

**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** SNMP des services \\  de CurrentControlSet de système d’ordinateur local PermittedManagers

Pour plus d’informations sur les paramètres de stratégie basés sur le registre, consultez [à propos de stratégie de groupe](/previous-versions/windows/desktop/Policy/about-group-policy).

 

 