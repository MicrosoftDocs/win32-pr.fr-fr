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
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010048"
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
| [**Init**](cseekingpassthru-init.md)                           | Initialise l'objet.            |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Seekpt. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




