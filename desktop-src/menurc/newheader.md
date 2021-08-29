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
ms.openlocfilehash: f8ce5407686d5e0e8ad4c0f17856241e9b47c70b2375f93f3b2b9046210d2faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011769"
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

## <a name="remarks"></a>Remarques

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

 

 





