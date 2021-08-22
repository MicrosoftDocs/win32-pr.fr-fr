---
description: Convertit un chemin d’accès Microsoft MS-DOS en URL canonique.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: f9da3dd84d54bb514b7dda519db3de376b2ebb2bd2088d8fc8e18b4f2b848231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739247"
---
# <a name="mfcreateurlfrompath-function"></a>MFCreateURLFromPath fonction)

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Au lieu de cela, les applications doivent appeler [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]

Convertit un chemin d’accès Microsoft MS-DOS en URL canonique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszFilePath* \[ dans, facultatif\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le chemin d’accès. La longueur maximale de la chaîne est la longueur de l' **\_ \_ URL \_ maximale Internet**.

</dd> <dt>

*ppwszFileURL* \[ à\]
</dt> <dd>

Reçoit une chaîne terminée par le caractère null qui contient l’URL. L’appelant doit libérer la chaîne en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                             | Description                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La chaîne spécifiée dans le paramètre *pwszFilePath* est déjà au format URL. Dans ce cas, *pszFilePath* est simplement copié sur *ppszFileURL* sans modification.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | La fonction a réussi. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mfplat.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
