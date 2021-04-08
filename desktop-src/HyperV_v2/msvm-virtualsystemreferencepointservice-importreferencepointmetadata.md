---
description: Importe les métadonnées de point de référence du système virtuel.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Méthode ImportReferencePointMetadata de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953450"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Méthode ImportReferencePointMetadata de la \_ classe VirtualSystemReferencePointService MSVM

Importe les métadonnées de point de référence du système virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AffectedSystem* \[ dans\]
</dt> <dd>

Référence à un [**\_ ComputerSystem MSVM**](msvm-computersystem.md) décrivant le système affecté.

</dd> <dt>

*ConfigFilePath* \[ dans\]
</dt> <dd>

Chemin d’accès complet du fichier de configuration à partir duquel les métadonnées de point de référence seront importées.

</dd> <dt>

*RuntimeStateFilePath* \[ dans\]
</dt> <dd>

Chemin d’accès qualifié complet du fichier d’état d’exécution à partir duquel les métadonnées de point de référence seront importées.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone. Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 (aucune erreur) ou l’un des messages d’erreur suivants :

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
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
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




