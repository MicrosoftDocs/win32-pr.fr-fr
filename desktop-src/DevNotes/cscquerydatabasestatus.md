---
description: Récupère l’état du cache de Fichiers hors connexion.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541455"
---
# <a name="cscquerydatabasestatus-function"></a>CSCQueryDatabaseStatus fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Récupère l’état du cache de Fichiers hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulStatus* 
</dt> <dd>

Statut. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                               | Signification                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**Indicateur \_ DATABASESTATUS \_ chiffré**</dt> <dt>0x00000002</dt> </dl>                                      | Le cache est marqué pour le chiffrement et tous les fichiers du cache sont chiffrés.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**Indicateur \_ DATABASESTATUS \_ partiellement \_ chiffré**</dt> <dt>0x00000004</dt> </dl>       | Le cache est marqué pour le chiffrement, mais certains fichiers du cache ne sont pas chiffrés.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**Indicateur \_ DATABASESTATUS \_ partiellement \_ non chiffré**</dt> <dt>0x00000004</dt> </dl> | Le cache n’est pas marqué pour le chiffrement, mais tous les fichiers du cache n’ont pas été déchiffrés.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**Indicateur \_ DATABASESTATUS \_ non chiffré**</dt> <dt>0x00000000</dt> </dl>                                | Le cache n’est pas marqué pour le chiffrement et tous les fichiers du cache ont été déchiffrés.<br/>      |



 

</dd> <dt>

*pulErrors* 
</dt> <dd>

Ce paramètre est une valeur différente de zéro s’il existe une erreur de base de données interne ou 0 dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSCIsCSCEnabled**](csciscscenabled.md)
</dt> </dl>

 

 
