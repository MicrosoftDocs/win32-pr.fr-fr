---
title: GetProcessHandleFromHwnd fonction)
description: Récupère un handle de processus à partir d’un handle de fenêtre.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- GetProcessHandleFromHwnd fonction d’accessibilité Windows
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103819"
---
# <a name="getprocesshandlefromhwnd-function"></a>GetProcessHandleFromHwnd fonction)

Récupère un handle de processus à partir d’un handle de fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Type : **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

Handle de fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **handle**](/windows/desktop/WinProg/windows-data-types)**

En cas de réussite, retourne le handle du processus qui possède la fenêtre.

En cas d’échec, retourne **null**.

## <a name="remarks"></a>Notes

Dans les versions précédentes du système d’exploitation, un processus pouvait ouvrir un autre processus (pour accéder à sa mémoire, par exemple) à l’aide de [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess). Cette fonction s’exécute correctement si l’appelant dispose des privilèges appropriés. en général, l’appelant et le processus cible doivent être le même utilisateur.

Sur Windows Vista, toutefois, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) échoue dans le scénario où l’appelant possède l’UIAccess et le processus cible est élevé. Dans ce cas, le propriétaire du processus cible se trouve dans le groupe administrateurs, mais le processus appelant s’exécute avec le jeton restreint, donc il n’est pas membre de ce groupe et l’accès au processus élevé est refusé. Toutefois, si l’appelant possède l’UIAccess, il peut utiliser un hook Windows pour injecter du code dans le processus cible et, à partir du processus cible, renvoyer un handle à l’appelant.

**GetProcessHandleFromHwnd** est une fonction pratique qui utilise cette technique pour obtenir le descripteur du processus qui possède le HWND spécifié. Notez qu’elle ne fonctionne que dans les cas où l’appelant et le processus cible s’exécutent en tant que même utilisateur. Le descripteur retourné possède les privilèges suivants : traiter le handle DUP traiter l’opération de la machine virtuelle traiter le processus lire la machine virtuelle \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ écrire \| synchroniser. Si d’autres privilèges sont requis, il peut être nécessaire d’implémenter la technique de raccordement explicitement au lieu d’utiliser cette fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

