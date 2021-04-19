---
description: Installe un fichier catalogue.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526782"
---
# <a name="psetupinstallcatalog-function"></a>pSetupInstallCatalog fonction)

\[Cette fonction n’est plus prise en charge par Microsoft. Les développeurs doivent utiliser **CryptCATAdminAddCatalog**.\]

Installe un fichier catalogue.

## <a name="syntax"></a>Syntaxe


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CatalogFullPath* \[ dans\]
</dt> <dd>

Chemin d’accès complet du catalogue à installer sur le système.

</dd> <dt>

*NewBaseName* \[ dans\]
</dt> <dd>

Nouveau nom de base à utiliser lorsque le fichier catalogue est copié dans le magasin de catalogues.

</dd> <dt>

*NewCatalogFullPath* \[ out, facultatif\]
</dt> <dd>

Reçoit éventuellement le chemin d’accès complet du fichier de catalogue dans le magasin de catalogues. Cette mémoire tampon doit être au moins d’octets de **\_ chemin d’accès** (version ANSI) ou de caractères (version Unicode).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle **ne retourne aucune \_ erreur**; sinon, elle retourne un code d’erreur Win32 qui indique la cause de l’échec.

## <a name="remarks"></a>Notes

Le fichier est copié par le système dans un répertoire spécial et est éventuellement renommé.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CryptCATAdminAddCatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
