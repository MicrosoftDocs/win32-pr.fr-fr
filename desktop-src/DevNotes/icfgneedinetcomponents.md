---
description: Détermine si les composants marqués dans les options sont installés sur le système.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 9b0d533e234986f54c6a4de668273bda08d9c810dc9f5a93acb3aaf030cea665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390659"
---
# <a name="icfgneedinetcomponents-function"></a>IcfgNeedInetComponents fonction)

Détermine si les composants marqués dans les options sont installés sur le système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwfOptions* 
</dt> <dd>

Combinaison des indicateurs suivants qui spécifient les composants à détecter dans la liste suivante.



| Valeur                                                                                                                                                                                                                                  | Signification                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt> </dl> | la messagerie Internet ou Exchange est-elle nécessaire ?<br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt> </dl>    | RAS est-il nécessaire ?<br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt> </dl>    | TCP/IP est-il nécessaire ?<br/>                    |



 

</dd> <dt>

*lpfNeedComponents* 
</dt> <dd>

Si cette valeur n’est pas **null**, elle a la valeur **true** en cas de retour si un ou plusieurs composants ne sont pas installés sur le système.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Si aucune erreur ne se produit, elle retourne le code d' **erreur de \_ réussite** .

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Icfgnt5.dll</dt> </dl> |



 

 
