---
description: Cette stratégie système par ordinateur peut être utilisée pour spécifier que la Windows Installer transmettre toutes les propriétés publiques côté serveur au cours d’une installation gérée à l’aide de privilèges élevés.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114570"
---
# <a name="enableusercontrol"></a>EnableUserControl

Dans le cas d’une installation gérée, l’auteur du package peut avoir besoin de limiter les propriétés publiques qui sont transmises côté serveur et peut être modifiée par un utilisateur qui n’est pas un administrateur système. Certaines restrictions sont généralement nécessaires pour maintenir un environnement sécurisé lorsque l’installation requiert que le programme d’installation utilise des privilèges élevés.

Si cette [stratégie système](system-policy.md) par ordinateur est définie sur « 1 », le programme d’installation peut passer toutes les [propriétés publiques](public-properties.md) côté serveur au cours d’une installation gérée à l’aide de privilèges élevés. La définition de cette stratégie a le même effet que la définition de la propriété **EnableUserControl** . La définition de cette stratégie permet de transmettre toutes les propriétés publiques au service et de les modifier par des utilisateurs non administratifs. Par défaut, cette stratégie n’est pas activée. seules les propriétés publiques restreintes sont transmises côté serveur et peuvent être modifiées par un utilisateur non administratif. Toutes les autres propriétés publiques sont ignorées.

Si le système d’exploitation est Windows 2000, que l’utilisateur n’est pas un administrateur système et que l’application ou le produit est installé avec des privilèges élevés, un utilisateur qui n’est pas un administrateur système peut uniquement remplacer une liste approuvée de propriétés publiques restreintes. Pour plus d’informations, consultez [propriétés publiques restreintes](restricted-public-properties.md).

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



