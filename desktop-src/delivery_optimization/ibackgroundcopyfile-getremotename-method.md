---
title: Méthode IBackgroundCopyFile GetRemoteName (Deliveryoptimization. h)
description: Récupère le nom distant du fichier.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Méthode GetRemoteName
- Méthode GetRemoteName, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, méthode GetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810330"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>IBackgroundCopyFile :: GetRemoteName, méthode

Récupère le nom distant du fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppName* \[ à\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom distant du fichier à transférer. Le nom est complet. Appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer *ppName* quand vous avez terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.

## <a name="remarks"></a>Remarques

Pour modifier le nom du fichier distant, appelez la méthode [**IBackgroundCopyFile2 :: SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

