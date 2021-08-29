---
description: Recherche la correspondance de BALIse suivante dans le parent spécifié et retourne le TAGID de la correspondance.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: fe9b9914ed9126a364fb377adc4afae84784df156a8e75c3d0d2f997f6185811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103699"
---
# <a name="sdbfindnexttag-function"></a>SdbFindNextTag fonction)

Recherche la correspondance de BALIse suivante dans le parent spécifié et retourne le **TagId** de la correspondance.

## <a name="syntax"></a>Syntaxe


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tiParent* \[ dans\]
</dt> <dd>

**TagId** du début de la recherche. Ce paramètre peut être **TagId \_ racine** ou **\_ \_ liste de types de balises**.

</dd> <dt>

*tiPrev* \[ dans\]
</dt> <dd>

**TagId** de la correspondance précédente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**TagId** de la correspondance.

## <a name="remarks"></a>Remarques

Avant d’appeler cette fonction, appelez la fonction [**SdbFindFirstTag**](sdbfindfirsttag.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




