---
description: La commande WPD de \_ \_ fin de \_ \_ \_ transfert de données de fin MTP MTP \_ termine une réponse de transfert de données et de lecture de l’appareil.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Commande WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540022"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>Commande \_ wpd \_ MTP \_ MTP \_ End \_ Data \_ Transfer

La commande **wpd de fin de \_ \_ \_ \_ \_ \_ transfert de données de fin MTP MTP** termine une réponse de transfert de données et de lecture de l’appareil. Le transfert est initié par la commande [**wpd \_ \_ MTP \_ ext \_ Execute \_ Command, avec les \_ \_ données \_ à \_ lire**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) ou la commande [**wpd \_ \_ MTP \_ ext \_ Execute \_ Command avec les \_ \_ données \_ à \_ écrire**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) .

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                                      | VarType    | Description                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd** | \_LPWStr VT | Obligatoire. Identifie le contexte retourné par un appel de méthode antérieur. |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultats                                        | VarType | Description                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_Code de \_ \_ réponse MTP \_ ext \_ de la propriété wpd**   | VT \_ UI4 | Requis. code de réponse au code d’opération du fournisseur.                                                                                |
| **param, propriété WPD, \_ \_ \_ paramètres de \_ réponse ext \_** | VT \_ UI4 | Optionnel. Collection **IPortableDevicePropVariantCollection** qui identifie les paramètres de réponse. Cette collection peut être vide. |



 

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

 

