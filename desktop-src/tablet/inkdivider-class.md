---
description: Représente la capacité à analyser la disposition d’une collection de traits et à les diviser en texte et en graphiques.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: InkDivider, classe (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536401"
---
# <a name="inkdivider-class"></a>InkDivider, classe

Représente la capacité à analyser la disposition d’une collection de traits et à les diviser en texte et en graphiques.

**InkDivider** possède les types de membres suivants :

-   [Interfaces](#interfaces)
-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="interfaces"></a>Interfaces

La classe **InkDivider** définit ces interfaces.



| Interface       | Description                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Cet objet implémente l’interface com **IInkDivider** .<br/> |



 

### <a name="methods"></a>Méthodes

La classe **InkDivider** possède ces méthodes.



| Méthode                              | Description                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Diviser**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Retourne un objet [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) qui contient des informations structurelles sur les traits de l’objet **InkDivider** .<br/> |



 

### <a name="properties"></a>Propriétés

La classe **InkDivider** possède les propriétés suivantes.



| Propriété                                                             | Type d’accès           | Description                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lecture/écriture<br/> | Obtient ou définit la hauteur attendue de l’écriture manuscrite en unités HIMETRIC.<br/>                                                      |
| [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lecture/écriture<br/> | Obtient ou définit l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) utilisé pour la reconnaissance de l’écriture manuscrite.<br/> |
| [**Traits**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lecture/écriture<br/> | Obtient ou définit la collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenue par l’objet **InkDivider** . <br/>     |



 

## <a name="remarks"></a>Notes

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

L’objet **InkDivider** utilise la disposition des traits, l’ordre dans lequel les traits sont ajoutés, la direction dans laquelle les traits sont dessinés et d’autres facteurs pour effectuer l’analyse de l’encre. La collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analysée par l’objet **InkDivider** est contenue dans la propriété [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) de l’objet **InkDivider** . L’objet **InkDivider** analyse dynamiquement la collection InkStrokes à mesure que vous ajoutez ou supprimez la collection, mais il n’effectue aucune modification des traits.

Les résultats de l’analyse sont retournés dans un objet [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

L’objet **InkDivider** utilise un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) pour diviser plus précisément les traits et assigner une chaîne de reconnaissance aux résultats.

> [!Note]  
> L’objet **InkDivider** utilise les paramètres de propriété par défaut de l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) .

 

Si vous n’assignez pas de contexte de module de reconnaissance à l’objet **InkDivider** , l’objet **InkDivider** analyse toujours l’encre, mais divise les traits moins précisément et n’associe pas de texte aux résultats de la Division.

> [!Note]  
> La propriété [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) doit être définie avant l’ajout de traits à la propriété [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) . Une fois que les traits ont été ajoutés à l’objet **InkDivider** , la propriété **RecognizerContext** ne peut pas être modifiée.

 

Le **InkDivider** ne prend pas actuellement en charge les langues verticales. Pour que l’objet **InkDivider** reconnaisse ces langues correctement, l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) de la langue doit prendre en charge la fonctionnalité d’entrée gratuite et les caractères doivent être écrits de gauche à droite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                               |
| En-tête<br/>                   | <dl> <dt>Msinkaut15. h (nécessite également Msinkaut15 \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**InkRecognizerContext, classe**](inkrecognizercontext-class.md)
</dt> <dt>

[Collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

