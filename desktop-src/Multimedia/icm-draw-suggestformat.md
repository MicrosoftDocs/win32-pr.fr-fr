---
title: Message ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: la ICM \_ message de dessin \_ SUGGESTFORMAT interroge un pilote de rendu pour suggérer un format décompressé qu’il peut dessiner.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- message ICM_DRAW_SUGGESTFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364208"
---
# <a name="icm_draw_suggestformat-message"></a>ICM \_ DESSINER le \_ message SUGGESTFORMAT

la **ICM message de \_ dessin \_ SUGGESTFORMAT** interroge un pilote de rendu pour suggérer un format décompressé qu’il peut dessiner.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Pointeur vers une structure [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite. Si le membre **lpbiSuggest** de la structure [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) est **null**, ce message retourne la quantité de mémoire nécessaire pour contenir le format suggéré.

## <a name="remarks"></a>Remarques

Le pilote doit examiner le format spécifié dans le membre **lpbiIn** de la structure [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) et utiliser le membre **lpbiSuggest** pour retourner un format qu’il peut dessiner. Le format de sortie doit conserver autant de données que possible à partir du format d’entrée.

Le cas échéant, le pilote peut utiliser le descripteur de compresseur installable passé dans le membre **hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) pour effectuer des sélections plus complexes. Par exemple, si le format d’entrée est données JPEG de 24 bits, un convertisseur peut interroger le décompresseur pour déterminer s’il peut être décompressé dans un format YUV (qui peut être dessiné plus efficacement) avant de sélectionner le format à suggérer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





