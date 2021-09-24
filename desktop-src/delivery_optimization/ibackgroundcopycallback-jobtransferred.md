---
title: Méthode IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: L’optimisation de la distribution appelle votre implémentation de la méthode JobTransferred lorsque tous les fichiers du travail ont été transférés avec succès.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Méthode JobTransferred
- Méthode JobTransferred, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, méthode JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5af8b1f6c9448da7141c041c52bd8ae3620f1360
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521236"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>IBackgroundCopyCallback :: JobTransferred, méthode

L’optimisation de la distribution appelle votre implémentation de la méthode **JobTransferred** lorsque tous les fichiers du travail ont été transférés avec succès.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJob* \[ dans\]
</dt> <dd>

Contient des informations relatives au travail, telles que l’heure de fin du travail, le nombre d’octets transférés et le nombre de fichiers transférés. Ne libérez pas *pJob*; L’optimisation de la distribution libère l’interface lorsque la méthode est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode doit retourner S_OK.

## <a name="remarks"></a>Remarques

En général, votre implémentation doit appeler la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour confirmer que l’optimisation de la remise a réussi à transférer les fichiers. Les fichiers téléchargés et le fichier de réponse ne sont pas disponibles sur le client tant que vous n’avez pas appelé la méthode **Complete** .

Si vous n’appelez pas la méthode [**Complete**](ibackgroundcopyjob-complete.md) ou si l’optimisation de la livraison de la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) annule le travail au bout de 30 jours et supprime les fichiers incomplets.

## <a name="requirements"></a>Configuration requise



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
</dt> <dt>

[**Méthode ibackgroundcopyjob :: complet**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





