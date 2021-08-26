---
description: Représente une matrice 3x3 qui, à son tour, représente une transformation affine.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: InkTransform, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 4bdc93e2c80f1a7ef4a8eacf1a58288c008e1354cda702e492deb2990e8938d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938659"
---
# <a name="inktransform-class"></a>InkTransform, classe

Représente une matrice 3x3 qui, à son tour, représente une transformation affine.

**InkTransform** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **InkTransform** possède ces méthodes.



| Méthode                                                  | Description                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**GetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | Récupère le **InkTransform** sous la forme de 6 valeurs à virgule flottante.<br/>                                                                      |
| [**Correspond**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | Reflète la transformation dans les directions horizontale ou verticale.<br/>                                          |
| [**Initialisation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | Rétablit l’état d’origine de la transformation.<br/>                                                                      |
| [**Faire pivoter**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | Fait pivoter la transformation d’un angle mesuré en degrés, et spécifie éventuellement un point central pour la rotation.<br/> |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | Met à l’échelle la transformation par facteurs X et Y.<br/>                                                                         |
| [**SetTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | Modifie le **InkTransform** à l’aide de 6 valeurs float.<br/>                                                                    |
| [**Incliné**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | Applique une inclinaison avec les facteurs horizontaux et verticaux spécifiés.<br/>                                              |
| [**Traduire**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | Déplace la transformation selon les composants horizontaux et verticaux spécifiés.<br/>                                         |



 

### <a name="properties"></a>Propriétés

La classe **InkTransform** possède les propriétés suivantes.



| Propriété                                     | Type d’accès           | Description                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**Métadonnée**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | Lecture/écriture<br/> | Obtient ou définit la version Automation de la structure WIN32 XFORM.<br/>                            |
| [**eDx**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | Lecture/écriture<br/> | Obtient ou définit le nombre réel qui spécifie l’élément de la troisième ligne, première colonne.<br/>   |
| [**eDy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | Lecture/écriture<br/> | Obtient ou définit le nombre réel qui spécifie l’élément de la troisième ligne, deuxième colonne.<br/>  |
| [**eM11**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | Lecture/écriture<br/> | Obtient ou définit le nombre réel qui spécifie l’élément dans la première ligne, première colonne.<br/>   |
| [**eM12**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | Lecture/écriture<br/> | Obtient ou définit le nombre réel qui spécifie l’élément dans la première ligne, deuxième colonne.<br/>  |
| [**eM21**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | Lecture/écriture<br/> | Obtient ou définit le nombre réel qui spécifie l’élément dans la deuxième ligne, première colonne.<br/>  |
| [**eM22**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | Lecture/écriture<br/> | Obtient ou définit le nombre réel qui spécifie l’élément dans la deuxième ligne, deuxième colonne.<br/> |



 

## <a name="remarks"></a>Remarques

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

L’objet stocke uniquement six des neuf chiffres dans une matrice 3x3, car toutes les matrices 3x3 qui représentent des transformations affines ont la même troisième colonne (0, 0, 1). Cet objet est utilisé à son tour pour décrire des opérations de transformation telles que le déplacement, la déformation, la mise à l’échelle ou la rotation dans un objet [**InkRenderer**](inkrenderer-class.md) , un objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ou une collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

> [!Note]  
> L’objet **InkTransform** est corrélé à la structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

