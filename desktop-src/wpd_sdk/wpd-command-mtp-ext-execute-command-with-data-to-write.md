---
description: La commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire commande envoie un bloc de commande MTP, qui est suivi d’une phase de données. Les données sont envoyées de l’hôte à l’appareil.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Commande WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae0e50ad2fad9967252d9a21c1e864d056338a3e3a2b82f4c29d951a722953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806309"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>Commande \_ wpd \_ MTP \_ ext \_ Execute Command Execute \_ \_ avec les \_ données \_ à \_ écrire, commande

La **commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire** commande envoie un bloc de commande MTP, qui est suivi d’une phase de données. Les données sont envoyées de l’hôte à l’appareil.

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                                                | VarType | Description                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_code d' \_ \_ opération ext \_ \_ de la propriété wpd MTP**             | VT \_ UI4 | Obligatoire. Identifie un code d’opération MTP étendu par le fournisseur.                                                                              |
| **param, propriété WPD, \_ \_ \_ paramètres d' \_ opération ext \_**           | VT \_ UI4 | Obligatoire. Collection **IPortableDevicePropVariantCollection** qui identifie les paramètres requis pour le code d’opération du fournisseur. |
| **\_propriété wpd \_ - \_ \_ \_ taille totale des \_ données de transfert ext \_** | \_UI8 VT | Obligatoire. spécifie la taille totale des données, en octets, à l’exception de toute surcharge, à envoyer à l’appareil.                                         |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultat                                                       | VarType    | Description                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **\_taille de \_ la \_ \_ \_ \_ mémoire tampon de transfert optimal ext \_ de la propriété wpd** | VT \_ UI4    | Obligatoire. Spécifie la taille optimale de la mémoire tampon de transfert.                       |
| **\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**               | \_LPWStr VT | Facultatif. Identificateur de contexte utilisé par le pilote pour les transferts de données suivants. |



 

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

 

 




