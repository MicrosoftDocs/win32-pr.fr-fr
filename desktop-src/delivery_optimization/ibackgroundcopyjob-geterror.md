---
title: Méthode méthode ibackgroundcopyjob GetError (Deliveryoptimization. h)
description: Récupère l’interface d’erreur après qu’une erreur s’est produite.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Méthode GetError
- Méthode GetError, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 016f11023d50d7ea1fa9024e270a7ebce0597e07d5c33a915facae47773759c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755509"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Méthode ibackgroundcopyjob :: GetError, méthode

Récupère l’interface d’erreur après qu’une erreur s’est produite.

L’optimisation de la remise (DO) génère un objet d’erreur lorsque l’état du travail est BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR. Le service ne crée pas d’objet d’erreur lorsqu’un appel à une méthode d’interface **IBackgroundCopyXXXX** échoue. L’objet d’erreur est disponible jusqu’à ce que commence à transférer les données (l’état du travail passe à BG_JOB_STATE_TRANSFERRING) pour le travail ou jusqu’à ce que votre application se ferme.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppError* \[ à\]
</dt> <dd>

Interface d’erreur qui fournit le code d’erreur, une description de l’erreur et le contexte dans lequel l’erreur s’est produite. Ce paramètre identifie également le fichier transféré au moment où l’erreur s’est produite. Libérez *ppError* quand vous avez terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                                           | Description                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>                              | L’objet d’erreur a été généré.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | L’interface d’erreur n’est disponible qu’après qu’une erreur s’est produite (BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR) et avant que ne commence à transférer les données (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Remarques

Le travail est placé dans un état d’erreur en cas d’erreurs irrécupérables. Utilisez l’une des options suivantes pour déterminer si le travail est en erreur :

-   Pour interroger l’état de la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md) . Le travail est erroné si l’État est BG_JOB_STATE_ERROR.
-   Pour recevoir une notification lorsqu’une erreur se produit, implémentez l’interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (plus précisément, la méthode [**JobError**](https://www.bing.com/search?q=**JobError**) ). Ensuite, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) pour inscrire le rappel et la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) pour définir l’indicateur de BG_NOTIFY_JOB_ERROR.

L’interface [**IBackgroundCopyError**](ibackgroundcopyerror.md) contient des informations que vous utilisez pour déterminer la cause de l’erreur et si le processus de transfert peut se poursuivre. Après avoir déterminé la cause de l’erreur, effectuez l’une des options suivantes :

-   Pour annuler la tâche, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Pour enregistrer les fichiers qui ont été transférés avec succès avant que l’erreur ne se produise, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) .
-   Pour terminer le traitement du travail, corrigez le problème, puis appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





