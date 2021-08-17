---
description: Annule une opération d’attente inscrite émise par la fonction RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: UnregisterWaitEx, fonction (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 4181aa43cb0c2844f99b7ad81b448271366eb2925740c25d400f891389efb129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765521"
---
# <a name="unregisterwaitex-function"></a>UnregisterWaitEx fonction)

Annule une opération d’attente inscrite émise par la fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*WaitHandle* \[ dans\]
</dt> <dd>

Handle d'attente. Ce descripteur est retourné par la fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

</dd> <dt>

*CompletionEvent* \[ dans, facultatif\]
</dt> <dd>

Handle de l’objet d’événement à signaler lorsque l’opération d’attente a été annulée. Ce paramètre peut être **NULL**.

Si ce paramètre n’est **pas une \_ \_ valeur de handle valide**, la fonction attend la fin de toutes les fonctions de rappel avant de retourner.

Si ce paramètre a la **valeur null**, la fonction marque le minuteur pour la suppression et le retourne immédiatement. Toutefois, la plupart des appelants doivent attendre la fin de la fonction de rappel afin qu’ils puissent effectuer tout nettoyage nécessaire.

Si l’appelant fournit cet événement et que la fonction réussit ou que la fonction échoue avec l' **erreur \_ e/s \_ en attente**, ne fermez pas l’événement tant qu’il n’est pas signalé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Vous ne pouvez pas effectuer un appel bloquant à **UnregisterWaitEx** à partir d’une fonction de rappel pour la même opération d’attente. Dans le cas contraire, le rappel attendra qu’il se termine. En général, un appel bloquant à **UnregisterWaitEx** crée une dépendance entre le thread actuel et le rappel, donc pour effectuer un appel de désinscription de blocage sur une autre opération d’attente, vous devez vous assurer que les fonctions de rappel ne dépendent pas les unes des autres et que la deuxième opération d’attente n’effectue pas non plus un appel de désinscription de blocage sur la première opération.

Soyez prudent lorsque vous effectuez un appel **UnregisterWaitEx** bloquant sur un thread persistant. Si l’opération d’attente en cours d’annulation d’inscription a été créée avec **WT \_ EXECUTEINPERSISTENTTHREAD**, un blocage peut se produire.

Après avoir effectué un appel non bloquant à **UnregisterWaitEx**, aucune nouvelle fonction de rappel associée à *WaitHandle* ne peut être mise en file d’attente. Toutefois, il peut y avoir des fonctions de rappel en attente déjà mises en file d’attente dans les threads de travail.

Dans certaines conditions, la fonction échoue avec l' **erreur \_ e/s \_ en attente** si *CompletionEvent* a la **valeur null**. Cela indique qu’il existe des fonctions de rappel en attente. Ces rappels s’exécutent ou sont en cours d’exécution.

Si *CompletionEvent* est un handle d’événement fourni par l’appelant, il est possible que la fonction réussisse, échoue avec une **erreur d' \_ e/s \_ en attente** ou échoue avec un code d’erreur différent. Si la fonction réussit, ou si la fonction échoue avec l' **erreur \_ e/s \_ en attente**, l’appelant doit toujours attendre que l’événement soit signalé pour fermer l’événement. Si la fonction échoue avec un code d’erreur différent, il n’est pas nécessaire d’attendre que l’événement soit signalé pour fermer l’événement.

**Windows XP :** Si *CompletionEvent* est un handle d’événement fourni par l’appelant et que la fonction échoue avec une **erreur d' \_ e/s \_ en attente**, l’appelant doit attendre jusqu’à ce que l’événement soit signalé pour fermer l’événement. ce comportement a été modifié à partir de Windows Vista.

Pour compiler une application qui utilise cette fonction, définissez **\_ Win32 \_ winnt** comme 0x0500 ou version ultérieure. pour plus d’informations, consultez [utilisation des en-têtes de Windows](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                                                                                                           |
| En-tête<br/>                   | <dl> <dt>Threadpoollegacyapiset. h sur Windows 8 et Windows Server 2012 (inclure Windows. h);</dt> <dt>WinBase. h sur Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP et Windows Server 2003 (include Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Fonctions de synchronisation](synchronization-functions.md)
</dt> <dt>

[Regroupement des threads](../procthread/thread-pooling.md)
</dt> </dl>

 

 
