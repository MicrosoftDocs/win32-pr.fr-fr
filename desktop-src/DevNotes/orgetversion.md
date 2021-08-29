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
ms.openlocfilehash: f72f4d9995a9cf01e887770bec2d51c6bf566772a1afd027d3419daf374b07e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653369"
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
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




