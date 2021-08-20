---
title: Structure MCI_OPEN_PARMS (Mciapi. h)
description: La \_ structure MCI Open \_ PARMS contient des informations pour la \_ commande MCI Open.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- structure MCI_OPEN_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80d01f41db904cea583f83aa446e718d1067e99e4d8bac3a3c6791ef5696f83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138304"
---
# <a name="mci_open_parms-structure"></a>\_Structure d’ouverture des \_ PARMS MCI

La structure **MCI \_ Open \_ PARMS** contient des informations pour la commande [**MCI \_ Open**](mci-open.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificateur retourné à l’application.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nom ou identificateur de constante du type d’appareil. (Le nom de l’appareil est généralement obtenu à partir du registre ou du fichier SYSTEM.INI.) Si ce membre est une constante, il peut s’agir de l’une des valeurs indiquées dans [types d’appareils MCI](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Élément d’appareil (souvent un chemin d’accès).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias d’appareil facultatif.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Structures MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ ouvert**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

