---
description: Obtient un handle vers un fournisseur de services de chiffrement (CSP) et une spécification de clé pour un contexte de certificat.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321026"
---
# <a name="getcryptprovfromcert-function"></a>GetCryptProvFromCert fonction)

> [!IMPORTANT]
> Cette API est déconseillée. Microsoft peut supprimer cette API dans les versions ultérieures.

 

La fonction **GetCryptProvFromCert** obtient un descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et une spécification de clé pour un contexte de [*certificat*](../secgloss/c-gly.md) . Utilisez cette fonction pour accéder à la [*clé privée*](../secgloss/p-gly.md) de l’émetteur du certificat.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre à utiliser comme propriétaire de toutes les boîtes de dialogue affichées. Ce membre n’est pas actuellement utilisé et est ignoré. Il est possible de passer la **valeur null** pour ce paramètre en toute sécurité.

</dd> <dt>

*pCert* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificat pour le certificat.

</dd> <dt>

*phCryptProv* \[ à\]
</dt> <dd>

Pointeur vers une structure [**HCRYPTPROV**](hcryptprov.md) qui est un handle pour le fournisseur de services de chiffrement.

</dd> <dt>

*pdwKeySpec* \[ à\]
</dt> <dd>

Spécification de la clé privée à récupérer. Les valeurs possibles sont notamment **at \_ KeyExchange** ou **at \_ signature**.

</dd> <dt>

*pfDidCryptAcquire* \[ dans\]
</dt> <dd>

Valeur qui spécifie si la fonction A acquis le handle de fournisseur en fonction du certificat.

</dd> <dt>

*ppwszTmpContainer* \[ out, facultatif\]
</dt> <dd>

Adresse d’un pointeur vers une chaîne se terminant par un caractère null pour le nom de conteneur de clé temporaire. La fonction **GetCryptProvFromCert** fournit et initialise le conteneur temporaire. Lors de l’appel de **GetCryptProvFromCert**, l’adresse doit pointer vers une valeur **null** .

</dd> <dt>

*ppwszProviderName* \[ out, facultatif\]
</dt> <dd>

Adresse d’un pointeur vers une chaîne terminée par le caractère null pour le nom du fournisseur. La fonction **GetCryptProvFromCert** retourne le nom du fournisseur. Lors de l’appel de **GetCryptProvFromCert**, l’adresse doit pointer vers une valeur **null** .

</dd> <dt>

*pdwProviderType* \[ à\]
</dt> <dd>

Spécifie le type de fournisseur de services de chiffrement. Il peut s’agir de zéro ou de l’un des [types de fournisseur de chiffrement](cryptographic-provider-types.md). Si ce membre est égal à zéro, le conteneur de clé est l’un des fournisseurs de stockage de clés CNG.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne **true**. La fonction **GetCryptProvFromCert** retourne la **valeur false** en cas d’échec.

## <a name="remarks"></a>Notes

L’outil [Makecert](makecert.md) appelle **GetCryptProvFromCert** quand vous l’appelez à l’aide de l’option **de ligne de commande-is** .

Si le paramètre *pfDidCryptAcquire* a la valeur **true**, la fonction définit les paramètres *phCryptProv*, *pdwKeySpec* et *pdwProviderType* sur les valeurs du fournisseur.

Lorsque vous avez terminé d’utiliser le fournisseur de services de chiffrement, libérez-le en appelant la fonction [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
