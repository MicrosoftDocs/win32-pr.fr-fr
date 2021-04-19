---
description: La commande \_ wpd \_ MTP MTP ext extension de la description de l' \_ \_ extension de \_ fournisseur \_ \_ récupère la chaîne de description du fournisseur. Cette chaîne est définie par un jeu de données DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Commande WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539978"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Commande \_ wpd \_ MTP \_ ext \_ \_ \_ extension \_ de la description de l’extension de fournisseur

La **commande \_ wpd \_ MTP MTP \_ ext \_ \_ \_ extension \_** de la description de l’extension de fournisseur récupère la chaîne de description du fournisseur. Cette chaîne est définie par un jeu de données **DeviceInfo** .

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Cette commande n’a pas de paramètres.

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultats                                                      | VarType    | Description                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **propriété WPD-Description de l' \_ \_ \_ extension de fournisseur ext MTP \_ \_ \_** | \_LPWStr VT | Obligatoire. Spécifie la chaîne de description de l’extension de fournisseur. |



 

## <a name="calling-methods"></a>Appel de méthodes

Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WpdMtpExtensions. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des extensions MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




