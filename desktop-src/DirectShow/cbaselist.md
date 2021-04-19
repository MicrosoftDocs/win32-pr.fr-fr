---
description: La méthode CBaseList implémente une liste ABTRACT. Le modèle de classe CGenericList, qui dérive de CBaseList, fournit la vérification de type et une interface plus simple que la classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: CBaseList, classe (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539583"
---
# <a name="cbaselist-class"></a>CBaseList, classe

![hiérarchie de la classe cbaselist](images/list01.png)

La méthode **CBaseList** implémente une liste ABTRACT. Le modèle de classe [**CGenericList**](cgenericlist.md) , qui dérive de **CBaseList**, fournit la vérification de type et une interface plus simple que la classe **CBaseList** .

La classe **CBaseList** est modélisée après la classe **CObList** dans la bibliothèque Microsoft Foundation classes (MFC). Les positions dans la liste sont représentées par une structure de POSITION. L’appelant ne doit pas accéder aux membres internes de la structure de POSITION ; le traiter en tant que pointeur vers un nœud de liste. La position d’un objet dans la liste reste valide jusqu’à ce que l’objet soit supprimé.

La liste ne nécessite aucune prise en charge par les objets qu’elle contient. Il n’effectue aucune gestion du stockage ou copie sur les objets. Les objets peuvent figurer dans plusieurs listes.

Environ la moitié des méthodes de cette classe agissent sur des objets uniques. Ces méthodes ont le suffixe-I dans le nom de la méthode. Les autres méthodes agissent sur des listes entières. Par exemple, la méthode [**CBaseList :: AddAfter**](cbaselist-addafter.md) ajoute une liste à une autre liste. Les opérations à objet unique retournent des valeurs de POSITION, ou **null** en cas d’échec. Les opérations de liste retournent **true** en cas de réussite ou **false** dans le cas contraire.



| Variables membres protégées                             | Description                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_nombre m**](cbaselist-m-count.md)                  | Nombre d’éléments dans la liste.                                              |
| [**m \_ pFirst**](cbaselist-m-pfirst.md)                | Pointeur vers le premier nœud de la liste.                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | Pointeur vers le dernier nœud de la liste.                                     |
| Méthodes protégées                                      | Description                                                               |
| [**GetNextI**](cbaselist-getnexti.md)                 | Récupère l’élément à la position spécifiée et avance la position.  |
| [**GetI**](cbaselist-geti.md)                         | Récupère l’élément à la position spécifiée.                             |
| [**Rechercher**](cbaselist-findi.md)                       | Récupère la première position qui contient l’élément spécifié.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Supprime le premier élément de la liste.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Supprime le dernier élément de la liste.                                        |
| [**Supprimeri**](cbaselist-removei.md)                   | Supprime l'élément à la position spécifiée.                               |
| [**AddTailI**](cbaselist-addtaili.md)                 | Ajoute un élément à la fin de la liste.                                      |
| [**AddHeadI**](cbaselist-addheadi.md)                 | Ajoute un élément au début de la liste.                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | Insère un élément après la position spécifiée.                             |
| [**AddBeforeI**](cbaselist-addbeforei.md)             | Insère un élément avant la position spécifiée.                            |
| M&#233;thodes publiques                                         | Description                                                               |
| [**CBaseList**](cbaselist-cbaselist.md)               | Méthode de constructeur.                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | Méthode de destructeur.                                                        |
| [**RemoveAll**](cbaselist-removeall.md)               | Supprime tous les nœuds de la liste.                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | Récupère la position du premier élément de la liste.                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | Récupère la position du dernier élément de la liste.                      |
| [**GetCountI**](cbaselist-getcounti.md)               | Récupère le nombre d’éléments dans la liste.                                |
| [**Suivant**](cbaselist-next.md)                         | Récupère la position suivante dans la liste.                                  |
| [**PREV**](cbaselist-prev.md)                         | Récupère la position précédente dans la liste.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Insère une autre liste au début de cette liste.                           |
| [**AddTail**](cbaselist-addtail.md)                   | Ajoute une autre liste à la fin de cette liste.                             |
| [**AddAfter**](cbaselist-addafter.md)                 | Insère une liste après la position spécifiée.                              |
| [**AddBefore**](cbaselist-addbefore.md)               | Insère une liste avant la position spécifiée.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Fractionne la liste et ajoute la partie d’en-tête à la fin d’une autre liste. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Divise la liste et insère la partie de la fin à l’en-tête d’une autre liste. |
| [**TVA**](cbaselist-reverse.md)                   | Inverse l’ordre de la liste.                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




