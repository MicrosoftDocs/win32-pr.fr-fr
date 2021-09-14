---
description: Contient des informations sur un fichier sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre de répertoire ou la fenêtre des résultats de la recherche).
title: Structure FMS_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226977"
---
# <a name="fms_getfilesel-structure"></a>\_GETFILESEL-structure FMS

Contient des informations sur un fichier sélectionné dans la fenêtre Gestionnaire de fichiers active (la fenêtre de répertoire ou la fenêtre des résultats de la recherche).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Membres

<dl> <dt>

**ftTime**
</dt> <dd>

Type : **fileTime**

</dd> <dd>

Heure et date de création du fichier.

</dd> <dt>

**dwSize nul**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille, en octets, du fichier.

</dd> <dt>

**bAttr**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Attributs du fichier.

</dd> <dt>

**szName**
</dt> <dd>

Type : **TCHAR**

</dd> <dd>

Chemin d’accès complet et nom de fichier du fichier sélectionné se terminant par un caractère null.

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
</dt> </dl>

 

 




