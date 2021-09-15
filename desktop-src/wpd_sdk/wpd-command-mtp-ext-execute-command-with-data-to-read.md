---
description: La commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ lire commande envoie un bloc de commande MTP, qui est suivi d’une phase de données. (Les données sont envoyées de l’appareil à l’ordinateur hôte.)
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Commande WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404628"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>Commande \_ wpd \_ MTP \_ ext \_ Execute Command Execute \_ \_ avec les \_ données \_ à \_ lire, commande

La **commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ lire** commande envoie un bloc de commande MTP, qui est suivi d’une phase de données. (Les données sont envoyées de l’appareil à l’hôte.)

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                                      | VarType | Description                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **\_code d' \_ \_ opération ext \_ \_ de la propriété wpd MTP**   | VT \_ UI4 | Obligatoire. Identifie un code d’opération MTP étendu par le fournisseur.                                                                    |
| **param, propriété WPD, \_ \_ \_ paramètres d' \_ opération ext \_** | VT \_ UI4 | Obligatoire. Un **IPortableDevicePropVariantCollection**, qui identifie les paramètres requis pour le code d’opération du fournisseur. |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultats                                                       | VarType    | Description                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_propriété wpd \_ - \_ \_ \_ taille totale des \_ données de transfert ext \_**     | \_UI8 VT    | Obligatoire. Retourne la taille totale des données, en octets, à l’exclusion de toute surcharge provenant de l’appareil. Si l’appareil signale une DataSize inconnue (0xFFFFFFFF), le pilote doit appeler **ReadData** à plusieurs reprises jusqu’à ce qu’un petit bloc soit reçu. |
| **\_taille de \_ la \_ \_ \_ \_ mémoire tampon de transfert optimal ext \_ de la propriété wpd** | VT \_ UI4    | Optionnel. Retourne la taille optimale de la mémoire tampon de transfert.                                                                                                                                                                          |
| **\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**               | \_LPWStr VT | Obligatoire. Spécifie l’identificateur de contexte pour les transferts de données suivants.                                                                                                                                                           |



 

## <a name="calling-methods"></a>Appel de méthodes

Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WpdMtpExtensions. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des extensions MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




