---
description: Détermine l’emplacement d’une ressource avec le type et le nom spécifiés, dans le module spécifié.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bfd640aaf0bbc68e8798f62f41542d794db34808674c0bdb47587c7396ad7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094194"
---
# <a name="findresourcewrapw-function"></a>FindResourceWrapW fonction)

\[**FindResourceWrapW** peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) à la place.\]

Détermine l’emplacement d’une ressource avec le type et le nom spécifiés, dans le module spécifié.

> [!Note]  
> **FindResourceWrapW** est un wrapper pour la fonction **FindResourceW** . Pour plus d’informations sur l’utilisation, consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .

 

## <a name="syntax"></a>Syntaxe


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HMODULE* \[ dans\]
</dt> <dd>

Type : **HMODULE**

Handle du module dont le fichier exécutable contient la ressource. La valeur **null** spécifie le descripteur de module associé au fichier image utilisé par le système d’exploitation pour créer le processus en cours.

</dd> <dt>

*lpName* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Nom de la ressource. Pour plus d’informations, consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> <dt>

*lpType* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne qui spécifie le type de ressource. Pour plus d’informations, consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRSRC**

Si la fonction est réussie, la valeur de retour est un handle vers le bloc d’informations de la ressource spécifiée. Pour obtenir un descripteur de la ressource, transmettez ce handle à la fonction [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

Si la fonction échoue, la valeur de retour est **null**. Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Remarques

Si vous devez spécifier une localisation particulière, utilisez la fonction [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) au lieu de **FindResourceWrapW**.

**FindResourceWrapW** offre la possibilité d’utiliser des chaînes Unicode dans les systèmes d’exploitation plus anciens. La méthode recommandée consiste à utiliser [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) conjointement avec la couche Microsoft pour Unicode (MSLU).

**FindResourceWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 66.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **FindResourceWrapW** (Unicode)<br/>                                                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
