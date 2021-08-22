---
description: La classe CSeekingPassThru est un objet d’assistance qui crée des objets CPosPassThru et CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: CSeekingPassThru, classe (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ffb8436623cb5ba5f415ceb8bbdafe00e22487da2bbfaba5d02ee4c8f189c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953768"
---
# <a name="cseekingpassthru-class"></a>CSeekingPassThru, classe

La `CSeekingPassThru` classe est un objet d’assistance qui crée des objets [**CPosPassThru**](cpospassthru.md) et [**CRendererPosPassThru**](crendererpospassthru.md) .

Les classes **CPosPassThru** et **CRendererPosPassThru** sont des objets d’assistance qui transmettent des commandes en amont, de sorte que la `CSeekingPassThru` classe est un objet d’assistance pour créer des objets d’assistance.

Il n’est pas nécessaire d’utiliser cette classe directement. Utilisez plutôt la fonction [**CreatePosPassThru**](createpospassthru.md) , qui gère tous les détails de l’utilisation de cette classe. Elle présente l’avantage supplémentaire de charger l’objet à partir de Quartz.dll, ce qui réduit quelque peu la taille du code de votre filtre. Pour plus d’informations, consultez [**CPosPassThru**](cpospassthru.md).

La `CSeekingPassThru` classe expose l’interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) . La méthode [**ISeekingPassThru :: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Initialise l’objet. Une fois l’objet initialisé, le filtre peut l’interroger pour les interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) et [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .



| M&#233;thodes publiques                                                  | Description                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | Méthode de constructeur.                |
| [**~ CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | Méthode de destructeur.                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | Crée une instance de l’objet. |
| Méthodes ISeekingPassThru                                        | Description                        |
| [**Rein**](cseekingpassthru-init.md)                           | Initialise l'objet.            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Seekpt. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




