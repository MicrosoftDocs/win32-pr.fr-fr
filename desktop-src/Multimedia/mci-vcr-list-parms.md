---
title: Structure de MCI_VCR_LIST_PARMS (VCR. h)
description: La structure de la \_ liste des magnétoscopes MCI \_ contient des \_ paramètres pour la \_ commande de liste MCI pour les enregistreurs de cassettes vidéo.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- structure MCI_VCR_LIST_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb74aeee254ab050d394dbf250c037d00d10d51fe872052dd5d36164b2c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137980"
---
# <a name="mci_vcr_list_parms-structure"></a>\_Liste des magnétoscopes MCI \_ \_ structure PARMS

La structure de la **\_ \_ liste \_ des magnétoscopes MCI** contient des paramètres pour la commande de [**\_ liste MCI**](mci-list.md) pour les enregistreurs de cassettes vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Mémoire tampon pour les informations renvoyées.

</dd> <dt>

**dwNumber**
</dt> <dd>

Nombre d’entrées vidéo ou audio du magnétoscope.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Structures MCI**](mci-structures.md)
</dt> <dt>

[**\_liste MCI**](mci-list.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

