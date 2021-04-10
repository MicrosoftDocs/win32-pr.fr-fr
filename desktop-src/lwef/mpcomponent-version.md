---
title: Structure MPCOMPONENT_VERSION (MpClient. h)
description: Version et heure de mise à jour pour un composant individuel.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPCOMPONENT_VERSION
- PMPCOMPONENT_VERSION des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942074"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





