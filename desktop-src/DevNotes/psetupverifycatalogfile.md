---
description: Vérifie un fichier catalogue unique à l’aide de la stratégie de signature de code du système d’exploitation standard, telle que la signature du pilote.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: pSetupVerifyCatalogFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528016"
---
# <a name="psetupverifycatalogfile-function"></a>pSetupVerifyCatalogFile fonction)

\[Cette fonction n’est plus prise en charge par Microsoft. Pour un fichier INF (installation d’appareils), les développeurs doivent utiliser **SetupVerifyInfFile**. Pour valider un catalogue non-INF, utilisez **WinVerifyTrust**.\]

Vérifie un fichier catalogue unique à l’aide de la stratégie de signature de code du système d’exploitation standard, telle que la signature du pilote.

## <a name="syntax"></a>Syntaxe


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CatalogFullPath* \[ dans\]
</dt> <dd>

Chemin d’accès qualifié complet du fichier catalogue à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne l' **erreur \_ réussite**; sinon, elle retourne l’erreur de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SetupVerifyInfFile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
