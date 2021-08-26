---
description: La classe CMediaSample définit un exemple de support qui prend en charge l’interface IMediaSample2. L’exemple de support contient un pointeur vers une mémoire tampon et diverses propriétés stockées en tant que variables membres protégées.
ms.assetid: 1e609c7c-3200-4540-904e-7659976df0da
title: CMediaSample, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b0b27c8878a2841eeecb3bc1ae24bdcc43d056c57a881596179f5d2bd990fcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084489"
---
# <a name="cmediasample-class"></a>CMediaSample, classe

![hiérarchie de la classe cmediasample](images/wutil03.png)

La `CMediaSample` classe définit un exemple de média qui prend en charge l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) . L’exemple de support contient un pointeur vers une mémoire tampon et diverses propriétés stockées en tant que variables membres protégées.

Les exemples de média sont créés par des allocateurs, qui sont dérivés de la classe [**CBaseAllocator**](cbaseallocator.md) . Le `CMediaSample` constructeur reçoit un pointeur vers une mémoire tampon allouée, ainsi que la taille de la mémoire tampon. D’autres propriétés sont généralement définies et récupérées par le biais de méthodes d’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .

Le cycle de vie d’un exemple de média diffère de celui de la plupart des objets COM :

-   L’Allocator contient une liste d’échantillons gratuits. Lorsqu’un filtre a besoin d’un nouvel exemple, il appelle la méthode [**IMemAllocator :: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) de l’allocateur. L’Allocator récupère un exemple à partir de sa liste libre, incrémente le décompte de références de l’exemple et retourne un pointeur vers l’exemple.
-   Une fois le filtre terminé avec l’exemple, il appelle la méthode **IUnknown :: Release** sur l’exemple. Contrairement à la plupart des objets, l’exemple ne se supprime pas quand son décompte de références atteint zéro. Au lieu de cela, il appelle la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) sur l’allocateur, et l’allocateur retourne l’exemple à sa liste libre.
-   L’Allocator ne détruit pas les exemples tant que la méthode [**IMemAllocator ::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) est appelée.



| Variables membres protégées                                           | Description                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**m \_ dwFlags**](cmediasample-m-dwflags.md)                         | Exemples d’indicateurs de propriété.                                                                          |
| [**m \_ dwTypeSpecificFlags**](cmediasample-m-dwtypespecificflags.md) | Indicateurs spécifiques au type.                                                                            |
| [**m \_ pbuffer**](cmediasample-m-pbuffer.md)                         | Pointeur vers la mémoire tampon qui contient les données multimédia.                                      |
| [**m \_ lActual**](cmediasample-m-lactual.md)                         | Longueur des données valides dans la mémoire tampon, en octets.                                               |
| [**m \_ cbBuffer**](cmediasample-m-cbbuffer.md)                       | Taille de la mémoire tampon, en octets.                                                                   |
| [**m \_ pAllocator**](cmediasample-m-pallocator.md)                   | Pointeur vers l’allocateur qui a créé cet exemple.                                              |
| [**m \_ pNext**](cmediasample-m-pnext.md)                             | Pointeur vers l’exemple suivant dans la liste des exemples de l’allocateur.                                  |
| [**\_début m**](cmediasample-m-start.md)                             | Heure de début de l’exemple.                                                                              |
| [**\_fin m**](cmediasample-m-end.md)                                 | Heure de fin de l’exemple.                                                                                |
| [**m \_ MediaStart**](cmediasample-m-mediastart.md)                   | Heure de début du média.                                                                               |
| [**m \_ MediaEnd**](cmediasample-m-mediaend.md)                       | Heure d’arrêt du support.                                                                                |
| [**m \_ pMediaType**](cmediasample-m-pmediatype.md)                   | Pointeur vers le type de média, si le type a été modifié par rapport à l’exemple précédent dans le flux de données. |
| [**m \_ dwStreamId**](cmediasample-m-dwstreamid.md)                   | Identificateur de flux.                                                                              |
| Variables membres publiques                                              | Description                                                                                     |
| [**m \_ cref**](cmediasample-m-cref.md)                               | Nombre de références.                                                                                |
| M&#233;thodes publiques                                                       | Description                                                                                     |
| [**CMediaSample**](cmediasample-cmediasample.md)                    | Méthode de constructeur.                                                                             |
| [**~ CMediaSample**](cmediasample--cmediasample.md)                 | Méthode de destructeur. Virtuels.                                                                     |
| [**SetPoint**](cmediasample-setpointer.md)                        | Définit le pointeur sur la mémoire tampon.                                                          |
| Méthodes IMediaSample                                                 | Description                                                                                     |
| [**GetPointer**](cmediasample-getpointer.md)                        | Récupère un pointeur en lecture/écriture dans la mémoire tampon.                                                   |
| [**GetSize**](cmediasample-getsize.md)                              | Récupère la taille de la mémoire tampon.                                                               |
| [**GetTime**](cmediasample-gettime.md)                              | Récupère les temps de flux auxquels cet exemple doit commencer et se terminer.                        |
| [**SetTime**](cmediasample-settime.md)                              | Définit les temps de flux auxquels cet exemple doit commencer et se terminer.                             |
| [**IsSyncPoint**](cmediasample-issyncpoint.md)                      | Détermine si le début de l’exemple est un point de synchronisation.                           |
| [**SetSyncPoint**](cmediasample-setsyncpoint.md)                    | Spécifie si le début de cet exemple est un point de synchronisation.                      |
| [**IsPreroll**](cmediasample-ispreroll.md)                          | Détermine si cet exemple est un exemple de préroll.                                                  |
| [**SetPreroll**](cmediasample-setpreroll.md)                        | Spécifie si cet exemple est un exemple de préroll.                                              |
| [**GetActualDataLength**](cmediasample-getactualdatalength.md)      | Récupère la longueur des données valides dans la mémoire tampon.                                           |
| [**SetActualDataLength**](cmediasample-setactualdatalength.md)      | Définit la longueur des données valides dans la mémoire tampon.                                                |
| [**GetMediaType**](cmediasample-getmediatype.md)                    | Récupère le type de média si le type de média diffère de l’exemple précédent.                   |
| [**SetMediaType**](cmediasample-setmediatype.md)                    | Définit le type de média pour l’exemple.                                                             |
| [**IsDiscontinuity**](cmediasample-isdiscontinuity.md)              | Détermine si cet exemple représente une rupture dans le flux de données.                                |
| [**SetDiscontinuity**](cmediasample-setdiscontinuity.md)            | Spécifie si cet exemple représente une rupture dans le flux de données.                            |
| [**GetMediaTime**](cmediasample-getmediatime.md)                    | Récupère les temps de support pour cet exemple.                                                      |
| [**SetMediaTime**](cmediasample-setmediatime.md)                    | Définit les durées de support pour cet exemple.                                                           |
| Méthodes IMediaSample2                                                | Description                                                                                     |
| [**GetProperties**](cmediasample-getproperties.md)                  | Récupère les propriétés de l’exemple.                                                         |
| [**SetProperties**](cmediasample-setproperties.md)                  | Définit les propriétés de l’exemple.                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




