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
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528919"
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



| Résultats                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**             | \_erreur VT | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd** | VT \_ UI4   | Optionnel. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                                                |



 

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

 

 




