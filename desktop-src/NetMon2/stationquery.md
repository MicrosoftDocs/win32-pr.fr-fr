---
description: La structure STATIONQUERY fournit des informations sur un ordinateur spécifique à l’aide de Moniteur réseau.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: STATIONQUERY, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a2e46f4c0d213091a3915b5310d7768a193d33e5ac3391fd3bc3c6781e32cb57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363055"
---
# <a name="stationquery-structure"></a>STATIONQUERY, structure

La structure **STATIONQUERY** fournit des informations sur un ordinateur spécifique à l’aide de moniteur réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a>Membres

<dl> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs identifiant l’état actuel de Moniteur réseau.



| Valeur                                                                                                                                                                                                                | Signification                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <dt>**\_indicateurs STATIONQUERY \_ chargés**</dt> </dl>                   | Le pilote est chargé, mais pas le noyau.<br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <dt>**\_indicateurs STATIONQUERY \_ en cours d’exécution**</dt> </dl>                | Le pilote est chargé mais ne capture pas les données.<br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <dt>**\_capture d’indicateurs STATIONQUERY \_**</dt> </dl>          | Le pilote est activement engagé dans une capture.<br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <dt>**\_indicateurs STATIONQUERY \_ transmettant**</dt> </dl> | Cet indicateur est obsolète.<br/>                       |



 

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Numéro de version mineure de Moniteur réseau installé sur l’ordinateur.

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Numéro de version principale de Moniteur réseau installé sur l’ordinateur.

</dd> <dt>

**LicenseNumber**
</dt> <dd>

Numéro de licence du logiciel.

</dd> <dt>

**MachineName**
</dt> <dd>

Nom du fabricant de l’ordinateur, le cas échéant.

</dd> <dt>

**UserName**
</dt> <dd>

Nom d’utilisateur ou identificateur système.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**AdapterAddress**
</dt> <dd>

Adresse de la carte réseau.

</dd> <dt>

**WMachineName**
</dt> <dd>

Nom de l’ordinateur Unicode. Ce membre s’applique à Moniteur réseau 2,0 ou version ultérieure.

</dd> <dt>

**WUserName**
</dt> <dd>

Nom d’utilisateur Unicode. Ce membre s’applique à Moniteur réseau 2,0 ou version ultérieure.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un tableau de ces structures est utilisé par la structure [QUERYTABLE](querytable.md) pour fournir une liste des ordinateurs qui utilisent actuellement Moniteur réseau pour capturer des données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[QUERYTABLE](querytable.md)
</dt> </dl>

 

 




