---
title: EnumEnabledLayoutOrTip fonction)
description: Énumère toutes les dispositions de clavier activées ou les services de texte du paramètre utilisateur spécifié.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip fonction Text Services Framework
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510138"
---
# <a name="enumenabledlayoutortip-function"></a>EnumEnabledLayoutOrTip fonction)

Énumère toutes les dispositions de clavier activées ou les services de texte du paramètre utilisateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
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

*pLayoutOrTipProfile* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit le tableau LAYOUTORTIPPROFILE.

</dd> <dt>

*uBufLength* \[ dans\]
</dt> <dd>

Longueur de la mémoire tampon vers laquelle pointe *pLayoutOrTipProfile*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si *pLayoutOrTipProfile* a la **valeur null**, le nombre d’éléments de clavier activés dans le paramètre utilisateur ; dans le cas contraire, il s’agit du nombre d’éléments de clavier copiés dans *pLayoutOrTipProfile*.

Pour les langages de l’éditeur de méthode d’entrée (IME), tous les IME sont retournés, même si un seul IME est activé. Par exemple, si CHT New Quick IME est activé pour un utilisateur, la fonction **EnumEnabledLayoutOrTip** retourne les 5 IME cht.

## <a name="remarks"></a>Notes

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

La définition de LAYOUTORTIPPROFILE est la suivante :

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

