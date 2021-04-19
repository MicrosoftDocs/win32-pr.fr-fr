---
title: QueryLayoutOrTipString fonction)
description: Interroge la chaîne spécifiée qui représente le format d’une liste de disposition de clavier ou d’une liste de profils de services de texte.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- QueryLayoutOrTipString fonction Text Services Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511382"
---
# <a name="querylayoutortipstring-function"></a>QueryLayoutOrTipString fonction)

Interroge la chaîne spécifiée qui représente le format d’une liste de disposition de clavier ou d’une liste de profils de services de texte.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

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



| Code de retour                                                                                  | Description                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Toutes les dispositions ou tous les profils définis dans *PSZ* sont valides.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Une ou plusieurs des dispositions ou des profils définis dans *PSZ* ne sont pas valides.<br/> |



 

## <a name="remarks"></a>Notes

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

