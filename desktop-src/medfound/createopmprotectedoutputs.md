---
description: Crée des objets de sortie protégés pour un périphérique d’affichage.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: fe2bcc0d190cf94a48b10f3d588ab4acd2d93913552f8ccef9d7eb92fefa598b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829059"
---
# <a name="createopmprotectedoutputs-function"></a>CreateOPMProtectedOutputs fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Crée des objets de sortie protégés pour un périphérique d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pstrDeviceName* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ chaîne Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) qui contient le nom du périphérique d’affichage, tel que retourné par la fonction [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .

</dd> <dt>

*vos* \[ dans\]
</dt> <dd>

Membre de l’énumération de la **\_ \_ \_ \_ sémantique de sortie vidéo de l’DXGKMDT OPM** , indiquant si la sortie protégée aura une sémantique COPP (Certified Output Protection Protocol) ou OPM.

</dd> <dt>

*dwOPMProtectedOutputArraySize* \[ dans\]
</dt> <dd>

Nombre d’éléments dans le tableau *pohOPMProtectedOutputArray* .

</dd> <dt>

*pdwNumOPMProtectedOutputsInArray* \[ à\]
</dt> <dd>

Reçoit le nombre d’éléments que la fonction copie dans le tableau *pohOPMProtectedOutputArray* .

</dd> <dt>

*pohOPMProtectedOutputArray* \[ à\]
</dt> <dd>

Tableau qui reçoit des handles vers les objets de sortie protégés. Chaque descripteur doit être libéré en appelant [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Remarques

Au lieu d’utiliser cette fonction, les applications doivent appeler l’une des fonctions suivantes :

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions OPM](opm-functions.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 
