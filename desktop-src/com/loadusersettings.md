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
# <a name="loadusersettings"></a><span data-ttu-id="c065a-104">LoadUserSettings</span><span class="sxs-lookup"><span data-stu-id="c065a-104">LoadUserSettings</span></span>

<span data-ttu-id="c065a-105">Détermine si COM doit charger le profil utilisateur pour les serveurs COM qui exécutent en tant qu’identité de l’application utilisateur de lancement.</span><span class="sxs-lookup"><span data-stu-id="c065a-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c065a-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="c065a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="c065a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="c065a-107">Remarks</span></span>

<span data-ttu-id="c065a-108">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c065a-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="c065a-109">Si la *valeur* est différente de zéro, com charge le profil du compte d’utilisateur avec lequel il lance le serveur com.</span><span class="sxs-lookup"><span data-stu-id="c065a-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="c065a-110">Si la *valeur* est égale à zéro ou absente, com ne chargera pas le profil du compte d’utilisateur avec lequel il lance le serveur com.</span><span class="sxs-lookup"><span data-stu-id="c065a-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="c065a-111">Ce paramètre est ignoré si une entrée [**runas**](runas.md) est présente.</span><span class="sxs-lookup"><span data-stu-id="c065a-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




