---
title: Structure MCI_SAVE_PARMS (Mciapi. h)
description: La \_ structure MCI Save \_ PARMS contient les informations de nom de fichier pour la \_ commande d’enregistrement MCI.
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- structure MCI_SAVE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d87f581e753265796259fbd33bfeeba3d4c2957e107c7edeb8d08c063e34e32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038329"
---
# <a name="mci_save_parms-structure"></a>\_Enregistrer la \_ structure des PARMS avec MCI

La structure **MCI \_ Save \_ PARMS** contient les informations de nom de fichier pour la commande d' [**\_ enregistrement MCI**](mci-save.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nom du fichier à enregistrer.

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

[**\_enregistrement MCI**](mci-save.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

