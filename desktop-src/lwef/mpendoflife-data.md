---
title: Structure MPENDOFLIFE_DATA (MpClient. h)
description: '\ 0034 ; Fin de vie \ 0034 ; données de notification.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPENDOFLIFE_DATA
- PMPENDOFLIFE_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532ee5f80e76de49c2c20bb01958e95fc13603b8f4b65666639834c5cad0fa72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476281"
---
# <a name="mpendoflife_data-structure"></a>\_Structure de données MPENDOFLIFE

Données de notification de « fin de vie ».

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**ftSignatureExpiry**
</dt> <dd>

Type : **fileTime**

</dd> <dd>

Heure d’expiration de la signature.

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

Type : **fileTime**

</dd> <dd>

Heure d’expiration de la plateforme.

</dd> <dt>

**fAdminControlled**
</dt> <dd>

Type : **bool**

</dd> <dd>

True si l’administrateur contrôlant la stratégie pour l’indication de la notification. Si cette option est définie, l’interface utilisateur n’affiche pas la notification de fin de vie.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Type : **bool**

</dd> <dd>

True si la « fin de vie » est en attente ou passée. Si la valeur est false, l’interface utilisateur et les clients peuvent effacer tout État lié à la EOL.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





