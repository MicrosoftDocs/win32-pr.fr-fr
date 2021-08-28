---
title: LoadUserSettings
description: Détermine si COM doit charger le profil utilisateur pour les serveurs COM qui exécutent en tant qu’identité de l’application utilisateur de lancement.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Valeur de Registre LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731039"
---
# <a name="loadusersettings"></a>LoadUserSettings

Détermine si COM doit charger le profil utilisateur pour les serveurs COM qui exécutent en tant qu’identité de l’application utilisateur de lancement.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** . Si la *valeur* est différente de zéro, com charge le profil du compte d’utilisateur avec lequel il lance le serveur com. Si la *valeur* est égale à zéro ou absente, com ne chargera pas le profil du compte d’utilisateur avec lequel il lance le serveur com.

Ce paramètre est ignoré si une entrée [**runas**](runas.md) est présente.

 

 




