---
title: EnumLayoutOrTipForSetup fonction)
description: Énumère les dispositions de clavier installées et les services de texte de l’interface utilisateur du programme d’installation ou OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- EnumLayoutOrTipForSetup fonction Text Services Framework
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511551"
---
# <a name="enumlayoutortipforsetup-function"></a>EnumLayoutOrTipForSetup fonction)

Énumère les dispositions de clavier installées et les services de texte de l’interface utilisateur du programme d’installation ou OOBE.

## <a name="syntax"></a>Syntaxe


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LangID* \[ dans\]
</dt> <dd>

ID de langue de l’élément à énumérer.

</dd> <dt>

*pLayoutOrTip* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit le tableau de structures LAYOUTORTIP. Il peut s’agir de la **valeur null** pour recevoir le nombre d’éléments.

</dd> <dt>

*uBufLength* \[ dans\]
</dt> <dd>

Longueur de la mémoire tampon vers laquelle pointe *pLayoutOrTip*. Cette valeur est ignorée si *pLayoutOrTip* a la **valeur null**.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Non utilisé. Ce doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si *pLayoutOrTip* a la **valeur null**, le nombre d’éléments de clavier enregistrés dans le système ; dans le cas contraire, il s’agit du nombre d’éléments de clavier copiés dans *pLayoutOrTip*.

## <a name="remarks"></a>Notes

Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte. Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

La définition de LAYOUTORTIP est la suivante :

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

