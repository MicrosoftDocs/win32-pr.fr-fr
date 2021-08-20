---
title: QueryLayoutOrTipStringUserReg fonction)
description: Interroge la chaîne spécifiée qui représente le format d’une liste de dispositions de clavier ou d’une liste de profils de services de texte du chemin d’accès au registre spécifié.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- QueryLayoutOrTipStringUserReg fonction Text Services Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e084d620e476f9b9a941d91f78310e7499dfd736f6cd252fc89aeffe1c652bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951496"
---
# <a name="querylayoutortipstringuserreg-function"></a>QueryLayoutOrTipStringUserReg fonction)

Interroge la chaîne spécifiée qui représente le format d’une liste de dispositions de clavier ou d’une liste de profils de services de texte du chemin d’accès au registre spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszUserReg* \[ dans\]
</dt> <dd>

Chemin d’accès au registre de l’utilisateur. Si ce paramètre a la **valeur null**, HKEY \_ Current \_ User est utilisé.

</dd> <dt>

*pszSystemReg* \[ dans\]
</dt> <dd>

Chemin d’accès au registre du système. Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ System est utilisé.

</dd> <dt>

*pszSoftwareReg* \[ dans\]
</dt> <dd>

Chemin d’accès du Registre du logiciel. Si ce paramètre a la **valeur null**, HKEY \_ local \_ machine \\ Software est utilisé.

</dd> <dt>

*PSZ* \[ dans\]
</dt> <dd>

Chaîne qui représente une liste de dispositions de clavier ou une liste de profils de services de texte.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Doit être 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Toutes les dispositions ou tous les profils définis dans **PSZ** sont valides.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Une ou plusieurs des dispositions ou des profils définis dans **PSZ** ne sont pas valides.<br/> |



 

## <a name="remarks"></a>Remarques

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Le format de chaîne de la liste de présentation est le suivant :

<LangID 1> : <KLID 1> ; \[ ...<LangID N>:<KLID N>

Le format de chaîne de la liste des profils de service de texte est le suivant :

<LangID 1> : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Voici un exemple de valeur pour le paramètre *PSZ* :

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

