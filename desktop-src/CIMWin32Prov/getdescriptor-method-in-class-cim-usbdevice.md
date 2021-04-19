---
description: La méthode GetDescriptor retourne le descripteur de périphérique USB comme spécifié par les paramètres d’entrée.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Méthode GetDescriptor de la classe CIM_USBDevice (Wmcodecdsp. h)
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
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517188"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a>Méthode GetDescriptor de la classe CIM_USBDevice (Wmcodecdsp. h)

La méthode **GetDescriptor** retourne le descripteur de périphérique USB comme spécifié par les paramètres d’entrée.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

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

Identificateur mappé en bits pour le type de demande de descripteur et le destinataire. Reportez-vous à la spécification USB pour obtenir les valeurs appropriées pour chaque bit.

</dd> <dt>

*RequestValue* \[ dans\]
</dt> <dd>

Contient le type de descripteur dans l’octet de poids fort et l’index de descripteur (par exemple, index ou offset dans le tableau de descripteurs) dans l’octet de poids faible. Pour plus d’informations, consultez la spécification USB.

</dd> <dt>

*RequestIndex* \[ dans\]
</dt> <dd>

Spécifie le code de l’identificateur de langue à 2 octets utilisé par le périphérique USB lors du retour de données de descripteur de chaîne. Le paramètre est généralement 0 (zéro) pour les descripteurs de non-chaîne. Pour plus d’informations, consultez la spécification USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

En entrée, longueur (en octets) du descripteur qui doit être retourné. Si cette valeur est inférieure à la longueur réelle du descripteur, seule la longueur demandée est retournée. Si elle est supérieure à la longueur réelle, la longueur réelle est retournée.

Sur la sortie, la longueur (en octets) de la mémoire tampon retournée. Si le descripteur demandé n’existe pas, le contenu de ce paramètre n’est pas défini.

</dd> <dt>

*Mémoire tampon* \[ à\]
</dt> <dd>

Retourne les informations de descripteur demandées. Si le descripteur n’existe pas, le contenu de ce paramètre n’est pas défini.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) si le descripteur USB est retourné avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur. Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode. Les chaînes dans lesquelles le contenu mofqualifier est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_USBDEVICE CIM**](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

