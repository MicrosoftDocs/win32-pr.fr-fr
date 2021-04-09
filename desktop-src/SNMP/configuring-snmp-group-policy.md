---
title: Configuration de stratégie de groupe SNMP
description: Si vous utilisez le composant logiciel enfichable MMC (Microsoft Management Console) pour stratégie de groupe d’administrer les paramètres de stratégie basés sur le Registre qui s’appliquent à SNMP, une ou plusieurs des sous-clés suivantes peuvent exister.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102113"
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

 

 