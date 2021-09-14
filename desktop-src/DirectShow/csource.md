---
description: La classe CSource est une classe de base pour l’implémentation de filtres sources. Un filtre dérivé de CSource contient une ou plusieurs broches de sortie dérivées de la classe CSourceStream. Chaque broche de sortie crée un thread de travail qui pousse les exemples de média en aval.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010025"
---
# <a name="csource-class"></a>CSource, classe

![hiérarchie de la classe CSource](images/source01.png)

La classe **CSource** est une classe de base pour l’implémentation de filtres sources. Un filtre dérivé de **CSource** contient une ou plusieurs broches de sortie dérivées de la classe [**CSourceStream**](csourcestream.md) . Chaque broche de sortie crée un thread de travail qui pousse les exemples de média en aval.

> [!Note]  
> La classe **CSource** est conçue pour prendre en charge le modèle push pour le workflow de données. Cette classe n’est pas recommandée pour créer des filtres de lecteur de fichier. Les lecteurs de fichiers doivent prendre en charge le modèle d’extraction par le biais de l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . pour plus d’informations, consultez [Flow de données pour les développeurs de filtres](data-flow-for-filter-developers.md).

 



| Variables membres protégées                     | Description                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**m \_ iPins**](csource-m-ipins.md)            | Nombre de broches sur le filtre.                                |
| [**m \_ paStreams**](csource-m-pastreams.md)    | Tableau de codes confidentiels.                                               |
| [**m \_ cStateLock**](csource-m-cstatelock.md)  | Objet de section critique qui protège l’état du filtre.      |
| M&#233;thodes publiques                                 | Description                                                  |
| [**CSource**](csource-csource.md)             | Méthode de constructeur.                                          |
| [**~ CSource**](csource--csource.md)           | Méthode de destructeur.                                           |
| [**GetPinCount**](csource-getpincount.md)     | Récupère le nombre de broches sur le filtre.                  |
| [**GetPin**](csource-getpin.md)               | Récupère un code confidentiel.                                             |
| [**pStateLock**](csource--pstatelock.md)      | Récupère un pointeur vers l’objet de section critique du filtre. |
| [**AddPin**](csource-addpin.md)               | Ajoute une nouvelle broche de sortie au filtre.                         |
| [**RemovePin**](csource-removepin.md)         | Supprime un pin spécifié du filtre.                     |
| [**FindPinNumber**](csource-findpinnumber.md) | Récupère le numéro d’un pin spécifié sur le filtre.       |
| Méthodes IBaseFilter                            | Description                                                  |
| [**FindPin**](csource-findpin.md)             | Récupère le code confidentiel avec l’identificateur spécifié.             |



 

## <a name="remarks"></a>Notes

Pour implémenter une broche de sortie, procédez comme suit :

-   Dérivez une classe de [**CSourceStream**](csourcestream.md).
-   Substituez la méthode [**CSourceStream :: GetMediaType**](csourcestream-getmediatype.md) et éventuellement la méthode [**CSourceStream :: CheckMediaType**](csourcestream-checkmediatype.md) , qui valide les types de média pour le code confidentiel.
-   Implémentez la méthode [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , qui retourne les exigences de mémoire tampon du pin.
-   Implémentez la méthode [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) , qui remplit un exemple de mémoire tampon de média avec des données.

Pour implémenter le filtre, procédez comme suit :

-   Dérivez une classe de **CSource**.
-   Dans le constructeur, créez une ou plusieurs broches de sortie dérivées de [**CSourceStream**](csourcestream.md). Les codes confidentiels s’ajoutent automatiquement au filtre dans leurs méthodes de constructeur et se suppriment dans leurs méthodes de destructeur.

Pour synchroniser l’état de filtre entre plusieurs threads, appelez la méthode [**CSource ::P statelock**](csource--pstatelock.md) . Cette méthode retourne un pointeur vers la section critique de l’état de filtre. Utilisez la classe [**CAutoLock**](cautolock.md) pour contenir la section critique. À partir d’un code confidentiel, vous pouvez accéder à **pStateLock** à partir de la variable membre [**CBasePin :: m \_ pFilter**](cbasepin-m-pfilter.md) du pin, comme suit :


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Écriture de filtres source](writing-source-filters.md)
</dt> </dl>

 

 




