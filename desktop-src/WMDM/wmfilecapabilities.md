---
title: WMFILECAPABILITIES, structure
description: La structure WMFILECAPABILITIES décrit le type MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Structure WMFILECAPABILITIES Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f4852eeb7142b92c2c1a4c2073dfc70e5f6a6d74c727a7ab9e63c285796846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903769"
---
# <a name="wmfilecapabilities-structure"></a>WMFILECAPABILITIES, structure

La structure **WMFILECAPABILITIES** décrit le type MIME.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>Membres

<dl> <dt>

**pwszMimeType**
</dt> <dd>

Type MIME.

</dd> <dt>

**dwReserved**
</dt> <dd>

**DWORD** réservé pour une utilisation ultérieure. A la valeur zéro (0).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





