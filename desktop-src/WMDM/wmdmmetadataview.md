---
title: WMDMMetadataView, structure
description: La structure WMDMMetadataView définit la vue de métadonnées. Le contenu est organisé en fonction de cette définition.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Structure WMDMMetadataView Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e442ed3058f1982ac7607c6b8a29e5df321d69776695821b278049e27cd7589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862589"
---
# <a name="wmdmmetadataview-structure"></a>WMDMMetadataView, structure

La structure **WMDMMetadataView** définit la vue de métadonnées. Le contenu est organisé en fonction de cette définition.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>Membres

<dl> <dt>

**pwszViewName**
</dt> <dd>

Pointeur vers une chaîne de caractères larges se terminant par un caractère null qui contient le nom de la vue. Il est utilisé comme nom du nœud racine sous lequel cette vue est présentée.

</dd> <dt>

**nDepth**
</dt> <dd>

Entier contenant la profondeur de la vue, qui indique le nombre de balises de métadonnées imbriquées utilisées pour la vue.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Tableau de chaînes de balises de métadonnées pour les balises imbriquées.

</dd> </dl>

## <a name="examples"></a>Exemples

Le code suivant crée une vue de métadonnées :


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



Le code précédent organise le contenu comme suit :

<dl> Ma vue<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





