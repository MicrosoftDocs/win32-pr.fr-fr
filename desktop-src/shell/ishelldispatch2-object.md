---
description: Étend l’objet IShellDispatch avec diverses nouvelles fonctionnalités.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objet IShellDispatch2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 481e64c00ced458be05255af451206a42d449c42d157794dfd1077cf2dda278a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721089"
---
# <a name="ishelldispatch2-object"></a>Objet IShellDispatch2

Étend l’objet [**IShellDispatch**](ishelldispatch.md) avec diverses nouvelles fonctionnalités.

> [!Note]  
> **IShellDispatch2** est implémenté et accessible via l’objet [**Shell**](shell.md) .

 

## <a name="members"></a>Membres

L’objet **IShellDispatch2** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **IShellDispatch2** a ces méthodes.



| Méthode                                                               | Description                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | Affiche la boîte de dialogue **Rechercher l’imprimante** .<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | Récupère des informations système.<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | Récupère le paramètre de restriction d’un groupe à partir du Registre.<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | Retourne une valeur qui indique si un service particulier est en cours d’exécution.<br/> |
| [**ServiceStart**](ishelldispatch2-servicestart.md)                 | Démarre un service nommé.<br/>                                                 |
| [**ServiceStop**](ishelldispatch2-servicestop.md)                   | Arrête un service nommé.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Exécute une opération spécifiée sur un fichier spécifié.<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | Affiche une barre de navigateur.<br/>                                                 |



 

## <a name="remarks"></a>Remarques

pour plus d’informations sur les services Windows, consultez la documentation sur les [services](../services/services.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objet Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 
