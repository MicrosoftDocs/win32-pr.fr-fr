---
title: Structure de MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: La \_ structure MCI OVLY \_ Open \_ PARMS contient des informations pour la \_ commande MCI Open pour les périphériques de superposition vidéo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Structure de MCI_OVLY_OPEN_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464227"
---
# <a name="mci_ovly_open_parms-structure"></a>\_OVLY \_ Open \_ PARMS, MCI

La structure **MCI \_ OVLY \_ Open \_ PARMS** contient des informations pour la commande [**MCI \_ Open**](mci-open.md) pour les périphériques de superposition vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
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

Nom de l’élément d’appareil (généralement un chemin d’accès).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias d’appareil facultatif.

</dd> <dt>

**dwStyle**
</dt> <dd>

Style de fenêtre.

</dd> <dt>

**hWndParent**
</dt> <dd>

Handle vers la fenêtre parente.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

Vous pouvez utiliser la [**structure \_ Open \_ parmss MCI**](mci-open-parms.md) à la place de **MCI \_ OVLY \_ ouvrir \_ parms** si vous n’utilisez pas les membres de données étendus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Structures MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ ouvert**](mci-open.md)
</dt> <dt>

[**les \_ PARMS ouverts MCI \_**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

