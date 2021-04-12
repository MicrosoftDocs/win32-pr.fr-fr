---
title: SaveDefaultUserInputSettings fonction)
description: Applique la disposition de clavier utilisateur et le paramètre de service de texte à la ruche utilisateur par défaut.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- SaveDefaultUserInputSettings fonction Text Services Framework
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384235"
---
# <a name="savedefaultuserinputsettings-function"></a>SaveDefaultUserInputSettings fonction)

Applique la disposition de clavier utilisateur et le paramètre de service de texte à la ruche utilisateur par défaut.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Fenêtre parente de la boîte de dialogue d’avertissement. La boîte de dialogue d’avertissement n’est pas toujours affichée et apparaît correctement. Si ce paramètre a la valeur NULL, la boîte de dialogue d’avertissement ne s’affiche pas.

</dd> <dt>

*hSourceRegKey* \[ dans\]
</dt> <dd>

Clé de Registre racine du paramètre utilisateur à copier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                          | Description                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**:**</dt> </dl>  | La fonction a réussi.<br/>   |
| <dl> <dt>**FAUSSES**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="examples"></a>Exemples

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). L’exemple suivant montre comment obtenir un pointeur vers cette fonction.

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

