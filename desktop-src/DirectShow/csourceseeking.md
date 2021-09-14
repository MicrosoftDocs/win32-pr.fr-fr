---
description: La classe CSourceSeeking est une classe abstraite pour l’implémentation de la recherche dans les filtres sources avec une seule broche de sortie.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: CSourceSeeking, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012253"
---
# <a name="csourceseeking-class"></a>CSourceSeeking, classe

![hiérarchie de la classe csourceseeking](images/cutil15.png)

La classe **CSourceSeeking** est une classe abstraite pour l’implémentation de la recherche dans les filtres sources avec une seule broche de sortie.

Cette classe prend en charge l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Il fournit des implémentations par défaut pour toutes les méthodes **IMediaSeeking** . Les variables membres protégées stockent l’heure de début, l’heure d’arrêt et la vitesse actuelle. Par défaut, le seul format d’heure pris en charge par la classe est l’heure du format de l’heure (unités de 100 nanosecondes). **\_ \_ \_** Pour plus d'informations, consultez la section Notes.



| Variables membres protégées                                          | Description                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**m \_ rtDuration**](csourceseeking-m-rtduration.md)                | Durée du flux.                                                                     |
| [**m \_ rtStart**](csourceseeking-m-rtstart.md)                      | Heure de début                                                                                 |
| [**m \_ rtStop**](csourceseeking-m-rtstop.md)                        | Heure d’arrêt.                                                                                  |
| [**m \_ dRateSeeking**](csourceseeking-m-drateseeking.md)            | Vitesse de lecture.                                                                              |
| [**m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md)          | Fonctionnalités de recherche.                                                                       |
| [**m \_ pLock**](csourceseeking-m-plock.md)                          | Pointeur vers un objet de section critique pour le verrouillage.                                           |
| Méthodes protégées                                                   | Description                                                                                 |
| [**CSourceSeeking**](csourceseeking-csourceseeking.md)             | Méthode de constructeur.                                                                         |
| Méthodes virtuelles pures                                                | Description                                                                                 |
| [**ChangeRate**](csourceseeking-changerate.md)                     | Appelé lorsque la vitesse de lecture change.                                                      |
| [**Modifiez l'**](csourceseeking-changestart.md)                   | Appelé lorsque la position de début change.                                                     |
| [**ChangeStop**](csourceseeking-changestop.md)                     | Appelé lorsque la position d’arrêt change.                                                      |
| Méthodes IMediaSeeking                                               | Description                                                                                 |
| [**IsFormatSupported**](csourceseeking-isformatsupported.md)       | Détermine si un format d’heure spécifié est pris en charge.                                    |
| [**QueryPreferredFormat**](csourceseeking-querypreferredformat.md) | Récupère le format d’heure préféré de l’objet.                                               |
| [**SetTimeFormat**](csourceseeking-settimeformat.md)               | Définit le format d’heure.                                                                       |
| [**IsUsingTimeFormat**](csourceseeking-isusingtimeformat.md)       | Détermine si un format d’heure spécifié est le format en cours d’utilisation.                  |
| [**GetTimeFormat**](csourceseeking-gettimeformat.md)               | Récupère le format d’heure actuel.                                                          |
| [**GetDuration**](csourceseeking-getduration.md)                   | Récupère la durée du flux.                                                       |
| [**GetStopPosition**](csourceseeking-getstopposition.md)           | Récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux. |
| [**GetCurrentPosition**](csourceseeking-getcurrentposition.md)     | Récupère la position actuelle, par rapport à la durée totale du flux.               |
| [**GetCapabilities**](csourceseeking-getcapabilities.md)           | Récupère toutes les fonctionnalités de recherche du flux.                                       |
| [**CheckCapabilities**](csourceseeking-checkcapabilities.md)       | Interroge si le flux a spécifié des fonctionnalités de recherche.                              |
| [**ConvertTimeFormat**](csourceseeking-converttimeformat.md)       | Convertit d’un format d’heure en un autre.                                                   |
| [**SetPositions**](csourceseeking-setpositions.md)                 | Définit la position actuelle et la position d’arrêt.                                            |
| [**GetPositions**](csourceseeking-getpositions.md)                 | Récupère la position actuelle et la position d’arrêt.                                       |
| [**GetAvailable**](csourceseeking-getavailable.md)                 | Récupère la plage de temps pendant laquelle la recherche est efficace.                                 |
| [**Seles**](csourceseeking-setrate.md)                           | Définit la vitesse de lecture.                                                                     |
| [**GetRate**](csourceseeking-getrate.md)                           | Récupère la vitesse de lecture.                                                                |
| [**GetPreroll**](csourceseeking-getpreroll.md)                     | Récupère le temps de préroll.                                                                 |



 

## <a name="remarks"></a>Notes

Chaque fois que la position de début, la position d’arrêt ou la vitesse de lecture change, l’objet **CSourceSeeking** appelle une méthode virtuelle pure correspondante :

-   Position de départ : [ **CSourceSeeking :: modifiez l'**](csourceseeking-changestart.md)
-   Position d’arrêt : [ **CSourceSeeking :: ChangeStop**](csourceseeking-changestop.md)
-   Vitesse de lecture : [ **CSourceSeeking :: ChangeRate**](csourceseeking-changerate.md)

La classe dérivée doit implémenter ces méthodes. Après une opération de recherche, un filtre doit effectuer les opérations suivantes :

1.  Appelez la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée en aval.
2.  Arrêtez le thread de travail qui fournit des données.
3.  Appelez la méthode [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée.
4.  Redémarrez le thread de travail.
5.  Appelez la méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) sur la broche d’entrée.
6.  Définissez la propriété discontinu sur le premier exemple. Appelez la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

L’appel à [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) libère le thread de travail, si le thread est bloqué en attente de remise d’un échantillon.

À l’étape 2, assurez-vous que le thread a cessé d’envoyer des données. Selon l’implémentation, vous devrez peut-être attendre que le thread se termine ou que le thread signale une réponse d’une sorte. Si votre filtre utilise la classe [**CSourceStream**](csourcestream.md) , la méthode [**CSourceStream :: Stop**](csourcestream-stop.md) se bloque jusqu’à ce que le thread de travail réponde.

Dans l’idéal, le nouveau segment (étape 5) doit être remis à partir du thread de travail. Elle peut également être effectuée par l’objet **CSourceSeeking** , à condition que le filtre le sérialise avec les exemples.

L’exemple suivant illustre une implémentation possible. Elle suppose que la broche de sortie du filtre source est dérivée de **CSourceSeeking** et [**CSourceStream**](csourcestream.md). Cet exemple définit une méthode d’assistance, UpdateFromSeek, qui effectue les étapes 1 4. La méthode [**CSourceStream :: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) est substituée pour envoyer le nouveau segment, et pour définir un indicateur qui spécifie la discontinuation. Le thread de travail sélectionne cet indicateur et appelle la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a>Prise en charge de formats d’heure supplémentaires

Par défaut, cette classe prend en charge la recherche uniquement en unités de temps de référence (temps de format de l’heure \_ \_ \_ ). Pour prendre en charge des formats d’heure supplémentaires, substituez les méthodes [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) qui traitent des formats d’heure :

-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

En outre, remplacez les méthodes [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) restantes pour effectuer les conversions nécessaires entre les formats d’heure. Après l’appel de la méthode [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) , toutes les méthodes **IMediaSeeking** doivent traiter les paramètres d’heure entrante et sortante comme étant dans le nouveau format d’heure. Par exemple, si la variable *m \_ rtDuration* représente la durée en unités de temps de référence, mais que le format d’heure actuel est frames, la méthode [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) doit retourner la valeur *m \_ rtDuration* convertie en frames. Par exemple :


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



En outre, assurez-vous de vérifier l' \_ indicateur AM recherché \_ ReturnTime dans la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) . Si cet indicateur est présent, convertissez les valeurs de position en heures de référence lorsque vous les Retournez à l’appelant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge de la recherche dans un filtre source](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




