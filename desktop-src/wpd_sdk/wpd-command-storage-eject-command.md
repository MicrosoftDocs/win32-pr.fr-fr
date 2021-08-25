---
description: La \_ \_ commande d’éjection du stockage de commande wpd \_ éjecte un support de stockage qui peut être éjecté à distance par l’ordinateur.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: Commande WPD_COMMAND_STORAGE_EJECT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a35b376ed9688217edfde03c76aed962d3e5fb74dc3d8bb7cc927ef1f621c9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839009"
---
# <a name="wpd_command_storage_eject-command"></a>\_Commande wpd \_ stockage commande \_ EJECT

La commande d' **\_ éjection du \_ stockage \_ de commande wpd** éjecte un support de stockage qui peut être éjecté à distance par l’ordinateur.

## <a name="command-category"></a>Catégorie de commande

**\_stockage de catégorie wpd \_**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                          | VarType    | Description                                             |
|------------------------------------|------------|---------------------------------------------------------|
| \_ID d' \_ objet de stockage de propriétés wpd \_ \_ | \_LPWStr VT | Obligatoire. ID d’objet de l’objet de stockage à éjecter. |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote doit renvoyer les résultats suivants.



| Résultat                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**             | \_erreur VT | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. les codes d’erreur incluent Windows codes d’erreur des [appareils mobiles](error-constants.md) ou tout autre code d’erreur approprié. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd** | VT \_ UI4   | Facultatif. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Appel de méthodes

Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Commandes**](commands.md)
</dt> </dl>

 

 




