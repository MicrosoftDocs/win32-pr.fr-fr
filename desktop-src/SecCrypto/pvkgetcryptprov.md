---
description: Obtient un handle vers un fournisseur de services de chiffrement (CSP) basé sur un fichier de clé privée ou un nom de conteneur de clé.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869001"
---
# <a name="pvkgetcryptprov-function"></a>PvkGetCryptProv fonction)

> [!IMPORTANT]
> Cette API est déconseillée. Microsoft peut supprimer cette API dans les versions ultérieures.

 

La fonction **PvkGetCryptProv** obtient un descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) basé sur un fichier de [*clé privée*](../secgloss/p-gly.md) ou un nom de conteneur de clé.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Si un mot de passe est requis pour déchiffrer le fichier de clé privée, ce paramètre est un handle vers le parent de la boîte de dialogue de mot de passe. dans le cas contraire, la **valeur est null**.

</dd> <dt>

*pwszCaption* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par null pour la légende de la boîte de dialogue.

</dd> <dt>

*pwszCapiProvider* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par null pour le nom du fournisseur de services de chiffrement.

</dd> <dt>

*dwProviderType* \[ dans\]
</dt> <dd>

Valeur **DWORD** qui représente le type de fournisseur de services de chiffrement. Pour plus d’informations, consultez [types de fournisseur de services de chiffrement](cryptographic-provider-types.md).

</dd> <dt>

*pwszPvkFile* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom d’un fichier de clé privée.

</dd> <dt>

*pwszKeyContainerName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null pour le nom du conteneur de clé privée.

</dd> <dt>

*pdwKeySpec* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** pour le type de clé du conteneur retourné avec *phCryptProv* et *ppwszTmpContainer*.

</dd> <dt>

*ppwszTmpContainer* \[ out, facultatif\]
</dt> <dd>

Adresse d’un pointeur vers une chaîne se terminant par un caractère null pour le nom de conteneur de clé temporaire. La fonction **PvkGetCryptProv** fournit et initialise le conteneur temporaire. Lors de l’appel de **PvkGetCryptProv**, l’adresse doit pointer vers une valeur **null** .

</dd> <dt>

*phCryptProv* \[ à\]
</dt> <dd>

Pointeur vers un handle pour le CSP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur **\_ OK**.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Notes

La fonction **PvkGetCryptProv** tente d’abord d’accéder au handle du fournisseur à partir du nom du conteneur de clé spécifié par le paramètre *pwszKeyContainerName* . Si vous transmettez la **valeur null** pour le paramètre *pwszKeyContainerName* , **PvkGetCryptProv** tente d’obtenir le fournisseur à partir du fichier de clé privée spécifié dans le paramètre *pwszPvkFile* .

Lorsque vous avez terminé d’utiliser le CSP, libérez le handle du fournisseur et le conteneur de clé temporaire en appelant la fonction [**PvkFreeCryptProv**](pvkfreecryptprov.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
