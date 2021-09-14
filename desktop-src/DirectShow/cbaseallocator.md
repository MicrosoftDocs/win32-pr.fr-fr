---
description: La classe CBaseAllocator est une classe de base abstraite qui implémente un allocateur. Les allocateurs exposent l’interface IMemAllocator.
ms.assetid: 3c9003d8-f15c-4e85-9712-9aaa87dffdf3
title: CBaseAllocator, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 068dd45ee3ffac5c3b915c3b0cdd8bc87756377e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012296"
---
# <a name="cbaseallocator-class"></a>CBaseAllocator, classe

![hiérarchie de la classe cbaseallocator](images/filter10.png)

La classe **CBaseAllocator** est une classe de base abstraite qui implémente un allocateur. Les allocateurs exposent l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Un *allocateur* est un objet qui alloue des mémoires tampons de mémoire. L’Allocator gère une liste de mémoires tampons disponibles. Lorsqu’un client (généralement un filtre) demande une mémoire tampon, l’allocateur en extrait un de la liste. Le client remplit la mémoire tampon avec des données et peut passer la mémoire tampon à un autre objet. Finalement, la mémoire tampon est libérée et l’allocateur la renvoie à la liste des mémoires tampons disponibles.

Chaque mémoire tampon est encapsulée par un objet appelé *exemple de support*. Les exemples de média sont un moyen de empaqueter des pointeurs vers des blocs de mémoire au sein de l’infrastructure COM (Component Object Model). Les exemples de média exposent l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) et sont implémentés à l’aide de la classe [**CMediaSample**](cmediasample.md) . Un exemple de support contient un pointeur vers la mémoire tampon associée, accessible en appelant la méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) . Pour plus d’informations, consultez [Samples and allocators](samples-and-allocators.md).

Pour utiliser cette classe, procédez comme suit :

1.  Appelez la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) pour spécifier les exigences de mémoire tampon, y compris le nombre de mémoires tampons et la taille de chaque mémoire tampon.
2.  Appelez la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) pour allouer les mémoires tampons.
3.  Appelez la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) pour récupérer des exemples de supports. Cette méthode se bloque jusqu’à ce que l’exemple suivant devienne disponible.
4.  Lorsque vous avez terminé avec chaque exemple, appelez la méthode **IUnknown :: Release** sur l’exemple. L’exemple n’est pas supprimé lorsque son décompte de références atteint zéro. Au lieu de cela, l’exemple retourne à la liste libre de l’allocateur.
5.  Quand vous avez fini d’utiliser l’allocateur, appelez la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) pour libérer de la mémoire pour les mémoires tampons.

La méthode [**Commit**](cbaseallocator-commit.md) appelle la méthode virtuelle [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md), qui alloue la mémoire pour les mémoires tampons. La méthode de [**dévalidation**](cbaseallocator-decommit.md) appelle la méthode virtuelle pure [**CBaseAllocator :: Free**](cbaseallocator-free.md), qui libère la mémoire. Les classes dérivées doivent remplacer ces deux méthodes.

La classe de base [**CMemAllocator**](cmemallocator.md) dérive de **CBaseAllocator**. Les classes de base de filtre utilisent la classe **CMemAllocator** .



| Variables membres protégées                                                   | Description                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**m \_ lFree**](cbaseallocator-m-lfree.md)                                   | Pointeur vers une liste d’exemples de médias disponibles (gratuits).                                       |
| [**m \_ hSem**](cbaseallocator-m-hsem.md)                                     | Sémaphore signalé lorsqu’un exemple devient disponible.                                |
| [**m \_ lWaiting**](cbaseallocator-m-lwaiting.md)                             | Nombre de threads en attente d’exemples.                                                      |
| [**m \_ lCount**](cbaseallocator-m-lcount.md)                                 | Nombre de mémoires tampons à fournir.                                                              |
| [**m \_ lAllocated**](cbaseallocator-m-lallocated.md)                         | Nombre de mémoires tampons actuellement allouées.                                                     |
| [**m \_ lSize**](cbaseallocator-m-lsize.md)                                   | Taille de chaque mémoire tampon.                                                                       |
| [**m \_ lAlignment**](cbaseallocator-m-lalignment.md)                         | Alignement de chaque mémoire tampon.                                                                  |
| [**m \_ lPrefix**](cbaseallocator-m-lprefix.md)                               | Préfixe de chaque mémoire tampon.                                                                     |
| [**m \_ bChanged**](cbaseallocator-m-bchanged.md)                             | Indicateur qui spécifie si les exigences de la mémoire tampon ont été modifiées.                              |
| [**m \_ bCommitted**](cbaseallocator-m-bcommitted.md)                         | Indicateur qui spécifie si l’allocateur a été validé.                                  |
| [**m \_ bDecommitInProgress**](cbaseallocator-m-bdecommitinprogress.md)       | Indicateur spécifiant si une opération de dévalidation est en cours.                               |
| [**m \_ pNotify**](cbaseallocator-m-pnotify.md)                               | Pointeur vers une interface de rappel, qui est appelée lorsque des exemples sont libérés.                |
| [**m \_ fEnableReleaseCallback**](cbaseallocator-m-fenablereleasecallback.md) | Indicateur qui spécifie si le rappel de mise en version est activé.                                   |
| Méthodes protégées                                                            | Description                                                                                |
| [**Utilis**](cbaseallocator-alloc.md)                                        | Alloue de la mémoire pour les mémoires tampons. Virtuels.                                                 |
| M&#233;thodes publiques                                                               | Description                                                                                |
| [**CBaseAllocator**](cbaseallocator-cbaseallocator.md)                      | Méthode de constructeur.                                                                        |
| [**~ CBaseAllocator**](cbaseallocator--cbaseallocator.md)                   | Méthode de destructeur.                                                                         |
| [**SetNotify**](cbaseallocator-setnotify.md)                                | Obsolète.                                                                                  |
| [**GetFreeCount**](cbaseallocator-getfreecount.md)                          | Récupère le nombre d’exemples de supports qui ne sont pas utilisés.                                 |
| [**NotifySample**](cbaseallocator-notifysample.md)                          | Libère tous les threads qui attendent des exemples.                                         |
| [**SetWaiting**](cbaseallocator-setwaiting.md)                              | Incrémente le nombre de threads en attente.                                                   |
| Méthodes virtuelles pures                                                         | Description                                                                                |
| [**Gratuit**](cbaseallocator-free.md)                                          | Libère toute la mémoire tampon.                                                         |
| Méthodes IMemAllocator                                                        | Description                                                                                |
| [**SetProperties**](cbaseallocator-setproperties.md)                        | Spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.                   |
| [**GetProperties**](cbaseallocator-getproperties.md)                        | Récupère le nombre de mémoires tampons créées par l’allocateur, ainsi que les propriétés de la mémoire tampon. |
| [**Commit**](cbaseallocator-commit.md)                                      | Alloue la mémoire pour les mémoires tampons.                                                      |
| [**Annulation**](cbaseallocator-decommit.md)                                  | Annule la validation des tampons.                                                                     |
| [**GetBuffer**](cbaseallocator-getbuffer.md)                                | Récupère un exemple de média qui contient une mémoire tampon.                                           |
| [**ReleaseBuffer**](cbaseallocator-releasebuffer.md)                        | Retourne un échantillon de média à la liste des exemples de médias libres.                                  |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fourniture d’un allocateur personnalisé](providing-a-custom-allocator.md)
</dt> </dl>

 

 




