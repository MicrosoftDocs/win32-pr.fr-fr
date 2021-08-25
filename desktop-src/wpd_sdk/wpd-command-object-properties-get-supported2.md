---
description: Récupère les propriétés prises en charge par un objet.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Commande WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5020494658f380abc465a9059544131174edc8c417f69f6322636e6c9d4170d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703979"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>Propriétés de l' \_ objet de commande wpd \_ recevoir une \_ \_ \_ commande prise en charge

La commande propriétés de l' **\_ objet de commande wpd obtenir la \_ \_ \_ \_ prise en charge** récupère les propriétés prises en charge par un objet.

## <a name="command-category"></a>Catégorie de commande

**Propriétés de l' \_ objet de catégorie wpd \_ \_**

## <a name="parameters"></a>Paramètres

Le pilote attend le paramètre suivant.



| Paramètre                                         | VarType        | Description                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **\_ID d' \_ \_ objet des \_ propriétés \_ de l’objet de propriété wpd** | **\_LPWStr VT** | Obligatoire. ID de l’objet qui contient les propriétés demandées. |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote doit renvoyer les résultats suivants.



| Résultat                                                | VarType         | Description                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propriétés de l’objet de propriété WPD, \_ \_ \_ clés de \_ propriété \_** | **VT \_ inconnu** | Obligatoire. Interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui spécifie toutes les propriétés prises en charge.                                                                                                                                                                                                            |
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**                    | **\_erreur VT**   | Obligatoire. Valeur **HRESULT** qui indique la réussite ou l’échec global. les valeurs possibles des résultats incluent [Windows les codes d’erreur des appareils mobiles](error-constants.md). Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** , mais il n’est pas nécessaire de retourner une autre valeur de résultat. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**        | **VT \_ UI4**     | Facultatif. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Commandes**](commands.md)
</dt> </dl>

 

 




