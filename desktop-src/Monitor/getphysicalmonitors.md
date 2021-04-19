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
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532047"
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

## <a name="remarks"></a>Notes

Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :

-   [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Surveiller les fonctions de configuration](monitor-configuration-functions.md)
</dt> </dl>

 

