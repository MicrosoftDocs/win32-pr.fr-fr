---
description: Met à jour le nom d’élément de l' \_ objet CIM CollectionOfMSEs spécifié.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Méthode RenameCollection de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867966"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a>Méthode RenameCollection de la \_ classe CollectionManagementService MSVM

Met à jour le nom d’élément de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Collection* \[ dans\]
</dt> <dd>

Collection à renommer.

</dd> <dt>

*NewName* \[ dans\]
</dt> <dd>

Nouveau nom à utiliser.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence au travail (peut avoir la valeur null si la tâche est terminée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, ou 4096 si le travail a démarré ; Sinon, retourne une erreur.

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
</dt> <dt>

**Fichier introuvable** (32779)
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

[**MSVM \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




