---
title: Méthode IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: L’optimisation de la remise (DO) appelle votre implémentation de la méthode JobError lorsque l’état du travail passe à BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Méthode JobError
- Méthode JobError, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, méthode JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384516"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>IBackgroundCopyCallback :: JobError, méthode

L’optimisation de la remise (DO) appelle votre implémentation de la méthode [**JobError**](https://www.bing.com/search?q=**JobError**) lorsque l’état du travail passe à BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pJob* \[ dans\]
</dt> <dd>

Contient des informations relatives au travail, telles que le nombre d’octets et de fichiers transférés avant l’erreur. Elle contient également les méthodes de reprise et d’annulation du travail. Ne libérez pas *pJob*; Libère l’interface lorsque la méthode [**JOBERROR**](https://www.bing.com/search?q=**JobError**) est retournée.

</dd> <dt>

*perror* \[ dans\]
</dt> <dd>

Contient des informations sur l’erreur, telles que le fichier en cours de traitement au moment où l’erreur irrécupérable s’est produite et une description de l’erreur. Ne libérez pas *perror*; Libère l’interface lorsque la méthode [**JOBERROR**](https://www.bing.com/search?q=**JobError**) est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode doit retourner **S_OK**; dans le cas contraire, continue à appeler cette méthode jusqu’à ce que **S_OK** soit retourné. Pour des raisons de performances, vous devez limiter le nombre de fois où vous retournez une valeur autre que **S_OK** à plusieurs fois. Au lieu de retourner un code d’erreur, envisagez de retourner toujours **S_OK** et de gérer l’erreur en interne. L’intervalle auquel cette méthode est appelée est arbitraire.

## <a name="remarks"></a>Notes

Après avoir déterminé la cause de l’erreur, effectuez l’une des options suivantes :

-   Pour annuler la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Pour accepter la partie du travail qui a été transférée correctement avant que l’erreur ne s’est produite, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) . Cette option ne s’applique pas aux travaux de chargement ; vous ne pouvez pas effectuer une partie d’une tâche de téléchargement.
-   Pour terminer le traitement du travail, corrigez le problème, puis appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) .

Les erreurs temporaires ne génèrent pas d’appels à la méthode [**JobError**](https://www.bing.com/search?q=**JobError**) .

Retourne BG_ERROR_CONTEXT_REMOTE_FILE si la tâche atteint une erreur HTTP 403, BG_ERROR_CONTEXT_NONE dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback est défini en tant que 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





