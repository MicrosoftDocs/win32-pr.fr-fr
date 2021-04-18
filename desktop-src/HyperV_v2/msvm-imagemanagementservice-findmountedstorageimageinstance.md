---
description: Recherche un \_ objet MSVM MountedStorageImage pour un chemin d’accès d’image de disque donné.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Méthode FindMountedStorageImageInstance de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526835"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a>Méthode FindMountedStorageImageInstance de la \_ classe ImageManagementService MSVM

Recherche un objet [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) pour un chemin d’accès d’image de disque donné.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SelectionCriterion* \[ dans\]
</dt> <dd>

Chemin d’accès complet qui spécifie l’emplacement d’un fichier image de disque.

</dd> <dt>

*CriterionType* \[ dans\]
</dt> <dd>

Type de critère à rechercher lors de la recherche de l’image de disque.

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

**inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

**Chemin d’accès** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Image* \[ à\]
</dt> <dd>

Référence au [**\_ MountedStorageImage MSVM**](msvm-mountedstorageimage.md) (peut avoir la valeur null si l’image n’est pas montée).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

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
</dt> <dt>

**Fichier introuvable** (32779)
</dt> <dt>

**Objet introuvable** (32789)
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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




