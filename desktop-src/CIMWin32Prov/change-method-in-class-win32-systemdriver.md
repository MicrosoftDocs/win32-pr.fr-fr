---
description: Modifie un \_ service SystemDriver Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Modifier la méthode de la classe Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483561"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Modifier la méthode de la \_ classe SystemDriver Win32

La méthode **change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifie un service [**\_ SystemDriver Win32**](win32-systemdriver.md) . Le [**paramètre \_ LoadOrderGroup Win32**](win32-loadordergroup.md) représente un regroupement de services système définissant les dépendances d’exécution. Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres. Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DisplayName* \[ dans\]
</dt> <dd>

Nom d’affichage du service. Cette chaîne a une longueur maximale de 256 caractères. Le nom est conservé dans le gestionnaire de contrôle des services. Les comparaisons *DisplayName* ne respectent jamais la casse.

Contraintes : accepte la même valeur que le paramètre *Name* .

Exemple : « Atdisk »

</dd> <dt>

*Nom du chemin* \[ dans\]
</dt> <dd>

Chemin d’accès qualifié complet au fichier exécutable qui implémente le service.

Exemple : *\\ racine_système \\ System32 \\ drivers \\afd.sys*

</dd> <dt>

*ServiceType* \[ dans\]
</dt> <dd>

Type des services fournis aux processus qui les appellent.

<dt>

1 (0x1)
</dt> <dd>

Pilote du noyau

</dd> <dt>

2 (0X2)
</dt> <dd>

Pilote du système de fichiers

</dd> <dt>

4 (0x4)
</dt> <dd>

Adaptateur

</dd> <dt>

8 (0x8)
</dt> <dd>

Pilote de reconnaissance

</dd> <dt>

16 (0x10)
</dt> <dd>

Propre processus

</dd> <dt>

32 (0x20)
</dt> <dd>

Processus de partage

</dd> <dt>

256 (0x100)
</dt> <dd>

Processus interactif

</dd> </dl> </dd> <dt>

*ErrorControl* \[ dans\]
</dt> <dd>

Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage. La valeur indique l’action entreprise par le programme de démarrage en cas d’échec. Toutes les erreurs sont consignées par le système.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** (0)


</dt> <dd>

L'utilisateur n'est pas notifié.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

Normal. L'utilisateur est notifié.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)


</dt> <dd>

Le système est redémarré avec la dernière bonne configuration.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (3)


</dt> <dd>

Le système tente de redémarrer avec une bonne configuration.

</dd> </dl> </dd> <dt>

*StartMode* \[ dans\]
</dt> <dd>

Mode de démarrage du service de base Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Démarrage du démarrage**


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Démarrage du démarrage**


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Démarrage du système**


</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique**


</dt> <dd>

Service pour démarrer automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande**


</dt> <dd>

Service à démarrer par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**


</dt> <dd>

Service qui ne peut pas être démarré.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ dans\]
</dt> <dd>

Valeur qui, si la valeur est **true**, le service peut créer ou communiquer avec les fenêtres sur le bureau.

</dd> <dt>

*StartName* \[ dans\]
</dt> <dd>

Nom du compte sous lequel le service s’exécute. Selon le type de service, le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur. Lorsqu’il s’exécute, le processus de service est enregistré à l’aide de l’une de ces deux formes. Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié. Si une chaîne vide est spécifiée, le service est connecté en tant que compte LocalSystem. Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote, par exemple, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS), que le système d’entrée et de sortie (e/s) utilise pour charger le pilote de périphérique. Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, \\ administrateur DWDOM.

Vous pouvez également utiliser le format UPN (user principal name) pour spécifier le **StartName**, par exemple, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ dans\]
</dt> <dd>

Mot de passe du nom de compte spécifié par le paramètre *StartName* . Spécifiez **null** si vous ne modifiez pas le mot de passe. Spécifiez une chaîne vide si le service ne possède pas de mot de passe.

> [!Note]  
> Lorsque vous modifiez un service d’un système local à un réseau ou d’un réseau à un système local, *StartPassword* doit être une chaîne vide ("") et non **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ dans\]
</dt> <dd>

Nom du groupe auquel il est associé. Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe. Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* . Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe. La liste des groupes d’ordre de chargement se trouve dans le registre système à l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder

</dd> <dt>

*LoadOrderGroupDependencies* \[ dans\]
</dt> <dd>

Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service. Le tableau se termine par un caractère double **null**. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier WinSvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms. La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.

</dd> <dt>

*ServiceDependencies* \[ dans\]
</dt> <dd>

Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service. Le tableau se termine par un caractère double **null**. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur zéro (0) si le service a été correctement modifié, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.

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

## <a name="remarks"></a>Notes

Pour modifier un service à partir d’un service réseau sur le système local, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Pour modifier un service d’un service système local en service réseau, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| En-tête<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

