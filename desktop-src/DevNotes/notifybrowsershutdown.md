---
description: Libère les chargeurs de classes Java qui ont pu être consommés lors de l’exploration des applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520917"
---
# <a name="notifybrowsershutdown-function"></a>NotifyBrowserShutdown fonction)

Libère les chargeurs de classes Java qui ont pu être consommés lors de l’exploration des applets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpvReserved* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est **S \_ OK**. Dans le cas contraire, la valeur de retour est un code d’erreur.

## <a name="remarks"></a>Notes

Lorsque le nombre de fenêtres du navigateur atteint zéro en mode Web intégré, cette fonction libère les chargeurs de classe Java. Lorsque l’utilisateur redémarre l’exploration des applets, la machine virtuelle Java télécharge les derniers fichiers de classe.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
