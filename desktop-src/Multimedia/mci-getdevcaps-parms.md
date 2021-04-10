---
title: Structure MCI_GETDEVCAPS_PARMS (Mciapi. h)
description: La structure de MCI \_ GETDEVCAPS \_ PARMS contient des informations sur les fonctionnalités de l’appareil pour la \_ commande MCI GETDEVCAPS.
ms.assetid: a7b128c5-2121-49cd-b668-3a8466d49a73
keywords:
- Structure de MCI_GETDEVCAPS_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a981f6fb9f156cecfa1b4b73046b1b3c654b32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032553"
---
# <a name="mci_getdevcaps_parms-structure"></a>MCI \_ GETDEVCAPS \_ PARMS, structure

La structure de **MCI \_ GETDEVCAPS \_ PARMS** contient des informations sur les fonctionnalités de l’appareil pour la commande [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
} MCI_GETDEVCAPS_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contient des informations à la sortie.

</dd> <dt>

**dwItem**
</dt> <dd>

Fonctionnalité en cours d’interrogation. Ce membre peut être l’une des constantes listées dans la documentation de référence pour la commande [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

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

[**\_GETDEVCAPS MCI**](mci-getdevcaps.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

