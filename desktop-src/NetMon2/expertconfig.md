---
description: La structure EXPERTCONFIG contient les données de configuration de l’expert. L’expert recouvre le membre RawConfigData avec une structure spécifique à l’expert.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: EXPERTCONFIG, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 93b47054fd5b8103d5bbe0d762db87f285a5f01690d0b93f6da14d215e404a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366909"
---
# <a name="expertconfig-structure"></a>EXPERTCONFIG, structure

La structure **EXPERTCONFIG** contient les données de configuration de l’expert. L’expert recouvre le membre **RawConfigData** avec une structure spécifique à l’expert.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Membres

<dl> <dt>

**RawConfigLength**
</dt> <dd>

Longueur totale de la structure, y compris les quatre octets utilisés pour le membre. Moniteur réseau utilise la valeur lors de l’enregistrement et de la lecture de la structure sur un lecteur de disque.

</dd> <dt>

**RawConfigData**
</dt> <dd>

Données de configuration. L’expert doit ajouter les données de configuration. Supposons, par exemple, que vous disposiez d’une structure de données similaire à celle-ci.

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

Notez que **RawConfigLength** garantit le bon fonctionnement de la superposition. Lorsque vous utilisez les données, votre code peut se présenter comme suit :

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




