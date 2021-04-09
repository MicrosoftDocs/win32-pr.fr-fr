---
description: Structure identifiant l’hôte et le fichier source à évaluer.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Structure WLDP_HOST_INFORMATION (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033593"
---
# <a name="wldp_host_information-structure"></a>Structure des informations de l' \_ hôte WLDP \_

Structure identifiant l’hôte et le fichier source à évaluer.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwRevision**
</dt> <dd>

Doit être **WLDP \_ \_ \_ révision des informations** de l’hôte.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valeur d’énumération de l' [**\_ \_ ID d’hôte WLDP**](wldp-host-id.md) qui décrit l’ID d’hôte.

</dd> <dt>

**szSource**
</dt> <dd>

Chemin d’accès complet et nom de script avec l’extension. NULL pour **l' \_ ID d’hôte WLDP \_ \_ Global**, ou l’exécution manuelle du script.

</dd> <dt>

**hSource**
</dt> <dd>

En plus du nom, l’appelant peut spécifier un handle vers le fichier utilisé pour la validation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




