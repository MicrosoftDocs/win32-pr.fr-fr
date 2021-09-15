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
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520976"
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



| Résultats                                                | VarType         | Description                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propriétés de l’objet de propriété WPD, \_ \_ \_ clés de \_ propriété \_** | **VT \_ inconnu** | Obligatoire. Interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui spécifie toutes les propriétés prises en charge.                                                                                                                                                                                                            |
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**                    | **\_erreur VT**   | Obligatoire. Valeur **HRESULT** qui indique la réussite ou l’échec global. les valeurs possibles des résultats incluent [Windows les codes d’erreur des appareils mobiles](error-constants.md). Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** , mais il n’est pas nécessaire de retourner une autre valeur de résultat. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**        | **VT \_ UI4**     | facultatif. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Commandes**](commands.md)
</dt> </dl>

 

 




