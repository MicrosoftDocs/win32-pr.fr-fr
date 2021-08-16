---
description: Installe les composants système spécifiés.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 7708dd065c066ce3e9fd8e4de1044c6bc8587d2526abdf9aeac175b4387dec42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827233"
---
# <a name="icfginstallinetcomponents-function"></a>IcfgInstallInetComponents fonction)

Installe les composants système spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* 
</dt> <dd>

Handle de la fenêtre parente.

</dd> <dt>

*dwfOptions* 
</dt> <dd>

Combinaison des indicateurs suivants qui contrôlent l’installation et la configuration.



| Valeur                                                                                                                                                                                                                                  | Signification                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | installez Exchange et la messagerie Internet.<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | Installez RAS (si nécessaire).<br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | Installez TCP/IP (si nécessaire).<br/>         |



 

</dd> <dt>

*lpfNeedsRestart* 
</dt> <dd>

si cette valeur n’est pas **NULL**, on retourne la valeur **TRUE** uniquement si Windows devez redémarrer pour terminer l’installation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Si aucune erreur ne se produit, elle retourne le code d' **erreur de \_ réussite** .

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
