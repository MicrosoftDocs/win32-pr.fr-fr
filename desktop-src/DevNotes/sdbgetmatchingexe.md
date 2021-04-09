---
description: Recherche l’exécutable spécifié.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861050"
---
# <a name="sdbgetmatchingexe-function"></a>SdbGetMatchingExe fonction)

Recherche l’exécutable spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSDB* \[ dans, facultatif\]
</dt> <dd>

Handle de la base de données de shims retournée par la fonction [**SdbInitDatabase**](sdbinitdatabase.md) .

</dd> <dt>

*szPath* \[ dans\]
</dt> <dd>

Chemin de l’exécutable.

</dd> <dt>

*szModuleName* \[ dans, facultatif\]
</dt> <dd>

Nom du module.

</dd> <dt>

*pszEnvironment* \[ dans, facultatif\]
</dt> <dd>

Variables d’environnement à utiliser comme contexte de recherche.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre peut avoir la valeur 0 ou **SDBGMEF \_ ignorer l' \_ environnement** (0x1).

</dd> <dt>

*pQueryResult* \[ à\]
</dt> <dd>

Structure [**SDBQUERYRESULT**](sdbqueryresult.md) . Si aucune correspondance n’est trouvée, la structure contient **TAGREF \_ null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="remarks"></a>Notes

Une fois que vous avez terminé avec le [**TAGREF**](tagref.md)retourné, libérez-le à l’aide de la fonction [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> </dl>

 

 




