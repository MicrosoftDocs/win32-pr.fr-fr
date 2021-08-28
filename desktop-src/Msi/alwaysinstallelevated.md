---
description: installez un package de Windows Installer avec des privilèges élevés (système).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc015dad8096db16d8b70238a5fd7e07544b83f9a9e3d1a5045be9d12bbb30cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650239"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated a

vous pouvez utiliser la stratégie alwaysinstallelevated a pour installer un package Windows Installer avec des privilèges élevés (système).

* * AVERTISSEMENT : * *

Cette option équivaut à accorder des droits d’administration complets, ce qui peut poser un risque de sécurité massif. Microsoft déconseille fortement l’utilisation de ce paramètre.

Pour installer un package avec des privilèges élevés (système), définissez la valeur AlwaysInstallElevated a sur « 1 » sous les deux clés de Registre suivantes :

**HKEY \_ \_** \\ **stratégies logicielles** de l’utilisateur actuel programme d' \\  \\  \\  \\ **installation** de Microsoft Windows

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Si la valeur AlwaysInstallElevated a n’est pas définie sur « 1 » sous les deux clés de Registre précédentes, le programme d’installation utilise des privilèges élevés pour installer les applications managées et utilise le niveau de privilège de l’utilisateur actuel pour les applications non gérées.

Étant donné que cette stratégie permet aux utilisateurs d’installer des applications qui requièrent l’accès aux répertoires et aux clés de Registre pour lesquels l’utilisateur n’a pas l’autorisation d’afficher ou de modifier, vous devez déterminer s’il fournit à vos utilisateurs un niveau de sécurité approprié. la définition de cette stratégie indique à Windows Installer d’utiliser des autorisations système lors de l’installation de l’application sur le système. Si cette stratégie n’est pas définie, les applications non distribuées par l’administrateur sont installées à l’aide des privilèges de l’utilisateur et seules les applications gérées obtiennent des privilèges élevés.

Notez qu’une fois que la stratégie par ordinateur pour AlwaysInstallElevated a est activée, tout utilisateur peut définir son paramètre par utilisateur.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 



