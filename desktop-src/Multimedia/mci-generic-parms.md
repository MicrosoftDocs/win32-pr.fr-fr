---
title: Structure MCI_GENERIC_PARMS (Mciapi. h)
description: La \_ \_ structure des PARMS génériques MCI contient le handle de la fenêtre qui reçoit les messages de notification. Cette structure est utilisée pour les messages de commande MCI qui ont des listes de paramètres vides.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Structure de MCI_GENERIC_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464983"
---
# <a name="mci_generic_parms-structure"></a>\_Structure des \_ PARMS génériques MCI

La structure des **\_ \_ PARMS génériques MCI** contient le handle de la fenêtre qui reçoit les messages de notification. Cette structure est utilisée pour les messages de commande MCI qui ont des listes de paramètres vides.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> </dl>

## <a name="remarks"></a>Notes

Les structures **MCI \_ Close \_ parms** et **MCI \_ réalisent \_** les mêmes que la structure des **\_ \_ parms génériques MCI** .

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

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

