---
title: GetPhysicalMonitors fonction)
description: Obtient les moniteurs physiques associés à un périphérique d’affichage.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Configuration de l’analyse de fonction GetPhysicalMonitors
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94cef0352aae75f95b1ff7ee9e65937f82c7b598a19cdce768028173dc97331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146152"
---
# <a name="getphysicalmonitors-function"></a>GetPhysicalMonitors fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Obtient les moniteurs physiques associés à un périphérique d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pstrDeviceName* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/desktop/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*dwPhysicalMonitorArraySize* \[ dans\]
</dt> <dd>

Nombre d’éléments dans le tableau *pdwNumPhysicalMonitorHandlesInArray* . Pour connaître la taille requise du tableau, appelez [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).

</dd> <dt>

*pdwNumPhysicalMonitorHandlesInArray* \[ à\]
</dt> <dd>

Reçoit le nombre d’éléments que la fonction copie dans le tableau *phPhysicalMonitorArray* .

</dd> <dt>

*phPhysicalMonitorArray* \[ à\]
</dt> <dd>

Tableau qui reçoit des handles vers les analyses physiques. Chaque descripteur doit être libéré en appelant [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Remarques

Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

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

 

