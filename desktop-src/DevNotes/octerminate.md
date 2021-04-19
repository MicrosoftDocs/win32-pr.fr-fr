---
description: Ferme le gestionnaire OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: OcTerminate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532568"
---
# <a name="octerminate-function"></a>OcTerminate fonction)

Ferme le gestionnaire OC.

## <a name="syntax"></a>Syntaxe


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OcManagerContext* \[ in, out\]
</dt> <dd>

En entrée, contient le pointeur de contexte du gestionnaire OC retourné par [**OcInitialize**](ocinitialize.md). Lors de la sortie, reçoit la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
