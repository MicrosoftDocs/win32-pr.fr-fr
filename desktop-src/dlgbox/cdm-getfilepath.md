---
title: Message d’CDM_GETFILEPATH (COMMDLG. h)
description: Récupère le chemin d’accès et le nom de fichier du fichier sélectionné dans une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- Boîtes de dialogue de CDM_GETFILEPATH message
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdb7739cd2ab66362e18cc70f9937e75f80a82d9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590916"
---
# <a name="cdm_getfilepath-message"></a>\_Message CDM GETFILEPATH

\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Récupère le chemin d’accès et le nom de fichier du fichier sélectionné dans une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur. La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taille, en caractères, de la mémoire tampon *lParam* . Pour la version ANSI, il s’agit du nombre d’octets ; pour la version Unicode, il s’agit du nombre de caractères.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit le nom et le chemin d’accès du fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, du nom de fichier et de la chaîne de chemin d’accès, y compris le caractère NULL de fin. Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.

Si une erreur se produit, la valeur de retour est inférieure à zéro.

## <a name="remarks"></a>Remarques

La macro correspondante est la suivante :

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

