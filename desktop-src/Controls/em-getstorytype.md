---
title: Message EM_GETSTORYTYPE (RichEdit. h)
description: Obtient le type d’histoire.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- EM_GETSTORYTYPE les contrôles de message Windows
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
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843485"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETSTORYTYPE em**](em-setstorytype.md)
</dt> <dt>

[**ITextStoryRanges :: Item**](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





