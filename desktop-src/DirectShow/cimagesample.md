---
description: La classe CImageSample implémente un exemple de média qui gère une image bitmap indépendante du périphérique (DIB) GDI.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: CImageSample, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afd19b6aba7546ec420985adf6d58d3f7acc7546913ec8f1c168c80ad3b7ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402405"
---
# <a name="cimagesample-class"></a>CImageSample, classe

![hiérarchie de la classe cimagesample](images/wutil03.png)

La `CImageSample` classe implémente un exemple de média qui gère une image bitmap indépendante du périphérique (DIB) GDI. Cette classe dérive de la classe [**CMediaSample**](cmediasample.md) . Elle est destinée à être utilisée avec la classe [**CImageAllocator**](cimageallocator.md) . La classe **CImageAllocator** fournit un allocateur qui crée des `CImageSample` objets.



| Variables membres protégées                        | Description                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**m \_ DibData**](cimagesample-m-dibdata.md)      | Contient des informations sur le DIB que cet objet gère.  |
| [**m \_ bInit**](cimagesample-m-binit.md)          | Indique si l’objet a été initialisé.                |
| M&#233;thodes publiques                                    | Description                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Méthode de constructeur.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Récupère des informations sur le DIB que cet objet gère. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Définit des informations sur le DIB que cet objet gère.      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




