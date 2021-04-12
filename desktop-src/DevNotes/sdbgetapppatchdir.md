---
description: Récupère le répertoire AppPatch du système.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109923"
---
# <a name="sdbgetapppatchdir-function"></a>SdbGetAppPatchDir fonction)

Récupère le répertoire AppPatch du système.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSDB* \[ dans, facultatif\]
</dt> <dd>

Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szAppPatchPath* \[ à\]
</dt> <dd>

Chemin d’accès résultant.

</dd> <dt>

*cchSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *szAppPatchPath* , en caractères. Si la fonction échoue, ce paramètre est défini sur la chaîne vide ("").

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 




