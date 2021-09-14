---
title: Structure MCI_SYSINFO_PARMS (Mciapi. h)
description: La \_ \_ structure de l’option MCI sysinfo PARMS contient des informations pour la \_ commande MCI sysinfo.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- structure MCI_SYSINFO_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195100"
---
# <a name="mci_sysinfo_parms-structure"></a>\_Structure des \_ PARMS MCI sysinfo

La structure de l’option **MCI \_ sysinfo \_ PARMS** contient des informations pour la commande [**MCI \_ sysinfo**](mci-sysinfo.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Pointeur vers une mémoire tampon fournie par l’utilisateur pour la chaîne de retour. Elle est également utilisée pour retourner une valeur **DWORD** lorsque l' \_ indicateur de quantité MCI sysinfo \_ est utilisé.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Taille, en octets, de la mémoire tampon de retour.

</dd> <dt>

**dwNumber**
</dt> <dd>

Nombre indiquant la position de l’appareil dans la table du périphérique MCI ou dans la liste des appareils ouverts si l' \_ indicateur d’ouverture MCI sysinfo \_ est défini.

</dd> <dt>

**wDeviceType**
</dt> <dd>

Type d’appareil. Ce membre peut être l’une des valeurs indiquées dans les [types d’appareils MCI](mci-device-types.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Spécifications



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

[**MCI \_ sysinfo**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

