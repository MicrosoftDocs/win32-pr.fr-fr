---
description: les classes de base DirectShow fournissent des fonctions d’assistance pour gérer la \_ structure du TYPE de média AM \_ .
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
ms.openlocfilehash: ef47b944d5d445f57779f99cb8517a773a7efba19ae3f2133f896fcba7b86548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153157"
---
# <a name="media-type-functions"></a>Fonctions de type de média

les classes de base DirectShow fournissent des fonctions d’assistance pour gérer la structure du [**\_ \_ TYPE de média AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

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
| En-tête<br/>  | <dl> <dt>Mtype. h (include Flux. h)</dt> </dl>                                                                                     |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




