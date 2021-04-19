---
title: Structure MCI_WAVE_OPEN_PARMS (Mciapi. h)
description: La \_ structure des \_ fonctions Open PARMS de l’onde MCI \_ contient des informations pour la \_ commande MCI Open pour les périphériques audio Waveform.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- Structure de MCI_WAVE_OPEN_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510155"
---
# <a name="mci_wave_open_parms-structure"></a>\_Structure des \_ PARMS d’ouverture MCI Wave \_

La structure des fonctions **\_ \_ Open \_ PARMS de l’onde MCI** contient des informations pour la commande [**MCI \_ Open**](mci-open.md) pour les périphériques audio Waveform.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificateur renvoyé à l’application.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nom ou identificateur de constante du type d’appareil. (Le nom de l’appareil est généralement obtenu à partir du registre ou du fichier SYSTEM.INI.) Ce membre peut être l’une des valeurs indiquées dans les [types d’appareils MCI](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nom de l’élément d’appareil (généralement un chemin d’accès).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias d’appareil facultatif.

</dd> <dt>

**dwBufferSeconds**
</dt> <dd>

Longueur de la mémoire tampon, en secondes.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

Si vous n’utilisez pas les membres de données étendus, vous pouvez utiliser la structure des [**\_ \_ parms Open parms**](mci-open-parms.md) au lieu de l' **\_ \_ ouverture \_ des sons MCI** .

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
</dt> <dt>

[**les \_ PARMS ouverts MCI \_**](mci-open-parms.md)
</dt> </dl>

 

