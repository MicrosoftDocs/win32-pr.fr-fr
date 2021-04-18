---
description: Obtient un objet énumérateur qui peut être utilisé à son tour pour énumérer les fournisseurs de stockage protégés qui sont actuellement installés sur le système.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Fonction PStoreEnumProviders (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540599"
---
# <a name="pstoreenumproviders-function"></a>PStoreEnumProviders fonction)

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtient un objet énumérateur qui peut être utilisé à son tour pour énumérer les fournisseurs de stockage protégés qui sont actuellement installés sur le système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*ppenum* 
</dt> <dd>

Pointeur vers un pointeur vers une interface [**IEnumPStoreProviders**](ienumpstoreproviders.md) qui peut être utilisée pour énumérer les fournisseurs installés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne un **HRESULT**.

## <a name="remarks"></a>Notes

Le composant de stockage protégé a une architecture basée sur un fournisseur. Les applications qui utilisent le stockage protégé peuvent spécifier les fournisseurs installés à utiliser lors du stockage et de la récupération de leurs données.

La fonction **PStoreEnumProviders** est utilisée pour énumérer les fournisseurs de stockage protégés installés. Chaque fournisseur est identifié par un identificateur global unique (GUID).

Jusqu’à présent, un seul fournisseur de stockage protégé a jamais été écrit. Étant donné que le service de stockage protégé est actuellement déconseillé, il est peu probable que des fournisseurs supplémentaires soient générés. Par conséquent, cette fonction ne doit pas être utilisée à quelque fin que ce soit.

Cette fonction n’a pas de bibliothèque d’importation associée ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
