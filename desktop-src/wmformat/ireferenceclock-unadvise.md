---
title: IReferenceClock méthode Unadvise
description: La méthode Unadvise annule une demande de notification.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Méthode Unadvise Windows Media format
- Méthode Unadvise Windows Media format, interface IReferenceClock
- Interface IReferenceClock Windows Media format, Unadvise, méthode
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104101008"
---
# <a name="ireferenceclockunadvise-method"></a>IReferenceClock :: Unadvise, méthode

La méthode **Unadvise** annule une demande de notification.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificateur de la demande à supprimer. Utilisez la valeur retournée par AdviseTime dans le paramètre pdwAdviseCookie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                             | Description                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | S_OK<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | L’identificateur passé n’existe pas.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





