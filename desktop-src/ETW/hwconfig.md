---
description: la classe HWConfig est la classe parente pour les événements de configuration matérielle sur Windows XP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: HWConfig, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1d4b8f69784729ffe5d51f3068b03fc0b4154182b2d05f2896e4556a05f7eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394679"
---
# <a name="hwconfig-class"></a>HWConfig, classe

la classe **HWConfig** est la classe parente pour les événements de configuration matérielle sur Windows XP.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **HWConfig** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Ces événements fournissent la configuration matérielle de l’ordinateur. Contrairement aux autres événements de journalisation de noyau NT, la session de noyau génère automatiquement des événements de configuration matérielle. vous n’activez pas ces événements lors du démarrage de la session du journal de noyau NT.

**Windows 2000 :** Non pris en charge.

pour les événements de configuration matérielle sur Windows Vista et Windows Server 2003, consultez la classe [SystemConfig](systemconfig.md) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de configuration matérielle en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement de configuration matérielle réel lors de l’utilisation d’événements.



| Type d'événement                                                                      | Description                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ \_ \_ Configuration \_ du type de suivi processeur**(la valeur du type d’événement est 10)<br/>          | Événement de configuration de l’UC. Les classes MOF de l' [**\_ UC HWConfig**](hwconfig-cpu.md) définissent les données d’événement pour cet événement.                            |
| **Événement \_ \_Type de \_ trace \_ disque logique**(la valeur du type d’événement est 12)<br/>  | Événement de configuration de disque logique. La classe MOF des classes MOF [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) définit les données d’événement pour cet événement. |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ carte réseau**(la valeur du type d’événement est 13)<br/>          | Événement de configuration de la carte réseau. Les classes HWConfig de la [**\_ carte d’interface réseau de l’interface réseau**](hwconfig-nic.md) définissent les données d’événement pour cet événement.                            |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ PHYSICALDISK**(la valeur du type d’événement est 11)<br/> | Événement de configuration de disque physique. Les classes [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF définissent les données d’événement pour cet événement.          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_Processeur HWConfig**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**\_Carte réseau HWConfig**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
