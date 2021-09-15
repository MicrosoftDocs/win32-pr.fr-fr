---
description: Convertit une URL de fichier en un chemin d’accès Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531749"
---
# <a name="mfcreatepathfromurl-function"></a>MFCreatePathFromURL fonction)

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Au lieu de cela, les applications doivent appeler [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]

Convertit une URL de fichier en un chemin d’accès Microsoft MS-DOS.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszFileURL* \[ dans, facultatif\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient l’URL. La longueur maximale de la chaîne est la longueur de l' **\_ \_ URL \_ maximale Internet**.

</dd> <dt>

*ppwszFilePath* \[ à\]
</dt> <dd>

Reçoit une chaîne terminée par le caractère null qui contient l’URL. L’appelant doit libérer la chaîne en appelant [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La fonction retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                  | Description                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi. <br/>                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide. La chaîne spécifiée dans le paramètre *pwszFileURL* ne peut pas être convertie en chemin d’accès.<br/> |



 

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mfplat.dll.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
