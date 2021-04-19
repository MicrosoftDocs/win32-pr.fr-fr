---
description: Crée une instance du moteur de capture.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527337"
---
# <a name="mfcreatecaptureengine-function"></a>MFCreateCaptureEngine fonction)

\[MFCreateCaptureEngine n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. \]

Crée une instance du moteur de capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppCaptureEngine* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) . L’appelant doit libérer l’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne la valeur \_ OK. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation associée et n’est pas déclarée dans un fichier d’en-tête public. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à MFCaptureEngine.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
