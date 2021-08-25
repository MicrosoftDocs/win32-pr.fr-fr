---
description: La fonction DllGetVersion récupère le numéro de version de Cabinet.dll à l’aide de la structure CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: DllGetVersion fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 7671465d20987de9ebe526db5961513c81cea5b30d6ad095baf4d3df3d798194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654039"
---
# <a name="dllgetversion-function"></a>DllGetVersion fonction)

\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.\]

La fonction **DllGetVersion** récupère le numéro de version de Cabinet.dll à l’aide de la structure [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) .

## <a name="syntax"></a>Syntaxe


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcdvi* 
</dt> <dd>

Pointeur vers la structure [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) qui contient les informations de version.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)
</dt> <dt>

[**GetDllVersion**](getdllversion.md)
</dt> </dl>

 

 
