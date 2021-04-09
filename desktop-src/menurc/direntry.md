---
title: Structure de dilocataire
description: Contient un ordinal unique qui identifie une police individuelle dans le groupe de ressources de police. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Menus de la structure dilocataires et autres ressources
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742029"
---
# <a name="direntry-structure"></a>Structure de dilocataire

Contient un ordinal unique qui identifie une police individuelle dans le groupe de ressources de police. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**fontOrdinal**
</dt> <dd>

Type : **Word**

</dd> <dd>

Identificateur ordinal unique pour une police individuelle dans un groupe de ressources de police.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure [**FONTDIRENTRY**](fontdirentry.md) pour la police spécifiée suit directement la structure de **dilocataires** pour cette police.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

 





