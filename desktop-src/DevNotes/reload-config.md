---
description: Recharge une configuration IME à partir du Registre HKCU, uniquement dans l’IME japonais.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: 343003156c2f93788ac87004657a21d3e9b31a47ff4585374836488642de3240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571619"
---
# <a name="reload_config-function"></a>recharger la \_ fonction de configuration

Recharge une configuration IME à partir du Registre HKCU, uniquement dans l’IME japonais.

## <a name="syntax"></a>Syntaxe


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Si aucune valeur de Registre n’est présente dans HKCU, la fonction de **\_ configuration de rechargement** écrit les données initiales dans le registre.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imejpknl.dll ; </dt> <dt>Imejp98k.dll</dt> </dl> |



 

 
