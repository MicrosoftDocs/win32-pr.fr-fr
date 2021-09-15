---
description: La commande \_ wpd \_ MTP \_ \_ Write ext \_ Data envoie des données à l’appareil après l’exécution de la commande wpd \_ \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Commande WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411334"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>Commande \_ wpd \_ MTP \_ ext. \_ écriture de \_ données

La **commande \_ wpd \_ MTP \_ \_ Write ext \_ Data** envoie des données à l’appareil après l’exécution de la commande **wpd \_ \_ MTP \_ ext \_ Execute \_ Command \_ avec les \_ données \_ à \_ écrire** .

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                                                    | VarType             | Description                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**               | \_LPWStr VT          | Obligatoire. Identifie le contexte qui a été retourné par l’appel précédent à l’appareil. |
| **\_propriété wpd \_ \_ \_ \_ nombre \_ d’octets de transfert ext MTP \_ à \_ écrire** | VT \_ UI4             | Obligatoire. Spécifie le nombre d’octets à écrire.                                      |
| **\_propriété wpd \_ \_ données de \_ transfert ext MTP \_**                  | VT \_ UI1 VT Vector \| \_ | Obligatoire. Identifie la mémoire tampon dans laquelle les données de l’appareil sont copiées.                  |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultats                                                     | VarType | Description                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **\_propriété wpd \_ nombre d’octets de \_ transfert ext MTP \_ \_ \_ \_ écrits** | VT \_ UI4 | Obligatoire. Spécifie le nombre d’octets envoyés à l’appareil. |



 

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

 

 




