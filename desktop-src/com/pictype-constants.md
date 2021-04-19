---
title: Constantes PICTYPE (OleCtl. h)
description: Décrivez le type d’un objet Picture tel qu’il est retourné par le type d’extraction IPicture, ainsi que \_ pour décrire le type d’image dans le membre picType de la structure PICTDESC transmise à OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511550"
---
# <a name="pictype-constants"></a>Constantes PICTYPE

Décrit le type d’un objet image tel qu’il est retourné par [**IPicture :: obtenir le \_ type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), ainsi que pour décrire le type d’image dans le membre **PicType** de la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) qui est passée à [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).



| Constante/valeur                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_ Non initialisé**</dt> <dt>(-1)</dt> </dl> | L’objet image n’est pas actuellement initialisé. Cette valeur est valide uniquement en tant que valeur de retour du [**\_ type ipicture :: obtenir**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) et n’est pas valide avec la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_ AUCUN**</dt> <dt>0</dt> </dl>                               | Un nouvel objet Picture doit être créé sans l’État Initialized. Cette valeur est valide uniquement dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt> </dl>                         | Le type Picture est un bitmap. Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ **BMP** de cette structure contient les paramètres d’initialisation appropriés.<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_ MÉTAFICHIER**</dt> <dt>2</dt> </dl>                   | Le type Picture est un métafichier. Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ **WMF** de cette structure contient les paramètres d’initialisation appropriés.<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_ ICÔNE**</dt> <dt>3</dt> </dl>                               | Le type d’image est une icône. Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ d' **icône** de cette structure contient les paramètres d’initialisation appropriés.<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt> </dl>          | Le type Picture est un métafichier amélioré. Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ **EMF** de cette structure contient les paramètres d’initialisation appropriés.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>OleCtl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPicture :: obten, \_ type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





