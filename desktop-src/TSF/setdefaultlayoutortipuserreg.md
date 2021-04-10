---
title: SetDefaultLayoutOrTipUserReg fonction)
description: Définit la disposition de clavier spécifiée ou un service de texte comme élément d’entrée par défaut du registre de l’utilisateur.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- SetDefaultLayoutOrTipUserReg fonction Text Services Framework
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103017"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>SetDefaultLayoutOrTipUserReg fonction)

Définit la disposition de clavier spécifiée ou un service de texte comme élément d’entrée par défaut du registre de l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszUserReg* \[ dans, facultatif\]
</dt> <dd>

Chemin d’accès au registre de l’utilisateur. Si ce paramètre a la **valeur null**, HKEY \_ Current \_ User est utilisé.

</dd> <dt>

*pszSystemReg* \[ dans, facultatif\]
</dt> <dd>

Chemin d’accès au registre du système. Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ System est utilisé.

</dd> <dt>

*pszSoftwareReg* \[ dans, facultatif\]
</dt> <dd>

Chemin d’accès du Registre du logiciel. Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ Software est utilisé.

</dd> <dt>

*PSZ* \[ dans\]
</dt> <dd>

Chaîne qui représente la liste de la disposition du clavier ou la liste des profils des services de texte.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Champ de valeurs de champ qui spécifie les indicateurs suivants :

> [!Note]  
> Les identificateurs suivants ne sont pas définis dans un fichier d’en-tête public. Vous devez soit utiliser la valeur hexadécimale, soit \# définir les identificateurs. Par exemple, pour utiliser SDLOT \_ NOAPPLYTOCURRENTSESSION, vous devez inclure \# define SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 dans votre code.

 



| Valeur                                                                                                                                                                                                                                                                         | Signification                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | Stocke le paramètre dans le registre, mais ne met pas à jour le paramètre de clavier du runtime de la session active. Si l’autre chemin d’accès au registre est défini dans **SetDefaultLayoutOrTipUserReg**, cet indicateur doit être défini.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | Applique le paramètre immédiatement sur le thread actuel.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                          | Description                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**:**</dt> </dl>  | La fonction a réussi.<br/>   |
| <dl> <dt>**FAUSSES**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

Le format de chaîne de la liste de présentation est le suivant :

<LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N>

Le format de chaîne de la liste des profils de service de texte est le suivant :

<LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Voici un exemple de valeur pour le paramètre *PSZ* :


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Exemples

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). L’exemple suivant montre comment obtenir un pointeur vers cette fonction.

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
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



 

