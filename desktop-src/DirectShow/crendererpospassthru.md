---
description: La classe CRendererPosPassThru gère les commandes de recherche pour les filtres de convertisseur, en les passant en amont au filtre suivant.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: CRendererPosPassThru, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 68d880a50b66190c64de19f98fd4ac9f06dffa79932d19c7f90654689e51811c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831459"
---
# <a name="crendererpospassthru-class"></a>CRendererPosPassThru, classe

![hiérarchie de la classe crendererpospassthru](images/cutil14.png)

La `CRendererPosPassThru` classe gère les commandes de recherche pour les filtres de convertisseur, en les passant en amont au filtre suivant.

Cette classe dérive de la classe [**CPosPassThru**](cpospassthru.md) . Elle ajoute la prise en charge de la mise en cache des horodatages à partir des exemples à mesure qu’ils arrivent. Utilisez cette classe de la même façon que la classe **CPosPassThru** . Pour plus d’informations, consultez la documentation de **CPosPassThru** .

Le filtre de convertisseur doit mettre à jour les `CRendererPosPassThru` horodatages mis en cache de l’objet, comme suit :

-   Pour chaque exemple reçu par le filtre, appelez la méthode [**CRendererPosPassThru :: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .
-   Lorsque le filtre est arrêté ou reçoit un appel **EndFlush** , appelez la méthode [**CRendererPosPassThru :: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .
-   Lorsque le filtre reçoit une notification de fin de flux, appelez la méthode [**CRendererPosPassThru :: EOS**](crendererpospassthru-eos.md) .

Pour obtenir un exemple d’utilisation de cette classe, reportez-vous au code source [**CBaseRenderer**](cbaserenderer.md) .



| M&#233;thodes publiques                                                            | Description                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**CRendererPosPassThru**](crendererpospassthru-crendererpospassthru.md) | Méthode de constructeur.                                                 |
| [**GetMediaTime**](crendererpospassthru-getmediatime.md)                 | Récupère les horodatages de l’échantillon actuel.                    |
| [**RegisterMediaTime**](crendererpospassthru-registermediatime.md)       | Met en cache les horodatages de l’échantillon actuel.                     |
| [**ResetMediaTime**](crendererpospassthru-resetmediatime.md)             | Réinitialise les horodatages mis en cache à zéro.                              |
| [**EOS**](crendererpospassthru-eos.md)                                   | Met à jour les horodatages mis en cache après une notification de fin de flux. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




