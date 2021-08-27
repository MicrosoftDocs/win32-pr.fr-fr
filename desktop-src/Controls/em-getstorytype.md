---
title: Message EM_GETSTORYTYPE (RichEdit. h)
description: Obtient le type d’histoire.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- EM_GETSTORYTYPE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e6d501fffca857e1e283f2678c1b42e5d3d12e587e51a3a58585041489f8b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048779"
---
# <a name="em_getstorytype-message"></a>\_Message GETSTORYTYPE em

Obtient le type d’histoire.


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’histoire.

</dd> <dt>

*lParam* 
</dt> <dd>

Réservé doit être égal à 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le type d’histoire, qui peut être une valeur personnalisée définie par le client, ou l’une des valeurs suivantes :

<dl> <dt>

**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> <dt>

**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETSTORYTYPE em**](em-setstorytype.md)
</dt> <dt>

[**ITextStoryRanges :: Item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





