---
title: Structure MPCOMPONENT_VERSION (MpClient. h)
description: Version et heure de mise à jour pour un composant individuel.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPCOMPONENT_VERSION
- PMPCOMPONENT_VERSION des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976069"
---
# <a name="mpcomponent_version-structure"></a>Structure de la version de MPCOMPONENT \_

Version et heure de mise à jour pour un composant individuel.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Type : **ULONGLONG**

</dd> <dd>

Champ version. Chaque **mot** représente major, minor, Build et revision.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Type : **\_ entier ULARGE**

</dd> <dd>

Heure de la dernière mise à jour du composant, au format **fileTime** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





