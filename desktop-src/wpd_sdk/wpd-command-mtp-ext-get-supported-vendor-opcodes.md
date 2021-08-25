---
description: La commande \_ wpd \_ MTP \_ ext \_ \_ prise en charge des OpCodes du fournisseur de la commande wpd \_ \_ envoie un bloc de commande MTP. Aucune phase de données ultérieure n’est associée à cette commande.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Commande WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b0ab00fc3ada963e56dced49f97d3c1dbca578dfc5c1cded4735f9df947ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927969"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>Commande \_ wpd \_ MTP \_ MTP \_ afficher \_ les \_ OpCodes fournisseur pris en charge \_

La **commande \_ wpd \_ MTP \_ ext \_ \_ prise en charge des \_ \_ OpCodes du fournisseur de la commande wpd** envoie un bloc de commande MTP. Aucune phase de données ultérieure n’est associée à cette commande.

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Cette commande n’a pas de paramètres.

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultat                                                | VarType | Description                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **\_codes d' \_ \_ opération du \_ fournisseur ext MTP \_ \_ de la propriété wpd** | VT \_ UI4 | Obligatoire. **IPortableDevicePropVariantCollection** qui contient tous les codes d’opération étendus par le fournisseur. |



 

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

 

 




