---
title: TF_InvalidAssemblyListCacheIfExist fonction)
description: La \_ fonction TF InvalidAssemblyListCacheIfExist invalide le cache de description du processeur d’entrée de texte.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- Infrastructure des services de texte de fonction TF_InvalidAssemblyListCacheIfExist
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508437"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a>TF \_ InvalidAssemblyListCacheIfExist fonction)

La fonction **tf \_ InvalidAssemblyListCacheIfExist** invalide le cache de description du processeur d’entrée de texte. Il n’est pas nécessaire d’appeler cette fonction si le programme d’installation du processeur d’entrée requiert un redémarrage ou une ouverture de session. Le cache est valide jusqu’à ce que l’utilisateur se déconnecte.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | La fonction a réussi.<br/>   |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="examples"></a>Exemples

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). L’exemple suivant montre comment obtenir un pointeur vers cette fonction.

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                      |
| DLL<br/>                      | <dl> <dt>Msctf.dll</dt> </dl> |



 

