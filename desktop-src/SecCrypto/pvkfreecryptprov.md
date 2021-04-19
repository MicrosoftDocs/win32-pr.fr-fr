---
description: Libère le descripteur d’un fournisseur de services de chiffrement (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530224"
---
# <a name="pvkfreecryptprov-function"></a>PvkFreeCryptProv fonction)

> [!IMPORTANT]
> Cette API est déconseillée. Microsoft peut supprimer cette API dans les versions ultérieures.

 

La fonction **PvkFreeCryptProv** libère le descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et supprime éventuellement le conteneur temporaire créé par la fonction [**PvkGetCryptProv**](pvkgetcryptprov.md) .

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProv* \[ dans\]
</dt> <dd>

Handle du fournisseur de services de chiffrement.

</dd> <dt>

*pwszCapiProvider* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par null pour le nom du fournisseur de services de chiffrement.

</dd> <dt>

*dwProviderType* \[ dans\]
</dt> <dd>

Valeur **DWORD** qui représente le type de fournisseur de services de chiffrement. Pour plus d’informations, consultez [types de fournisseur de services de chiffrement](cryptographic-provider-types.md).

</dd> <dt>

*pwszTmpContainer* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par null pour le nom de conteneur de clé temporaire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
