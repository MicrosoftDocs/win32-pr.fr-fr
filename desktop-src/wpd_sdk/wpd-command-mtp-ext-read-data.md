---
description: La commande \_ wpd \_ MTP \_ ext \_ Read \_ Data de la commande wpd récupère les données de l’appareil après l’exécution de la commande wpd \_ \_ MTP \_ ext \_ Execute \_ \_ , avec les \_ données \_ à \_ lire.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Commande WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526575"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Commande \_ wpd \_ MTP de lecture de \_ données MTP ext \_ \_

La **commande \_ wpd \_ MTP \_ ext \_ Read \_ Data** de la commande wpd récupère les données de l’appareil après l’exécution de la commande **wpd \_ \_ MTP \_ ext \_ Execute, \_ avec les \_ \_ données \_ à \_ lire** .

## <a name="command-category"></a>Catégorie de commande

**\_opérations de \_ \_ fournisseur ext \_ MTP \_ de catégorie wpd**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                                                   | VarType             | Description                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **\_contexte de \_ \_ transfert ext \_ MTP \_ de la propriété wpd**              | \_LPWStr VT          | Obligatoire. Identifie le contexte qui a été retourné par l’appel précédent à l’appareil. |
| **\_propriété wpd \_ \_ \_ \_ nombre \_ d’octets de transfert ext \_ à \_ lire** | VT \_ UI4             | Obligatoire. Spécifie le nombre d’octets à lire.                                       |
| **\_propriété wpd \_ \_ données de \_ transfert ext MTP \_**                 | VT \_ UI1 VT Vector \| \_ | Obligatoire. Identifie la mémoire tampon dans laquelle les données de l’appareil sont copiées.                  |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote retourne les résultats suivants.



| Résultats                                                  | VarType             | Description                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **\_propriété wpd \_ nombre \_ d' \_ octets de transfert ext de transfert MTP \_ \_ \_** | VT \_ UI4             | Obligatoire. Spécifie le nombre d’octets reçus à partir de l’appareil. |
| **\_propriété wpd \_ \_ données de \_ transfert ext MTP \_**             | VT \_ UI1 VT Vector \| \_ | Obligatoire. Mémoire tampon qui contient les données de l’appareil.               |



 

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

 

 




