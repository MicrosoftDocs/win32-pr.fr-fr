---
description: Représente l’accès à un rectangle.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: InkRectangle, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538195"
---
# <a name="inkrectangle-class"></a>InkRectangle, classe

Représente l’accès à un rectangle.

**InkRectangle** possède les types de membres suivants :

-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="interfaces"></a>Interfaces

La classe **InkRectangle** définit ces interfaces.



| Interface         | Description                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkRectangle** | Cet objet implémente l’interface com **IInkRectangle** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkRectangle** possède ces méthodes.



| Méthode                                            | Description                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**GetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Récupère les éléments de l’objet **InkRectangle** en un seul appel.<br/> |
| [**SetRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Modifie les éléments de l’objet **InkRectangle** en un seul appel.<br/>  |



 

### <a name="properties"></a>Propriétés

La classe **InkRectangle** possède les propriétés suivantes.



| Propriété                                         | Type d’accès           | Description                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Bas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Lecture/écriture<br/> | Obtient ou définit la position inférieure du rectangle.<br/>      |
| [**Données**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Lecture/écriture<br/> | Obtient ou définit l’accès au struct rectangle (C++ uniquement).<br/> |
| [**Gauche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Lecture/écriture<br/> | Obtient ou définit la position gauche du rectangle.<br/>        |
| [**Oui**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Lecture/écriture<br/> | Obtient ou définit la position droite du rectangle.<br/>       |
| [**Retour au début**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Lecture/écriture<br/> | Obtient ou définit la position supérieure du rectangle.<br/>         |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Un point se trouve dans un **InkRectangle** s’il se trouve sur le côté [**gauche**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) ou [**supérieur**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) ou se trouve dans les quatre côtés. Un point situé à [**droite**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) ou en [**bas**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) est pris en compte à l’extérieur du rectangle.

 

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

> [!Note]  
> Une **InkRectangle** ne peut pas être utilisée si elle est supérieure à la longueur \_ maximale (2 ^ 31-1) dans l’une ou l’autre dimension.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

