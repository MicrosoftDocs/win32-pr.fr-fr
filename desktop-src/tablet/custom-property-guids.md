---
description: Les identificateurs globaux uniques (GUID) suivants sont utilisés par le journal Windows pour identifier les propriétés personnalisées sur les traits ou les attributs de dessin.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUID de propriété personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536587"
---
# <a name="custom-property-guids"></a>GUID de propriété personnalisée

Les identificateurs globaux uniques (GUID) suivants sont utilisés par le journal Windows pour identifier les propriétés personnalisées sur les traits ou les attributs de dessin.

## <a name="guid_stroke_timestamp"></a>\_horodateur du trait GUID \_


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



Il s’agit d’une structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) qui indique l’heure à laquelle le trait a été créé ou ajouté au document.


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>\_TimeID traits \_ GUID


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



Il s’agit d’une structure **TimeID** . Cela permet de conserver l’ordre des traits dans les opérations de collage et de suppression. Sans la structure **TimeID** , l’horodateur de tous les objets d' [**interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coupés et collés dans une [collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sera le même.


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>\_Surligneur GUID

Il s’agit d’un **bool**, où **true**= encre du surligneur, **false**= entrée normale. Cela s’applique aux attributs de dessin.


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>STYLE de l’encre du GUID \_ \_ \_ gras

Il s’agit d’un **bool**, où **true**= écriture manuscrite, **false**= normal. Cela s’applique aux attributs de dessin.


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>STYLE de l’encre du GUID \_ \_ \_ italique

Il s’agit d’un **bool**, où **true**= encre en italique, **false**= normal. Cela s’applique aux attributs de dessin.


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IJournalReader**](ijournalreader.md)
</dt> </dl>

 

 
