---
title: Message d’CDM_GETFOLDERPATH (COMMDLG. h)
description: Récupère le chemin d’accès du dossier ou du répertoire actuellement ouvert pour une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- Boîtes de dialogue de CDM_GETFOLDERPATH message
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff15e72d93e921968601f9c8472901d20769478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942212"
---
# <a name="cdm_getfolderpath-message"></a>\_Message CDM GETFOLDERPATH

\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Récupère le chemin d’accès du dossier ou du répertoire actuellement ouvert pour une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur. La boîte de dialogue doit avoir été créée avec l’indicateur **OFN \_ Explorer** ; sinon, le message échoue.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taille, en caractères, de la mémoire tampon *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit le chemin d’accès.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est la taille, en caractères, de la chaîne de chemin d’accès, y compris le caractère null de fin. Il s’agit du nombre d’octets ou de caractères copiés dans la mémoire tampon, ou de la taille de mémoire tampon requise si la mémoire tampon est trop petite.

Si une erreur se produit, la valeur de retour est inférieure à zéro.

## <a name="remarks"></a>Notes

La macro correspondante est la suivante :

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Configuration requise



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

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

