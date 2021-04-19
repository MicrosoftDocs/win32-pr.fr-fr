---
description: Retourne le descripteur USBDevice comme spécifié par les paramètres d’entrée.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Méthode GetDescriptor de la classe CIM_USBDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529780"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>Méthode GetDescriptor de la classe CIM_USBDevice (gestion Hyper-V)

Retourne le descripteur USBDevice comme spécifié par les paramètres d’entrée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestType* \[ dans\]
</dt> <dd>

Mappage de bits qui identifie le type de demande de descripteur et le destinataire. Le type de la demande peut être « standard », « Class » ou « Specification Vendor ». Le destinataire peut être « Device », « interface », « Endpoint » ou « other ». Reportez-vous à la spécification USB pour obtenir les valeurs appropriées pour chaque bit.

</dd> <dt>

*RequestValue* \[ dans\]
</dt> <dd>

Contient le type de descripteur dans l’octet de poids fort et l’index de descripteur (par exemple, index ou offset dans le tableau de descripteurs) dans l’octet de poids faible. Pour plus d’informations, reportez-vous à la spécification USB.

</dd> <dt>

*RequestIndex* \[ dans\]
</dt> <dd>

Définit le code d’ID de langage de 2 octets utilisé par USBDevice lors du retour de données de descripteur de chaîne. Le paramètre est généralement 0 pour les descripteurs de non-chaîne. Pour plus d’informations, reportez-vous à la spécification USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

En entrée, contient la longueur (en octets) du descripteur qui doit être retourné. Si cette valeur est inférieure à la longueur réelle du descripteur, seule la longueur demandée est retournée. Si elle est supérieure à la longueur réelle, la longueur réelle est retournée. Lors de la sortie, ce paramètre correspond à la longueur, en octets, de la mémoire tampon retournée. Si le descripteur demandé n’existe pas, le contenu de ce paramètre n’est pas défini.

</dd> <dt>

*Mémoire tampon* \[ à\]
</dt> <dd>

Retourne les informations de descripteur demandées. Si le descripteur n’existe pas, le contenu du paramètre n’est pas défini.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

 




