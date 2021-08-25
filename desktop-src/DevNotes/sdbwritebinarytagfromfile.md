---
description: Écrit des données binaires à partir du fichier spécifié dans la base de données spécifiée.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ec2acf733a870d3dcff57ceb7cdea996c6b6dc1e5d950ec85944285e6ba6cc35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815139"
---
# <a name="sdbwritebinarytagfromfile-function"></a>SdbWriteBinaryTagFromFile fonction)

Écrit des données binaires à partir du fichier spécifié dans la base de données spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tTag* \[ dans\]
</dt> <dd>

BALIse pour l’entrée. Cette BALIse doit être de **type \_ \_ binaire**.

</dd> <dt>

*pwszPath* \[ dans\]
</dt> <dd>

Chemin d’accès au fichier qui contient les données. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




