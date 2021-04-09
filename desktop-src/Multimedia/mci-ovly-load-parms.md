---
title: Structure de MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: La \_ structure des PARMS de charge OVLY MCI contient des \_ \_ informations pour la \_ commande de chargement MCI pour les périphériques de superposition vidéo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Structure de MCI_OVLY_LOAD_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032330"
---
# <a name="mci_ovly_load_parms-structure"></a>\_OVLY de \_ charge de chargement MCI \_

La structure des **\_ \_ \_ PARMS de charge OVLY MCI** contient des informations pour la commande de [**\_ chargement MCI**](mci-load.md) pour les périphériques de superposition vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nom du fichier à charger.

</dd> <dt>

**Release**
</dt> <dd>

Identifie la zone de la mémoire tampon vidéo à mettre à jour. Les structures [Rect](/previous-versions//ms536136(v=vs.85)) sont gérées différemment dans MCI et dans d’autres parties de Windows. dans MCI, **RC. Right** contient la largeur du rectangle et **RC. Bottom** contient sa hauteur.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

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

[**\_chargement MCI**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECTANGULAIRE](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

