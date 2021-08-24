---
description: La \_ commande de \_ capture d’image continue de la commande wpd \_ \_ \_ lance une capture d’image continue par un objet fonctionnel d’image continue. Si un nouvel objet est créé suite à la capture d’une image, le pilote doit envoyer l’événement de l' \_ objet d’événement wpd \_ \_ ajouté.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Commande WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5c5490a5af583753f504decacaccf4b4373890fdb7f0e5b099389df29cdc0571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806279"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>\_Commande d' \_ \_ initialisation de capture d’image continue \_ de la commande wpd \_

La commande de **\_ \_ capture d' \_ image \_ \_ continue de la commande wpd** lance une capture d’image continue par un objet fonctionnel d’image continue. Si un nouvel objet est créé suite à la capture d’une image, le pilote doit envoyer l’événement de l' **\_ objet d’événement wpd \_ \_ ajouté** .

## <a name="command-category"></a>Catégorie de commande

**\_capture d' \_ \_ image continue de catégorie \_ wpd**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                              | VarType    | Description                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cible de \_ la \_ commande \_ commune de la propriété wpd | \_LPWStr VT | Obligatoire. ID d’objet de l’objet fonctionnel de capture d’image continue sur l’appareil qui doit prendre l’image. Chaque objet fonctionnel de capture d’images continues peut avoir des paramètres différents et peut faire référence à un matériel différent sur un appareil (par exemple, un appareil photo avant ou arrière d’un téléphone) et ce paramètre indique celui à utiliser.<br/> |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote doit renvoyer les résultats suivants.



| Résultat                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**             | \_erreur VT | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. les codes d’erreur incluent Windows codes d’erreur des [appareils mobiles](error-constants.md) ou tout autre code d’erreur approprié. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd** | VT \_ UI4   | Facultatif. Code d’erreur spécifique au pilote. Cette valeur est généralement utilisée par les fournisseurs de périphériques pour améliorer le diagnostic des erreurs d’appareil lors de l’utilisation de leurs applications. Les applications à usage général l’ignorent et s’appuient uniquement sur la propriété WPD de \_ \_ HRESULT commun à la \_ place.                                                                                                                   |



 

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

 

 




