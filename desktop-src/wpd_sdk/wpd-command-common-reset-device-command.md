---
description: La commande de \_ réinitialisation d’appareil pour la commande wpd réinitialise \_ \_ \_ l’appareil. Cela ne signifie pas de reformatage ; Cela équivaut à éteindre et rallumer l’appareil.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Commande WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411335"
---
# <a name="wpd_command_common_reset_device-command"></a>Commande WPD- \_ \_ commande de \_ réinitialisation d' \_ appareil courante

La commande de **\_ \_ \_ réinitialisation d' \_ appareil pour la commande wpd** réinitialise l’appareil. Cela ne signifie pas de reformatage ; Cela équivaut à éteindre et rallumer l’appareil.

## <a name="command-category"></a>Catégorie de commande

**WPD, \_ catégorie \_ commune**

## <a name="parameters"></a>Paramètres

Cette commande n’a pas de paramètres.

## <a name="return-value"></a>Valeur renvoyée

Le pilote doit renvoyer les résultats suivants.



| Résultats                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**             | \_erreur VT | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. les codes d’erreur incluent Windows codes d’erreur des [appareils mobiles](error-constants.md) ou tout autre code d’erreur approprié. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd** | VT \_ UI4   | Optionnel. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Appel de méthodes

Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Commandes**](commands.md)
</dt> </dl>

 

 




