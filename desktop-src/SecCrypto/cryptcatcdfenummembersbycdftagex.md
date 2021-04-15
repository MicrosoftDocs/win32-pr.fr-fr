---
description: Énumère les membres de fichier individuels dans la section CatalogFiles d’un fichier de définition de catalogue (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525732"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>CryptCATCDFEnumMembersByCDFTagEx fonction)

\[La fonction **CryptCATCDFEnumMembersByCDFTagEx** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

La fonction **CryptCATCDFEnumMembersByCDFTagEx** énumère les membres de fichier individuels dans la section **CatalogFiles** d’un fichier de définition de catalogue (CDF). **CryptCATCDFEnumMembersByCDFTagEx** est appelé par [MakeCat](makecat.md).

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCDF* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszPrevCDFTag* \[ in, out\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère **null** qui identifie le membre du fichier catalogue.

</dd> <dt>

*pfnParseError* \[ dans\]
</dt> <dd>

Pointeur vers une fonction définie par l’utilisateur pour gérer les erreurs d’analyse de fichier.

</dd> <dt>

*ppMember* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) qui contient les informations relatives au membre de fichier.

</dd> <dt>

*fContinueOnError* \[ dans\]
</dt> <dd>

Valeur qui spécifie s’il faut conserver en mémoire une référence au dernier membre énuméré.

</dd> <dt>

*pvReserved* \[ dans\]
</dt> <dd>

Ce paramètre est réservé. ne l’utilisez pas.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne un pointeur vers une chaîne se terminant par un caractère **null** qui identifie un membre de fichier dans la section **CATALOGFILES** d’un CDF. La fonction **CryptCATCDFEnumMembersByCDFTagEx** retourne un pointeur **null** en cas d’échec.

## <a name="remarks"></a>Notes

En général, vous appelez cette fonction dans une boucle pour énumérer tous les membres du fichier catalogue dans un CDF. Avant d’entrer dans la boucle, affectez à *pwszPrevCDFTag* la **valeur null**. La fonction retourne un pointeur vers le premier membre. Affectez à *pwszPrevCDFTag* la valeur de retour de la fonction pour les itérations suivantes de la boucle.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la séquence correcte des assignations pour le paramètre *pwszPrevCDFTag* ( `pwszMemberTag` ).


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
