---
description: La classe CCritSec fournit un verrou de thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: CCritSec, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537453"
---
# <a name="ccritsec-class"></a>CCritSec, classe

La classe **CCritSec** fournit un verrou de thread.

Cette classe est un wrapper léger pour un objet **de \_ section critique** Windows. Vous pouvez verrouiller et déverrouiller le thread en appelant les méthodes [**CCritSec :: Lock**](ccritsec-lock.md) et [**CCritSec :: Unlock**](ccritsec-unlock.md) . Toutefois, il est plus sûr d’utiliser cette classe conjointement avec la classe [**CAutoLock**](cautolock.md) . Lorsque la classe **CAutoLock** devient hors de portée, elle déverrouille automatiquement l’objet **CCritSec** . En outre, il est compilé en code inline efficace.



| Variables membres publiques                            | Description                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentOwner**](ccritsec-m-currentowner.md) | Identificateur de thread du thread propriétaire.                  |
| [**m \_ lockCount**](ccritsec-m-lockcount.md)       | Nombre de verrous en attente sur cet objet.              |
| [**m \_ fTrace**](ccritsec-m-ftrace.md)             | Valeur booléenne qui spécifie s’il faut tracer ce verrou. |
| M&#233;thodes publiques                                     | Description                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Méthode de constructeur.                                      |
| [**~ CCritSec**](ccritsec--ccritsec.md)            | Méthode de destructeur.                                       |
| [**Lock**](ccritsec-lock.md)                      | Verrouille l’objet de section critique.                       |
| [**Bloquer**](ccritsec-unlock.md)                  | Déverrouille l’objet de section critique.                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de section critique](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[Référence de classe de base DirectShow](base-class-reference.md)
</dt> </dl>

 

