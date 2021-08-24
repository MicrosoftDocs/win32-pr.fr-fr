---
description: La commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans \_ \_ commande Data phase envoie un bloc de commande MTP. Aucune phase de données ultérieure n’est associée à cette commande.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Commande WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c4d1d5af4d1e4e712f3a39dd5cbb296133bb16f4de3b677da4a45fa7bbc204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806299"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>Commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans \_ \_ commande Data phase

La **commande \_ wpd \_ MTP \_ ext \_ Execute \_ Command \_ sans commande \_ Data \_ phase** envoie un bloc de commande MTP. Aucune phase de données ultérieure n’est associée à cette commande.

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



| Résultat                                        | VarType | Description                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **\_Code de \_ \_ réponse MTP \_ ext \_ de la propriété wpd**   | VT \_ UI4 | Obligatoire. Code de réponse au code d’opération du fournisseur.                                                                      |
| **param, propriété WPD, \_ \_ \_ paramètres de \_ réponse ext \_** | VT \_ UI4 | Facultatif. **IPortableDevicePropVariantCollection** qui identifie les paramètres de réponse. Cette collection peut être vide. |



 

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

 

 




