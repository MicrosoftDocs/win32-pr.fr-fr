---
description: La classe CPosPassThru gère les commandes de recherche pour les filtres de transformation, en les passant en amont au filtre suivant.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: CPosPassThru, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230382"
---
# <a name="cpospassthru-class"></a>CPosPassThru, classe

![hiérarchie de la classe de base cpospassthru](images/cutil14.png)

La `CPosPassThru` classe gère les commandes de recherche pour les filtres de transformation, en les passant en amont au filtre suivant.

quand une application recherche le graphique de filtre, le gestionnaire de Graph de filtre donne la commande seek aux filtres de convertisseur. La commande est passée en amont, via la broche de sortie de chaque filtre, jusqu’à ce qu’elle atteigne un filtre qui peut exécuter la commande (le cas échéant). Pour plus d’informations, consultez [recherche](seeking.md). La `CPosPassThru` classe transmet toutes les commandes Seek à la broche de sortie sur le filtre en amont, comme indiqué dans le diagramme suivant.

![la classe cpospassthru envoie des commandes de recherche en amont.](images/cpospassthru.png)

bien que cette classe soit fournie dans la bibliothèque de classes de base, DirectShow fournit également la même classe dans Quartz.dll. L’utilisation de la version Quartz.dll peut être légèrement réduite dans votre filtre, car la classe est chargée au moment de l’exécution à partir de la DLL. Pour utiliser cette version, appelez la fonction [**CreatePosPassThru**](createpospassthru.md) .

Dans la méthode **NonDelegatingQueryInterface** de votre code confidentiel de sortie, déléguez à l’objet **CPosPassThru** chaque fois que l’interface demandée est [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ou [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), comme illustré dans le code suivant :


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



Sauf indication contraire, toutes les méthodes [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de cette classe appellent la méthode correspondante sur l’épingle connectée et retournent le résultat.



| M&#233;thodes publiques                                                    | Description                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CPosPassThru**](cpospassthru-cpospassthru.md)                 | Méthode de constructeur.                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | Obsolète.                                                                                           |
| [**GetMediaTime**](cpospassthru-getmediatime.md)                 | Récupère les horodatages de l’échantillon actuel. Virtuels.                                           |
| Méthodes IMediaPosition                                            | Description                                                                                         |
| [**Obtient la \_ durée**](cpospassthru-get-duration.md)                | Récupère la durée du flux.                                                               |
| [**put \_ CurrentPosition**](cpospassthru-put-currentposition.md)  | Définit la position actuelle, par rapport à la durée totale du flux.                            |
| [**Obtient \_ StopTime**](cpospassthru-get-stoptime.md)                | Récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.         |
| [**put \_ StopTime**](cpospassthru-put-stoptime.md)                | Définit l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.              |
| [**Obtient \_ PrerollTime**](cpospassthru-get-prerolltime.md)          | Récupère la quantité de données qui seront placées en file d’attente avant la position de début.                         |
| [**put \_ PrerollTime**](cpospassthru-put-prerolltime.md)          | Définit la quantité de données qui seront placées en file d’attente avant la position de début.                              |
| [**taux d’accès \_**](cpospassthru-get-rate.md)                        | Récupère la vitesse de lecture.                                                                        |
| [**taux de placement \_**](cpospassthru-put-rate.md)                        | Définit la vitesse de lecture.                                                                             |
| [**Obtient \_ CurrentPosition**](cpospassthru-get-currentposition.md)  | Récupère la position actuelle, par rapport à la durée totale du flux.                       |
| [**CanSeekForward**](cpospassthru-canseekforward.md)             | Détermine si le flux peut être recherché en arrière.                                               |
| [**CanSeekBackward**](cpospassthru-canseekbackward.md)           | Détermine si le flux peut être recherché par progression.                                                |
| Méthodes IMediaSeeking                                             | Description                                                                                         |
| [**CheckCapabilities**](cpospassthru-checkcapabilities.md)       | Interroge si un flux a spécifié des fonctionnalités de recherche.                                        |
| [**ConvertTimeFormat**](cpospassthru-converttimeformat.md)       | Convertit d’un format d’heure en un autre.                                                           |
| [**GetAvailable**](cpospassthru-getavailable.md)                 | Récupère la plage de temps pendant laquelle la recherche est efficace.                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | Récupère toutes les fonctionnalités de recherche du flux.                                               |
| [**GetCurrentPosition**](cpospassthru-getcurrentposition.md)     | Récupère la position actuelle, par rapport à la durée totale du flux.                       |
| [**GetDuration**](cpospassthru-getduration.md)                   | Récupère la durée du flux.                                                               |
| [**GetPositions**](cpospassthru-getpositions.md)                 | Récupère la position actuelle et la position d’arrêt, par rapport à la durée totale du flux. |
| [**GetPreroll**](cpospassthru-getpreroll.md)                     | Récupère la quantité de données qui seront placées en file d’attente avant la position de début.                         |
| [**GetRate**](cpospassthru-getrate.md)                           | Récupère la vitesse de lecture.                                                                        |
| [**GetStopPosition**](cpospassthru-getstopposition.md)           | Récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | Récupère le format d’heure actuel.                                                                  |
| [**IsFormatSupported**](cpospassthru-isformatsupported.md)       | Détermine si un format d’heure spécifié est pris en charge.                                            |
| [**IsUsingTimeFormat**](cpospassthru-isusingtimeformat.md)       | Détermine si un format d’heure spécifié est le format en cours d’utilisation.                          |
| [**QueryPreferredFormat**](cpospassthru-querypreferredformat.md) | Récupère le format d’heure par défaut pour le flux.                                                 |
| [**SetPositions**](cpospassthru-setpositions.md)                 | Définit la position actuelle et la position d’arrêt.                                                    |
| [**Seles**](cpospassthru-setrate.md)                           | Définit la vitesse de lecture.                                                                             |
| [**SetTimeFormat**](cpospassthru-settimeformat.md)               | Définit le format d’heure.                                                                               |
| Fonctions d’assistance                                                  | Description                                                                                         |
| [**CreatePosPassThru**](createpospassthru.md)                    | Crée un `CPosPassThru` objet ou [**CRendererPosPassThru**](crendererpospassthru.md) .            |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




