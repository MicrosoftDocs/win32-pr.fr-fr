---
title: DDCCISaveCurrentSettings fonction)
description: Enregistre les paramètres actuels du moniteur dans le stockage non volatile de l’affichage.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Configuration de l’analyse de fonction DDCCISaveCurrentSettings
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1307747fca18cd1cd86d13c5718240bff260d0882a6865bd817d44632093e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013457"
---
# <a name="ddccisavecurrentsettings-function"></a>DDCCISaveCurrentSettings fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Enregistre les paramètres actuels du moniteur dans le stockage non volatile de l’affichage.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMonitor* 
</dt> <dd>

Handle d’une analyse physique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Remarques

Les applications doivent appeler [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) au lieu d’appeler cette fonction.

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Surveiller les fonctions de configuration](monitor-configuration-functions.md)
</dt> </dl>

 

