---
description: Utilisé par un fournisseur de services de chiffrement (CSP) pour vérifier la signature d’une DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: CRYPT_VERIFY_IMAGE pointeur de fonction (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521208"
---
# <a name="crypt_verify_image-function-pointer"></a>Chiffrer le \_ pointeur de fonction d’image de vérification \_

La fonction de rappel **FuncVerifyImage** est utilisée par un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour vérifier la signature d’une dll.

Toutes les dll auxiliaires dans lesquelles un CSP effectue des appels de fonction doivent être signées de la même manière (et avec la même clé) que la DLL CSP principale. Pour garantir cette signature, les dll auxiliaires doivent être chargées de manière dynamique à l’aide de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Mais avant le chargement de la DLL, la signature de la DLL doit être vérifiée. Le fournisseur CSP effectue cette vérification en appelant la fonction **FuncVerifyImage** , comme illustré dans l’exemple ci-dessous.

## <a name="syntax"></a>Syntaxe


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszImage* \[ dans\]
</dt> <dd>

Adresse d’une chaîne terminée par le caractère null qui contient le chemin d’accès et le nom de fichier de la DLL pour laquelle vérifier la signature.

</dd> <dt>

*pbSigData* \[ dans\]
</dt> <dd>

Adresse d’une mémoire tampon qui contient la signature.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction réussit, **false** en cas d’échec.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser la fonction de rappel **FuncVerifyImage** pour vérifier la signature d’une dll avant qu’elle ne soit chargée par un CSP.


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
