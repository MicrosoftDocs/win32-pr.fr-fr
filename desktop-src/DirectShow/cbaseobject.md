---
description: La classe CBaseObject est une classe abstraite pour l’implémentation d’objets DirectShow. Pour implémenter des objets COM (Component Object Model), utilisez la classe CUnknown, qui dérive de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: CBaseObject, classe (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532812"
---
# <a name="cbaseobject-class"></a>CBaseObject, classe

La classe **CBaseObject** est une classe abstraite pour l’implémentation d’objets DirectShow. Pour implémenter des objets COM (Component Object Model), utilisez la classe [**CUnknown**](cunknown.md) , qui dérive de **CBaseObject**.



| Méthodes de classe                                      | Description                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Méthode de constructeur.                    |
| [**~ CBaseObject**](cbaseobject--cbaseobject.md)   | Méthode de destructeur.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Récupère le nombre d’objets actifs. |



 

## <a name="remarks"></a>Notes

La plupart des classes de base DirectShow dérivent de **CBaseObject**. Cette classe fournit une assistance en matière de débogage en conservant le décompte de tous les objets DirectShow actifs au moment de l’exécution. Le nombre d’objets est stocké dans une variable membre statique de classe :


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



Dans les versions Debug, la DLL déclarera si elle est déchargée alors que le nombre d’objets est supérieur à zéro. Cela facilite le suivi des fuites provoquées par des problèmes de comptage des références.

Le constructeur **CBaseObject** prend un argument, un nom de débogage pour l’objet. Ce nom est stocké dans une table globale de la DLL. La fonction [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) met en forme une liste des objets actifs dans la dll et l’envoie à la sortie de débogage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




