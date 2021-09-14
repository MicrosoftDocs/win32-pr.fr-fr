---
description: Modifie le mode de démarrage d’un \_ service SystemDriver Win32.
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Méthode ChangeStartMode de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: edb6dfc9d745f5e408871246b581e6fab7eb72d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007047"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>Méthode ChangeStartMode de la \_ classe Win32 SystemDriver

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifie le mode de démarrage d’un service [**\_ SystemDriver Win32**](win32-systemdriver.md) .

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StartMode* \[ dans\]
</dt> <dd>

mode de démarrage du service de base Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)


</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)


</dt> <dd>

Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)


</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")


</dt> <dd>

Service qui ne peut plus être démarré.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur 0 (zéro) si le service a été correctement modifié, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Accès refusé** (2)
</dt> <dt>

**Services dépendants en cours d’exécution** (3)
</dt> <dt>

**Contrôle de service non valide** (4)
</dt> <dt>

**Le service ne peut pas accepter le contrôle** (5)
</dt> <dt>

**Service non actif** (6)
</dt> <dt>

**Délai d’expiration** de la demande de service (7)
</dt> <dt>

**Échec inconnu** (8)
</dt> <dt>

**Chemin introuvable** (9)
</dt> <dt>

**Service déjà en cours d’exécution** (10)
</dt> <dt>

**Base de données de service verrouillée** (11)
</dt> <dt>

**Dépendance de service supprimée** (12)
</dt> <dt>

**Échec** de la dépendance du service (13)
</dt> <dt>

**Service désactivé** (14)
</dt> <dt>

**Échec** de l’ouverture de session du service (15)
</dt> <dt>

**Service marqué pour suppression** (16)
</dt> <dt>

**Service sans thread** (17)
</dt> <dt>

**Dépendance circulaire d’État** (18)
</dt> <dt>

**Nom de l’État en double** (19)
</dt> <dt>

**Nom de l’état non valide** (20)
</dt> <dt>

**Paramètre d’État non valide** (21)
</dt> <dt>

**Compte de service de l’état non valide** (22)
</dt> <dt>

Le **service d’État existe** (23)
</dt> <dt>

**Service déjà suspendu** (24)
</dt> <dt>

**Autre** (25 4294967295)
</dt> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

