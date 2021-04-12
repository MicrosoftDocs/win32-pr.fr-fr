---
description: Ouvre la base de données de shims.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482896"
---
# <a name="sdbinitdatabase-function"></a>SdbInitDatabase fonction)

Ouvre la base de données de shims.

## <a name="syntax"></a>Syntaxe


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre spécifie le format du chemin d’accès dans le paramètre *pszDatabasePath* . Il peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                      | Signification                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_ \_Chemins dos**</dt> <dt>0x00000001</dt> </dl>                             | Un chemin d’accès de style MS-DOS.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_ BASE de données \_ FullPath**</dt> <dt>0x00000002</dt> </dl>     | Chemin d’accès complet.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_ AUCUNE \_ base de données**</dt> <dt>0x00000004</dt> </dl>                       | Le paramètre *pszDatabasePath* est ignoré et aucune base de données n’est ouverte.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_ \_ \_ Masque de type de base de données**</dt> <dt>0xF00F0000</dt> </dl> | Ce paramètre spécifie une base de données prédéfinie. Le paramètre *pszDatabasePath* est ignoré.<br/> |



 

Si *dwFlags* contient **un \_ \_ \_ masque de type de données HID**, ce paramètre peut également inclure l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                               | Signification                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**Sdb \_ 0x80030000 \_ de \_ shim principal de base de données**</dt> <dt></dt> </dl>          | Base de données de shims d’application.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**Sdb \_ BASE de données \_ principale \_ MSI**</dt> <dt>0x80020000</dt> </dl>             | Base de données MSI.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**Sdb \_ \_ \_ Pilotes principaux de base de données**</dt> <dt>0x80040000</dt> </dl> | Base de données des pilotes à bloquer.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ dans\]
</dt> <dd>

Chemin d’accès à la base de données. Ce paramètre peut avoir la **valeur null** si le paramètre *dwFlags* spécifie une base de données prédéfinie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un descripteur à la base de données ouverte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
</dt> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




