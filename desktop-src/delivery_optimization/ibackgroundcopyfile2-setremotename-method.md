---
title: Méthode IBackgroundCopyFile2 SetRemoteName (Deliveryoptimization. h)
description: Remplace le nom distant par une nouvelle URL dans un travail de téléchargement.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Méthode SetRemoteName
- Méthode SetRemoteName, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, méthode SetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921756"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>IBackgroundCopyFile2 :: SetRemoteName, méthode

Remplace le nom distant par une nouvelle URL dans un travail de téléchargement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom_distant* \[ dans\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom du fichier sur le serveur. Pour plus d’informations sur la spécification du nom distant, consultez le membre **nom_distant** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.



| Code de retour                                                                                  | Description                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>     | Succès<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Le nouveau nom distant est une URL non valide ou la nouvelle URL est trop longue (l’URL ne peut pas dépasser 2 200 caractères).<br/> |



 

## <a name="remarks"></a>Notes

En général, vous appelez cette méthode si vous souhaitez modifier l’URL utilisée pour transférer le fichier ou si vous souhaitez modifier le nom ou le chemin d’accès du fichier.

Cette méthode ne sérialise pas quand elle retourne. Pour sérialiser la modification, [**interrompez**](ibackgroundcopyjob-suspend.md) la tâche, appelez cette méthode (si vous modifiez plusieurs fichiers du travail, utilisez une boucle) et [**reprenez**](ibackgroundcopyjob-resume.md) la tâche. L’appel de la méthode **méthode ibackgroundcopyjob :: Resume** sérialise la modification.

Si l’horodatage ou la taille de fichier du nouveau nom distant est différent du nom distant précédent ou si le nouveau serveur ne prend pas en charge la reprise de point de contrôle (pour les noms distants HTTP), redémarre le téléchargement. Dans le cas contraire, le transfert reprend à partir de la même position sur le nouveau serveur. Ne redémarrez pas les fichiers déjà transférés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 est défini en tant que 83e81b93-0873-474d-8A8C-f2018b1a939c<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





