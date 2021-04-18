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
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526696"
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



| Résultats                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**             | \_erreur VT | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd** | VT \_ UI4   | Optionnel. Code d’erreur spécifique au pilote. Cette valeur est généralement utilisée par les fournisseurs de périphériques pour améliorer le diagnostic des erreurs d’appareil lors de l’utilisation de leurs applications. Les applications à usage général l’ignorent et s’appuient uniquement sur la propriété WPD de \_ \_ HRESULT commun à la \_ place.                                                                                                                   |



 

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

 

 




