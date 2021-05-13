---
description: Contient des informations sur le lecteur sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre du répertoire ou la fenêtre des résultats de la recherche).
title: Structure FMS_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842230"
---
# <a name="fms_getdriveinfo-structure"></a>\_GETDRIVEINFO-structure FMS

Contient des informations sur le lecteur sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre du répertoire ou la fenêtre des résultats de la recherche).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwTotalSpace**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Quantité totale d’espace de stockage, en octets, sur le disque associé au lecteur.

</dd> <dt>

**dwFreeSpace**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Quantité d’espace de stockage disponible, en octets, sur le disque associé au lecteur.

</dd> <dt>

**szPath**
</dt> <dd>

Type : **TCHAR \[ 260 \]**

</dd> <dd>

chemin d’accès se terminant par un caractère null du répertoire actif.

</dd> <dt>

**szVolume**
</dt> <dd>

Type : **TCHAR \[ 14 \]**

</dd> <dd>

Nom de volume terminé par le caractère null du disque associé au lecteur.

</dd> <dt>

**szShare**
</dt> <dd>

Type : **TCHAR \[ 128 \]**

</dd> <dd>

Nom se terminant par un caractère null de la ressource réseau (si le lecteur est accessible via un réseau).

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_GETDRIVEINFO FM**](fm-getdriveinfo.md)
</dt> </dl>

 

 




