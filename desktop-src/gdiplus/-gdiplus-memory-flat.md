---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plates sont encapsulées par la classe C++ GdiplusBase.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Fonctions de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395824"
---
# <a name="memory-functions"></a>Fonctions de mémoire

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement. Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).

Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Fonctions de mémoire et méthodes Wrapper correspondantes



| Fonction plate                                          | Méthode Wrapper                                                                                                                                      | Remarques                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc (taille \_ t taille)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new) (taille \_ t en \_ taille)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Alloue de la mémoire pour un objet GDI+ Windows. <br/> GdipAlloc est déclaré dans GdiplusMem. h.<br/>  |
| GpStatus WINGDIPAPI GdipFree (void \* PTR);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (opérateur delete) (void \* dans \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Libère de la mémoire pour un objet GDI+ Windows. <br/> GdipFree est déclaré dans GdiplusMem. h.<br/> |



 

 

 
