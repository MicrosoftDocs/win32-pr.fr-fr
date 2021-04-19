---
title: Message TB_ADDSTRING (commctrl. h)
description: Ajoute une nouvelle chaîne au pool de chaînes de la barre d’outils.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509759"
---
# <a name="tb_addstring-message"></a>TO \_ message ADDSTRING

Ajoute une nouvelle chaîne au pool de chaînes de la barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de l’instance de module avec un fichier exécutable qui contient la ressource de chaîne. Si *lParam* pointe plutôt vers un tableau de caractères avec une ou plusieurs chaînes, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur de ressource de la ressource de type chaîne, ou pointeur vers un tableau TCHAR. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de la première nouvelle chaîne en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Si *wParam* a la **valeur null**, *lParam* pointe vers un tableau de caractères avec une ou plusieurs chaînes se terminant par un caractère null. La dernière chaîne dans le tableau doit se terminer par deux caractères null.

Si *wParam* est le HINSTANCE de l’application ou d’un autre module contenant une ressource de type chaîne, *lParam* est l’identificateur de ressource de la chaîne. Chaque élément de la chaîne doit commencer par un caractère de séparation arbitraire, et la chaîne doit se terminer par deux caractères. Par exemple, le texte de trois boutons peut apparaître dans la table de chaînes sous la forme « /New/Open/Save// ». Le message retourne l’index de « New » dans le pool de chaînes de la barre d’outils, et les autres éléments se trouvent à des positions consécutives.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ ADDSTRINGW** (Unicode) et **to \_ ADDSTRINGA** (ANSI)<br/>                 |



 

 





