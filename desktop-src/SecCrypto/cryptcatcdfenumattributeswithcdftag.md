---
description: Énumère les attributs des fichiers membres dans la section CatalogFiles d’un fichier de définition de catalogue (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: f1bffd01865b524b0f06003a6a46b8f81542d7f6113f98db55202e08d8dd7ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768894"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>CryptCATCDFEnumAttributesWithCDFTag fonction)

\[La fonction **CryptCATCDFEnumAttributesWithCDFTag** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

La fonction **CryptCATCDFEnumAttributesWithCDFTag** énumère les attributs des fichiers membres dans la section **CatalogFiles** d’un fichier de définition de catalogue (CDF). **CryptCATCDFEnumAttributesWithCDFTag** est appelé par [MakeCat](makecat.md).

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCDF* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszMemberTag* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère **null** qui identifie le membre du fichier catalogue.

</dd> <dt>

*pMember* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) qui contient les informations de membre.

</dd> <dt>

*pPrevAttr* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) pour un attribut de membre de fichier dans le CDF désigné par *pCDF*.

</dd> <dt>

*pfnParseError* \[ dans\]
</dt> <dd>

Pointeur vers une fonction définie par l’utilisateur pour gérer les erreurs d’analyse de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne un pointeur vers une structure [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) . La fonction **CryptCATCDFEnumAttributesWithCDFTag** retourne un pointeur **null** en cas d’échec.

## <a name="remarks"></a>Remarques

En général, vous appelez cette fonction dans une boucle pour énumérer tous les attributs de membre de fichier de catalogue dans un CDF. Avant d’entrer dans la boucle, affectez à *pPrevAttr* la **valeur null**. La fonction retourne un pointeur vers le premier attribut. Affectez à *pPrevAttr* la valeur de retour de la fonction pour les itérations suivantes de la boucle.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la séquence correcte des assignations pour le paramètre *pPrevAttr* ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
