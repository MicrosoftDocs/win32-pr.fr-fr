---
description: Définit les informations de paramètre spécifiées.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'IPStore :: SetProvParam, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9ec106cd4558ddab7fd8bc430088f1bd7d721d7122f77166dfe0da7de35f1787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749719"
---
# <a name="ipstoresetprovparam-method"></a>IPStore :: SetProvParam, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Définit les informations de paramètre spécifiées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwParam* \[ dans\]
</dt> <dd>

Contient un **fichier PST \_ pp \_ flush \_ PW \_ cache** pour vider le cache des mots de passe utilisateur.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Longueur du mot de passe dans la mémoire tampon.

</dd> <dt>

*pbData* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient le mot de passe de l’utilisateur. La valeur doit être **null**.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Réservé : doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **HRESULT** . La valeur **PST \_ E \_ OK** indique que la fonction a réussi.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
