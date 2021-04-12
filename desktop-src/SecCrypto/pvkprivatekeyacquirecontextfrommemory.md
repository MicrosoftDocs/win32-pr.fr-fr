---
description: Crée un conteneur temporaire dans le fournisseur de services de chiffrement (CSP) et charge une clé privée à partir de la mémoire dans le conteneur.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320370"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>PvkPrivateKeyAcquireContextFromMemory fonction)

> [!IMPORTANT]
> Cette API est déconseillée. Microsoft peut supprimer cette API dans les versions ultérieures.

 

La fonction **PvkPrivateKeyAcquireContextFromMemory** crée un conteneur temporaire dans le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et charge une [*clé privée*](../secgloss/p-gly.md) à partir de la mémoire dans le conteneur.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszProvName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom du fournisseur de services de chiffrement dont le type est demandé dans *dwProvType*.

</dd> <dt>

*dwProvType* \[ dans\]
</dt> <dd>

Valeur **DWORD** pour le type CSP. Pour plus d’informations sur les types CSP, consultez [types de fournisseur de chiffrement](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon destinée à recevoir les données de contexte. L’appelant doit fournir cette ressource.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Valeur **DWORD** qui spécifie la taille, en octets, de la mémoire tampon *pbData* . L’appelant doit fournir cette valeur.

</dd> <dt>

*hwndOwner* \[ dans\]
</dt> <dd>

Si un mot de passe est requis pour déchiffrer les données de contexte pointées par le paramètre *pbData* , ce paramètre est un handle vers le parent de la boîte de dialogue ; dans le cas contraire, la **valeur est null**.

</dd> <dt>

*pwszKeyName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de la clé à récupérer.

</dd> <dt>

*pdwKeySpec* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui spécifie le type de clé. Les valeurs possibles sont notamment **at \_ KeyExchange** ou **at \_ signature**.

</dd> <dt>

*phCryptProv* \[ à\]
</dt> <dd>

Pointeur vers un handle pour le CSP.

</dd> <dt>

*ppwszTmpContainer* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers une chaîne se terminant par null pour le nom de conteneur temporaire. La fonction **PvkPrivateKeyAcquireContextFromMemory** fournit la mémoire tampon pour cette chaîne et l’initialise. Lors de l’appel de **PvkPrivateKeyAcquireContextFromMemory**, l’adresse doit pointer vers une valeur **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne **true**. La fonction **PvkPrivateKeyAcquireContextFromMemory** retourne la **valeur false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
