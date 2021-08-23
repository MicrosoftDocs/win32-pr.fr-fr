---
description: Ajoute des paramètres de DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) à un port de Fibre Channel synthétique sur une machine virtuelle.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Méthode AddFibreChannelChap de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26a9f99826e92a35462f0c42e8fce723168799177e96e0ae429aad45c99de928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562359"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Méthode AddFibreChannelChap de la \_ classe VirtualSystemManagementService MSVM

Ajoute des paramètres de DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) à un port de Fibre Channel synthétique sur une machine virtuelle. Cette méthode échoue si l’ordinateur virtuel est en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FcPortSettings* \[ dans\]
</dt> <dd>

Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) qui décrit les paramètres des ports de Fibre Channel synthétique pour les ordinateurs virtuels. La propriété **InstanceID** de chacune de ces instances identifie les éléments à modifier.

</dd> <dt>

*SecretEncoding* \[ dans\]
</dt> <dd>

Spécifie le type d’encodage pour le secret partagé.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**ASCII imprimable** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binaire** (2)


</dt> <dd></dd> </dl> </dd> <dt>

Sous-son  \[ dans\]
</dt> <dd>

Spécifie le secret partagé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




