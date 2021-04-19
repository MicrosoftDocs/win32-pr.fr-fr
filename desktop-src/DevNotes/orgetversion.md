---
description: Cette fonction récupère la version de la bibliothèque de Registre hors connexion.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: ORGetVersion, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541286"
---
# <a name="orgetversion-function"></a>ORGetVersion fonction)

Cette fonction récupère la version de la bibliothèque de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwMajorVersion* \[ à\]
</dt> <dd>

Pointeur vers une variable qui doit recevoir la version principale de la bibliothèque de Registre hors connexion. Pour la version initiale de la bibliothèque, la valeur est 1.

</dd> <dt>

*pdwMinorVersion* \[ à\]
</dt> <dd>

Pointeur vers une variable qui doit recevoir la version mineure de la bibliothèque de Registre hors connexion. Pour la version initiale de la bibliothèque, la valeur est 0.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




