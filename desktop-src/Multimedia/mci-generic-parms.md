---
title: Structure MCI_GENERIC_PARMS (Mciapi. h)
description: La \_ \_ structure des PARMS génériques MCI contient le handle de la fenêtre qui reçoit les messages de notification. Cette structure est utilisée pour les messages de commande MCI qui ont des listes de paramètres vides.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- structure MCI_GENERIC_PARMS Windows multimédia
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
ms.openlocfilehash: 0e2da55b721c7567b5fbc52d965cf753f896ee28fa4d76e094c7867434a69791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784309"
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

## <a name="remarks"></a>Remarques

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

 

