---
title: Méthode IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: L’optimisation de la remise (DO) appelle votre implémentation de la méthode JobModification lorsque le travail a été modifié.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Méthode JobModification
- Méthode JobModification, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, méthode JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517617"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>IBackgroundCopyCallback :: JobModification, méthode

L’optimisation de la remise (DO) appelle votre implémentation de la méthode [**JobModification**](https://www.bing.com/search?q=**JobModification**) lorsque le travail a été modifié. Le service génère cet événement lorsque les octets sont transférés, que des fichiers ont été ajoutés au travail, que des propriétés ont été modifiées ou que l’état de la tâche a changé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJob* \[ dans\]
</dt> <dd>

Contient les méthodes permettant d’accéder à la propriété, à la progression et aux informations d’État du travail. Ne libérez pas *pJob*; Libère l’interface lorsque la méthode [**JOBMODIFICATION**](https://www.bing.com/search?q=**JobModification**) est retournée.

</dd> <dt>

*dwReserved* \[ dans\]
</dt> <dd>

Réservé pour un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode doit retourner S_OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





