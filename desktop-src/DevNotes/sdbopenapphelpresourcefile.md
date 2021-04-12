---
description: Charge le fichier de ressources AppHelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393076"
---
# <a name="sdbopenapphelpresourcefile-function"></a>SdbOpenApphelpResourceFile fonction)

Charge le fichier de ressources AppHelp.

## <a name="syntax"></a>Syntaxe


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszACResourceFile* \[ dans, facultatif\]
</dt> <dd>

Chemin d’accès au fichier de ressources. Si ce paramètre a la **valeur null**, la dll de ressource locale est ouverte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un handle au fichier de ressources ouvert.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




