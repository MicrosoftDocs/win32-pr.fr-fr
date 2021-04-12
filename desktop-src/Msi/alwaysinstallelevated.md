---
description: Installez un package de Windows Installer avec des privilèges élevés (système).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528876"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated a

Vous pouvez utiliser la stratégie AlwaysInstallElevated a pour installer un package Windows Installer avec des privilèges élevés (système).

* * AVERTISSEMENT : * *

Cette option équivaut à accorder des droits d’administration complets, ce qui peut poser un risque de sécurité massif. Microsoft déconseille fortement l’utilisation de ce paramètre.

Pour installer un package avec des privilèges élevés (système), définissez la valeur AlwaysInstallElevated a sur « 1 » sous les deux clés de Registre suivantes :

**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

Si la valeur AlwaysInstallElevated a n’est pas définie sur « 1 » sous les deux clés de Registre précédentes, le programme d’installation utilise des privilèges élevés pour installer les applications managées et utilise le niveau de privilège de l’utilisateur actuel pour les applications non gérées.

Étant donné que cette stratégie permet aux utilisateurs d’installer des applications qui requièrent l’accès aux répertoires et aux clés de Registre pour lesquels l’utilisateur n’a pas l’autorisation d’afficher ou de modifier, vous devez déterminer s’il fournit à vos utilisateurs un niveau de sécurité approprié. La définition de cette stratégie indique à Windows Installer d’utiliser des autorisations système lors de l’installation de l’application sur le système. Si cette stratégie n’est pas définie, les applications non distribuées par l’administrateur sont installées à l’aide des privilèges de l’utilisateur et seules les applications gérées obtiennent des privilèges élevés.

Notez qu’une fois que la stratégie par ordinateur pour AlwaysInstallElevated a est activée, tout utilisateur peut définir son paramètre par utilisateur.

## <a name="remarks"></a>Notes

Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



