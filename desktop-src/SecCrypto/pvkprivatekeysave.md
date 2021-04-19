---
description: Enregistre une clé privée et la clé publique correspondante dans un fichier spécifié.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523315"
---
# <a name="pvkprivatekeysave-function"></a>PvkPrivateKeySave fonction)

> [!IMPORTANT]
> Cette API est déconseillée. Microsoft peut supprimer cette API dans les versions ultérieures.

 

La fonction **PvkPrivateKeySave** enregistre une [*clé privée*](../secgloss/p-gly.md) et la [*clé publique*](../secgloss/p-gly.md) correspondante dans un fichier spécifié.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCryptProv* \[ dans\]
</dt> <dd>

Handle d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ dans\]
</dt> <dd>

Handle vers un fichier créé avec l’autorisation de lecture/écriture initiale et l’autorisation en lecture seule ultérieure.

</dd> <dt>

*dwKeySpec* \[ dans\]
</dt> <dd>

Entier long pour le type de clé. Les valeurs possibles sont notamment **at \_ KeyExchange** ou **at \_ signature**.

</dd> <dt>

*hwndOwner* \[ dans\]
</dt> <dd>

Si un mot de passe est requis pour chiffrer la clé privée, ce paramètre est un handle vers le parent de la boîte de dialogue ; dans le cas contraire, la **valeur est null**.

</dd> <dt>

*pwszKeyName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null pour le nom de la clé à enregistrer.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur **DWORD** qui spécifie des options supplémentaires pour la fonction. Pour plus d’informations, consultez le paramètre *dwFlags* dans [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne **true**. La fonction **PvkPrivateKeySave** retourne la **valeur false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
