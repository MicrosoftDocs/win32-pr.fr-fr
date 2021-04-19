---
title: InstallLayoutOrTip fonction)
description: Active les dispositions de clavier ou les services de texte spécifiés.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- InstallLayoutOrTip fonction Text Services Framework
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510540"
---
# <a name="installlayoutortip-function"></a>InstallLayoutOrTip fonction)

Active les dispositions de clavier ou les services de texte spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PSZ* \[ dans\]
</dt> <dd>

Chaîne qui représente la liste de la disposition du clavier ou la liste des profils des services de texte.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Champ de valeurs de champ qui spécifie les indicateurs suivants :

> [!Note]  
> Les identificateurs suivants ne sont pas définis dans un fichier d’en-tête public. Vous devez soit utiliser la valeur hexadécimale, soit \# définir les identificateurs. Par exemple, pour utiliser **la \_ désinstallation de ilot** , vous devez inclure `#define ILOT_UNINSTALL 0x00000001` dans votre code.

 



| Valeur                                                                                                                                                                                                                                                                      | Signification                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**Ilot \_ Désinstaller**</dt> <dt>0x00000001</dt> </dl>                                           | Identique à **ilot \_ désactivé**.<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**Ilot \_ DEFPROFILE**</dt> <dt>0x00000002</dt> </dl>                                        | Définit la disposition ou le Conseil spécifié en tant qu’élément par défaut.<br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <dt>**Ilot \_ DEFUSER4**</dt> <dt>0x00000004</dt> </dl>                                              | Modifie le paramètre de. Valeurs.<br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <dt>**Ilot \_ SYSLOCALE**</dt> <dt>0x00000008</dt> </dl>                                           | Inutilisé.<br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <dt>**Ilot \_ NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt> </dl>             | Inutilisé.<br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**Ilot \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt> </dl> | Le paramètre est enregistré, mais n’est pas appliqué à la session active.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**Ilot \_ CLEANINSTALL**</dt> <dt>0x00000040</dt> </dl>                                  | Désactive toutes les dispositions de clavier et les services de texte actuels.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**Ilot \_ Désactivation**</dt> de <dt>0x00000080</dt> </dl>                                              | Désactive la disposition de clavier et le service de texte spécifiés.<br/>        |



 

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


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Exemples

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
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



 

