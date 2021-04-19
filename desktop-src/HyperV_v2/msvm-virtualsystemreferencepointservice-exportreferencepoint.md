---
description: Exporte le point de référence du système virtuel.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Méthode ExportReferencePoint de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538432"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Méthode ExportReferencePoint de la \_ classe VirtualSystemReferencePointService MSVM

Exporte le point de référence du système virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ReferencePoint* \[ dans\]
</dt> <dd>

Référence à l’instance [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente le point de référence à exporter.

</dd> <dt>

*ExportDirectory* \[ dans\]
</dt> <dd>

Chemin d’accès complet du répertoire vers lequel le point de référence doit être exporté.

</dd> <dt>

*ExportSettingData* \[ dans\]
</dt> <dd>

Instance de [**MSVM \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone. Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 (terminé sans erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




