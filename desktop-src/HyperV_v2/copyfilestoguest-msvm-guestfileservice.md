---
description: Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Msvm_GuestFileService :: CopyFilesToGuest, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536490"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a>MSVM \_ GuestFileService :: CopyFilesToGuest, méthode

Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CopyFileToGuestSettings* \[ dans\]
</dt> <dd>

Tableau d’instances de la classe [**MSVM \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) qui représente un travail d’opération de service de fichiers invité.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone. Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.

> [!Note]  
> Ce paramètre a été ajouté dans Windows 10.

 

</dd> <dt>

*ParentPools* \[ out, facultatif\]
</dt> <dd>

Tableau facultatif de références [**\_ CopyFileToGuestJob MSVM**](msvm-copyfiletoguestjob.md) utilisées pour surveiller la progression de l’opération. **CopyFilesToGuest** utilise *ParentPools* s’il ne peut pas s’exécuter de façon synchrone. Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.

> [!Note]  
> Ce paramètre a été supprimé dans Windows 10.

 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, retourne 0 ; Sinon, retourne une valeur d’erreur.

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
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ GuestFileService**](msvm-guestfileservice.md)
</dt> </dl>

 

 




