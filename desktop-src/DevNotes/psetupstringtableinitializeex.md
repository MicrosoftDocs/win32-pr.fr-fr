---
description: fonction pSetupStringTableInitializeEx-Initialise une table de chaînes.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 189bb94b70366ad66f0fe4dd4c4c9d5884e762cf20638f7c3ae2dc9b587f15ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538469"
---
# <a name="psetupstringtableinitializeex-function"></a>pSetupStringTableInitializeEx fonction)

\[cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]

Initialise une table de chaînes.

## <a name="syntax"></a>Syntaxe


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ExtraDataSize* \[ dans\]
</dt> <dd>

Taille de l’objet de données supplémentaire.

</dd> <dt>

*Réservé* \[ dans\]
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
