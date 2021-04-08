---
title: NEWHEADER, structure
description: Contient le nombre de composants icône ou curseur dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menus de la structure NEWHEADER et autres ressources
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941804"
---
# <a name="newheader-structure"></a>NEWHEADER, structure

Contient le nombre de composants icône ou curseur dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Reserved**
</dt> <dd>

Type : **Word**

</dd> <dd>

Réservé doit être égal à zéro.

</dd> <dt>

**ResType**
</dt> <dd>

Type : **Word**

</dd> <dd>

Type de ressource. Ce membre doit avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                       | Signification                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**Ressource \_ CURSEUR**</dt> <dt>2</dt> </dl> | Type de ressource de curseur.<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**Ressource \_ ICÔNE**</dt> <dt>1</dt> </dl>       | Type de ressource d’icône.<br/>   |



 

</dd> <dt>

**ResCount**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre de composants icône ou curseur dans le groupe de ressources.

</dd> </dl>

## <a name="remarks"></a>Notes

Une ou plusieurs structures [**RESDIR**](resdir.md) suivent immédiatement la structure **NEWHEADER** dans le fichier. res. Le membre **ResCount** spécifie le nombre de structures **RESDIR** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

 





