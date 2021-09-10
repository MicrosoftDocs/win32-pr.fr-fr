---
title: Structure de MCI_VCR_SEEK_PARMS (VCR. h)
description: La structure de la \_ recherche MCI VCR \_ contient des \_ paramètres pour la \_ commande MCI Seek pour les enregistreurs vidéo-cassettes.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- structure MCI_VCR_SEEK_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363856"
---
# <a name="mci_vcr_seek_parms-structure"></a>Structure de la \_ recherche MCI VCR \_ \_

La structure de la **\_ \_ \_ recherche MCI VCR** contient des paramètres pour la commande [**MCI \_ Seek**](mci-seek.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwTo**
</dt> <dd>

Position à laquelle effectuer la recherche.

</dd> <dt>

**dwMark**
</dt> <dd>

Marque numérotée à rechercher.

</dd> <dt>

**dwAt**
</dt> <dd>

Heure de début de la recherche.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les positions sont spécifiées dans le format d’heure actuel.

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Spécifications



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

[**\_recherche MCI**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

