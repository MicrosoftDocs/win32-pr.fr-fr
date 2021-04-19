---
description: Lance une opération de redémarrage du système d’exploitation sur l’ordinateur virtuel enfant associé.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Méthode InitiateReboot de la classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533612"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>Méthode InitiateReboot de la \_ classe ShutdownComponent MSVM

Lance une opération de redémarrage du système d’exploitation sur l’ordinateur virtuel enfant associé.

Si la valeur zéro (0) est retournée, le redémarrage a été lancé avec succès. Tout autre code de retour indique une condition d’erreur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Force* \[ dans\]
</dt> <dd>

Indicateur qui, si la valeur est TRUE, force la fermeture des applications malgré la non-enregistrement des données.

</dd> <dt>

*Raison* \[ dans\]
</dt> <dd>

Raison de l’opération de redémarrage. Il s’agit d’une chaîne définie par l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l'une des valeurs suivantes :

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
</dt> <dt>

**Le système n’est pas prêt** (32780)
</dt> <dt>

**L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option force** (32781)
</dt> <dt>

**Un arrêt système est en cours** (32782)
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

[**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




