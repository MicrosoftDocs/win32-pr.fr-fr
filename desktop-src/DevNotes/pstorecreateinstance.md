---
description: Récupère un pointeur d’interface vers un fournisseur de stockage.
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: Fonction PStoreCreateInstance (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955688"
---
# <a name="pstorecreateinstance-function"></a>PStoreCreateInstance fonction)

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Cette fonction peut être modifiée ou indisponible dans les futures versions de Windows. Utilisez les fonctions **CryptProtectData** et **CryptUnprotectData** au lieu de cette fonction.\]

Récupère un pointeur d’interface vers un fournisseur de stockage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppProvider* \[ à\]
</dt> <dd>

Pointeur vers le pointeur d’interface récupéré pour le fournisseur de stockage. Lorsque vous avez fini d’utiliser l’interface, décrémente son décompte de références en appelant sa méthode [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Ce paramètre ne peut pas être **null**.

</dd> <dt>

*pProviderID* \[ dans\]
</dt> <dd>

Pointeur vers le **GUID** qui identifie le fournisseur de stockage. Si ce paramètre a la **valeur null**, le fournisseur de stockage de base est utilisé.

</dd> <dt>

*conservé* \[ dans\]
</dt> <dd>

Réservé doit avoir la **valeur null**.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur **S \_ OK** indique que la fonction a réussi.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation associée ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
