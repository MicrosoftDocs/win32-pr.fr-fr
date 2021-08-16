---
description: La fonction WiaAddDevice appelle l’interface utilisateur de l’Assistant Installation du scanneur et de l’appareil photo. Cela équivaut à exécuter &\# 0034 ; rundll32.exe sti \_ci.dll AddDevice&\# 0034 ; à partir de l’invite de commandes.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Fonction WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 81dcff3cdca3459126751b12b86f1e11adc2b4fec8926f69211f0508253b64fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965398"
---
# <a name="wiaadddevice-function"></a>WiaAddDevice fonction)

La fonction **WiaAddDevice** appelle l’interface utilisateur de l’Assistant Installation du scanneur et de l’appareil photo. Cela équivaut à exécuter « rundll32.exe STI \_ci.dll AddDevice » à partir de l’invite de commandes.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction doit être appelée avec les informations d’identification d’administrateur. En cas d’exécution sous le contrôle de compte d’utilisateur (LUA), le processus doit être élevé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




