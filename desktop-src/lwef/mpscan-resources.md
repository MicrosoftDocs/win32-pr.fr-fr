---
title: Structure MPSCAN_RESOURCES (MpClient. h)
description: Informations de ressource passées pendant une opération d’analyse.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSCAN_RESOURCES
- PMPSCAN_RESOURCES des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942855"
---
# <a name="mpscan_resources-structure"></a>\_Structure des ressources MPSCAN

Informations de ressource passées pendant une opération d’analyse.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwResourceCount**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre de ressources.

</dd> <dt>

**pResourceList**
</dt> <dd>

Type : **PMPRESOURCE \_ info**

</dd> <dd>

Tableau de ressources. Consultez [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations MPRESOURCE**](mpresource-info.md)
</dt> </dl>

 

 





