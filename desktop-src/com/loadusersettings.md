---
title: LoadUserSettings
description: Détermine si COM doit charger le profil utilisateur pour les serveurs COM qui exécutent en tant qu’identité de l’application utilisateur de lancement.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valeur de Registre LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940160"
---
# <a name="loadusersettings"></a>LoadUserSettings

Détermine si COM doit charger le profil utilisateur pour les serveurs COM qui exécutent en tant qu’identité de l’application utilisateur de lancement.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** . Si la *valeur* est différente de zéro, com charge le profil du compte d’utilisateur avec lequel il lance le serveur com. Si la *valeur* est égale à zéro ou absente, com ne chargera pas le profil du compte d’utilisateur avec lequel il lance le serveur com.

Ce paramètre est ignoré si une entrée [**runas**](runas.md) est présente.

 

 




