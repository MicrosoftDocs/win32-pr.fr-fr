---
description: La classe CAutoLock contient une section critique pour l’étendue d’un bloc de code.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: CAutoLock, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296867"
---
# <a name="cautolock-class"></a>CAutoLock, classe

La `CAutoLock` classe contient une section critique pour la portée d’un bloc de code.

Cette classe fonctionne conjointement avec la classe [**CCritSec**](ccritsec.md) , qui est un wrapper pour les objets de section critiques. Le `CAutoLock` constructeur verrouille la section critique et le destructeur le déverrouille. En utilisant un `CAutoLock` objet en tant que variable locale, vous pouvez verrouiller une section critique avec la garantie que tous les chemins de code déverrouilleront la section critique.

L’exemple de code suivant montre comment utiliser cette classe :


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



Les méthodes de cette classe ne sont pas conçues pour être substituées.



| Variables membres protégées                 | Description                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [**m \_ pLock**](cautolock-m-plock.md)      | Section critique pour ce verrou.                                  |
| M&#233;thodes publiques                             | Description                                                      |
| [**CAutoLock**](cautolock-cautolock.md)   | Méthode de constructeur. Verrouille l’objet de section critique spécifié. |
| [**~ CAutoLock**](cautolock--cautolock.md) | Méthode de destructeur. Déverrouille l’objet de section critique.          |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




