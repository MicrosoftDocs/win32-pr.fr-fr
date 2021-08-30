---
title: Structure de MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: La \_ structure des PARMS de charge OVLY MCI contient des \_ \_ informations pour la \_ commande de chargement MCI pour les périphériques de superposition vidéo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- structure MCI_OVLY_LOAD_PARMS Windows multimédia
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
ms.openlocfilehash: dc966b51224246dbceda46927f605c214ba4809a1cca451813a1075811fa5225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039099"
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

Identifie la zone de la mémoire tampon vidéo à mettre à jour. Les structures [Rect](/previous-versions//ms536136(v=vs.85)) sont gérées différemment dans MCI et dans d’autres parties de Windows ; dans MCI, **RC. Right** contient la largeur du rectangle et **RC. Bottom** contient sa hauteur.

</dd> </dl>

## <a name="remarks"></a>Remarques

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

 

