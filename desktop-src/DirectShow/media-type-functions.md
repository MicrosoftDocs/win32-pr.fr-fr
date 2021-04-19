---
description: Les classes de base DirectShow fournissent des fonctions d’assistance pour gérer la \_ structure du type de média am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Fonctions de type de média (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540963"
---
# <a name="media-type-functions"></a>Fonctions de type de média

Les classes de base DirectShow fournissent des fonctions d’assistance pour gérer la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

La structure du **\_ \_ type de média am** contient un pointeur (le membre **pbFormat** ) vers un autre bloc de mémoire, appelé le *bloc de format*. Par conséquent, lorsque vous utilisez cette structure, vous devez faire attention à l’allocation de mémoire afin d’éviter les fuites de mémoire.

Les fonctions suivantes allouent de la mémoire :

-   **CreateMediaType** alloue une nouvelle structure **de \_ \_ type de média am** et le bloc de format.
-   **CopyMediaType** copie dans une structure **de \_ \_ type de média am** existante, mais alloue le bloc de format.
-   **CreateAudioMediaType** Initialise une structure de **\_ \_ type de média am** existante et alloue éventuellement le bloc de format.

La mémoire disponible pour les fonctions suivantes :

-   **FreeMediaType** libère le bloc de format.
-   **DeleteMediaType** libère une structure **de \_ \_ type de média am** , y compris le bloc de format.



| Fonction                                             | Description                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | Copie une structure de **type de \_ média \_ am** allouée par la tâche.                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | Initialise une structure de type de média en fonction d’une structure de format Wave.                                           |
| [**CreateMediaType**](createmediatype.md)           | Alloue et Initialise une structure de **\_ \_ type de média am** , à partir d’une structure de **\_ \_ type de média am** existante. |
| [**DeleteMediaType**](deletemediatype.md)           | Supprime une structure de **\_ \_ type de média am** allouée par la tâche.                                                     |
| [**FreeMediaType**](freemediatype.md)               | Libère une structure de **\_ \_ type de média am** allouée à la tâche à partir de la mémoire.                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Mtype. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




