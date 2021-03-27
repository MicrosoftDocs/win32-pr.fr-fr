---
description: Cette classe est la classe parente pour les événements de configuration matérielle. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: SystemConfig, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3332d396005deb2fb811d101a99827544ebc6df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869289"
---
# <a name="systemconfig-class"></a>SystemConfig, classe

Cette classe est la classe parente pour les événements de configuration matérielle.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **SystemConfig** ne définit aucun membre.

## <a name="remarks"></a>Notes

Ces événements fournissent la configuration matérielle de l’ordinateur. Contrairement aux autres événements de journalisation de noyau NT, la session de noyau génère automatiquement des événements de configuration matérielle. vous n’activez pas ces événements lors du démarrage de la session du journal de noyau NT.

Pour les événements de configuration matérielle sur Windows XP, consultez la classe [HWConfig](hwconfig.md) .

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements de configuration matérielle en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez les types d’événements suivants pour identifier l’événement de configuration matérielle réel lors de l’utilisation d’événements.



| Type d'événement                                                                      | Description                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ \_ \_ Configuration \_ du type de suivi processeur**(la valeur du type d’événement est 10)<br/>          | Événement de configuration de l’UC. Les classes MOF de l' [**\_ UC SystemConfig**](systemconfig-cpu.md) définissent les données d’événement pour cet événement.                                                       |
| **Événement \_ Type de TRACE \_ \_ configuration \_ IDECHANNEL**(la valeur type d’événement est 23)<br/>   | Événement de configuration de canal IDE principal et secondaire. La classe MOF des classes MOF [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) définit les données d’événement pour cet événement. |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ IRQ**(la valeur du type d’événement est 21)<br/>          | Événement de requête d’interruption (IRQ). La classe MOF des classes MOF [**SystemConfig \_ IRQ**](systemconfig-irq.md) définit les données d’événement pour cet événement.                                       |
| **Événement \_ \_Type de \_ trace \_ disque logique**(la valeur du type d’événement est 12)<br/>  | Événement de configuration de disque logique. La classe MOF des classes MOF [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) définit les données d’événement pour cet événement.                            |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ NetInfo**(la valeur du type d’événement est 17)<br/>      | Événement réseau iformation. La classe MOF du [**\_ réseau SystemConfig**](systemconfig-network.md) définit les données d’événement pour cet événement.                                                |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ carte réseau**(la valeur du type d’événement est 13)<br/>          | Événement de configuration de la carte réseau. Les classes SystemConfig de la [**\_ carte d’interface réseau de l’interface réseau**](systemconfig-nic.md) définissent les données d’événement pour cet événement.                                                       |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ PHYSICALDISK**(la valeur du type d’événement est 11)<br/> | Événement de configuration de disque physique. Les classes [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) MOF définissent les données d’événement pour cet événement.                                     |
| **Événement \_ Configuration du type de TRACE \_ \_ \_ PNP**(la valeur du type d’événement est 22)<br/>          | Événement Plug-and-Play. La classe MOF des classes MOF [**SystemConfig \_ PNP**](systemconfig-pnp.md) définit les données d’événement pour cet événement.                                                 |
| **Événement \_ \_Mise en \_ \_ marche** de la configuration du type de trace (la valeur du type d’événement est 16)<br/>        | Événement de configuration de l’alimentation. La classe [**SystemConfig \_ Power**](systemconfig-power.md) MOF définit les données d’événement pour cet événement.                                                   |
| **Événement \_ \_Services de \_ configuration \_ du type de trace**(la valeur du type d’événement est 15)<br/>     | Événement de configuration des services. La classe MOF des [**\_ services SystemConfig**](systemconfig-services.md) définit les données d’événement pour cet événement.                                          |
| **Événement \_ \_Vidéo de \_ configuration \_ du type de trace**(la valeur du type d’événement est 14)<br/>        | Événement de configuration de la carte graphique. La classe MOF [**\_ Video SystemConfig**](systemconfig-video.md) définit les données d’événement pour cet événement.                                        |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_Processeur SystemConfig**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ IRQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**\_Réseau SystemConfig**](systemconfig-network.md)
</dt> <dt>

[**\_Carte réseau SystemConfig**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**\_PNP SystemConfig**](systemconfig-pnp.md)
</dt> <dt>

[**SystemConfig \_**](systemconfig-power.md)
</dt> <dt>

[**\_Services SystemConfig**](systemconfig-services.md)
</dt> <dt>

[**\_Vidéo SystemConfig**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 
