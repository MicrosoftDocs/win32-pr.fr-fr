---
title: DDCCIGetCapabilitiesString fonction)
description: Obtient une chaîne qui décrit les fonctionnalités d’une analyse.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configuration de l’analyse de fonction DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511148"
---
# <a name="ddccigetcapabilitiesstring-function"></a>DDCCIGetCapabilitiesString fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Obtient une chaîne qui décrit les fonctionnalités d’une analyse.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMonitor* \[ dans\]
</dt> <dd>

Handle d’une analyse physique.

</dd> <dt>

*pszString* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la chaîne de fonctionnalités. Pour connaître la longueur de la chaîne de fonctionnalités, appelez [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).

</dd> <dt>

*dwLength* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *pszString* , en caractères, y compris le caractère null de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Notes

Les applications doivent appeler [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) au lieu d’appeler cette fonction.

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

 

