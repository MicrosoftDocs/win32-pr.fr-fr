---
title: ImageList_SetColorTable fonction)
description: Définit la table des couleurs pour une liste d’images.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable Windows des contrôles de fonction
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412237"
---
# <a name="imagelist_setcolortable-function"></a>\_Fonction SetColorTable ImageList

Définit la table des couleurs pour une liste d’images.

## <a name="syntax"></a>Syntaxe


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*himl* \[ dans\]
</dt> <dd>

Type : **HIMAGELIST**

Handle de la liste d’images.

</dd> <dt>

*Démarrer* \[ dans\]
</dt> <dd>

Type : **int**

Index de table de couleur de base zéro qui spécifie la première entrée de la table des couleurs à définir.

</dd> <dt>

*Len* \[ dans\]
</dt> <dd>

Type : **int**

Nombre d’entrées de table des couleurs à définir.

</dd> <dt>

*prgb* \[ dans\]
</dt> <dd>

Type : **[ **RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

Pointeur vers un tableau de structures  [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) Len contenant de nouvelles informations de couleur pour la table des couleurs du dib.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Si la fonction est réussie, elle retourne le nombre d’entrées de table des couleurs définies par la fonction. Si la fonction échoue, la valeur de retour est inférieure ou égale à zéro.

## <a name="remarks"></a>Remarques

Seules les listes d’images créées avec l’indicateur [**ILC \_ color4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ou [**ILC \_ color8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) ont des tables de couleurs. La table des couleurs d’une telle liste d’images est généralement définie automatiquement en copiant la table des couleurs de la première image ajoutée à la liste (par exemple, à l’aide de la fonction [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ) si cette image est un dib. Si la première image ajoutée à la liste d’images n’est pas un DIB, la table des couleurs de la palette de demi-teintes est utilisée pour les listes d’images **ILC \_ color8** et la table de couleurs VGA est utilisée pour **ILC \_ color4**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 3,51 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table des couleurs](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

