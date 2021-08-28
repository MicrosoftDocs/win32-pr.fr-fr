---
description: La \_ commande de format de stockage de commande wpd \_ \_ met en forme un objet fonctionnel de stockage sur l’appareil.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: Commande WPD_COMMAND_STORAGE_FORMAT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 353710bc4167b626b6af001ef535f6d21538a328609aaf05e5e8846415485914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806199"
---
# <a name="wpd_command_storage_format-command"></a>\_Commande de \_ format de stockage de commande wpd \_

La commande de **\_ format de \_ stockage \_ de commande wpd** met en forme un objet fonctionnel de stockage sur l’appareil.

## <a name="command-category"></a>Catégorie de commande

**\_stockage de catégorie wpd \_**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                          | VarType    | Description                                              |
|------------------------------------|------------|----------------------------------------------------------|
| \_ID d' \_ objet de stockage de propriétés wpd \_ \_ | \_LPWStr VT | Obligatoire. ID d’objet du support de stockage à mettre en forme. |



 

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

 

 




