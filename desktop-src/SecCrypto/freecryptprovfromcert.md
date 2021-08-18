---
description: Libère le descripteur d’un fournisseur de services de chiffrement (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8797a6f48bcfb973a6c07a4b05ae0d39bc3b4522ab6f7ae70a80eaa77081da44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006787"
---
# <a name="freecryptprovfromcert-function"></a>FreeCryptProvFromCert fonction)

> [!IMPORTANT]
> Cette API est déconseillée. Microsoft peut supprimer cette API dans les versions ultérieures.

 

La fonction **FreeCryptProvFromCert** libère le descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction [**GetCryptProvFromCert**](getcryptprovfromcert.md) .

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fAcquired* \[ dans\]
</dt> <dd>

Valeur qui spécifie si le handle du fournisseur a été acquis à partir du [*certificat*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**HCRYPTPROV**](hcryptprov.md) pour le fournisseur de services de chiffrement.

</dd> <dt>

*pwszCapiProvider* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null pour le nom du fournisseur.

</dd> <dt>

*dwProviderType* \[ dans\]
</dt> <dd>

Spécifie le type de fournisseur de services de chiffrement. Il peut s’agir de zéro ou de l’un des [types de fournisseur de chiffrement](cryptographic-provider-types.md). Si ce membre est égal à zéro, le conteneur de clé est l’un des fournisseurs de stockage de clés CNG.

</dd> <dt>

*pwszTmpContainer* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null pour le nom du conteneur de clé temporaire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
