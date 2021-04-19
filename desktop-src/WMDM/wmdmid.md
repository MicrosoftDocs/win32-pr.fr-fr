---
title: WMDMID, structure
description: La structure WMDMID décrit les numéros de série et les ID de groupe.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Structure WMDMID Windows Media Gestionnaire de périphériques
- Pointeur de structure PWMDMID Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534884"
---
# <a name="wmdmid-structure"></a>WMDMID, structure

La structure **WMDMID** décrit les numéros de série et les ID de groupe.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille de la structure **WMDMID** , en octets.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**Valeur DWORD** contenant le numéro d’ID inscrit du fournisseur. Contient zéro si la valeur n’est pas utilisée.

</dd> <dt>

**\[longueur WMDMID \_ PID\]**
</dt> <dd>

Pointeur vers un tableau d’octets contenant le numéro de série. Le numéro de série est une chaîne de valeurs d’octets qui n’ont pas de format standard. Notez qu’il ne s’agit pas d’une valeur à caractères larges. **WMDMID \_ LENGTH** est une valeur constante définie dans mswmdm. h.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Longueur réelle du numéro de série retourné, en octets.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMDSPDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





