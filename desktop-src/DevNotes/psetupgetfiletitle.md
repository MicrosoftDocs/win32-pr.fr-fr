---
description: Récupère le titre du fichier pour le chemin d’accès au fichier spécifié.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: pSetupGetFileTitle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539523"
---
# <a name="psetupgetfiletitle-function"></a>pSetupGetFileTitle fonction)

\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]

Récupère le titre du fichier pour le chemin d’accès au fichier spécifié.

## <a name="syntax"></a>Syntaxe


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FilePath* \[ dans\]
</dt> <dd>

Chemin d'accès au fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pointeur vers une chaîne qui reçoit le titre du fichier.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
