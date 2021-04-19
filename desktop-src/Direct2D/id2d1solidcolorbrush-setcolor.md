---
title: Méthodes ID2D1SolidColorBrush SetColor
description: Spécifie la couleur de ce pinceau de couleur unie.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Méthodes SetColor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541671"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>ID2D1SolidColorBrush :: SetColor, méthodes

Spécifie la couleur de ce pinceau de couleur unie.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                          | Description                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor (D2D1 de \_ couleur \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | Spécifie la couleur de ce pinceau de couleur unie. <br/> |
| [**SetColor ( \_ couleur d2d1 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | Spécifie la couleur de ce pinceau de couleur unie. <br/> |



## <a name="remarks"></a>Notes

Pour vous aider à créer des couleurs, Direct2D fournit la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) . Il offre plusieurs méthodes d’assistance pour la création de couleurs et fournit un jeu ou des couleurs prédéfinies.

## <a name="examples"></a>Exemples

Le code suivant montre comment utiliser cette méthode.


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

