---
description: Modifie un objet de service dérivé de Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Modifier la méthode de la classe Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 306f771df0e44cb11ec61631b2d6b51f11ccefac9a719776d3a483d5cc861133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085829"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Modifier la méthode de la \_ classe BaseService Win32

La méthode de la classe **change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifie un objet de service dérivé de [**Win32 \_ BaseService**](win32-baseservice.md). Le [**paramètre \_ LoadOrderGroup Win32**](win32-loadordergroup.md) représente un groupe de services système qui définissent des dépendances d’exécution. Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres. Ces services dépendants requièrent que les services antécédents fonctionnent correctement.

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

Nom complet d’un service. Cette chaîne a une longueur maximale de 256 caractères. Le nom est conservé dans le gestionnaire de contrôle des services. Les comparaisons *DisplayName* ne respectent jamais la casse.

Contraintes : accepte la même valeur que le paramètre *Name* .

Exemple : « Atdisk ».

</dd> <dt>

*Nom du chemin* \[ dans\]
</dt> <dd>

Chemin d’accès qualifié complet au fichier exécutable qui implémente un service.

Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ dans\]
</dt> <dd>

Type de services fourni aux processus qui les appellent.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Pilote de noyau** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Pilote du système de fichiers** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptateur** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Pilote de reconnaissance** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Propre processus** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processus de partage** (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Processus interactif

</dd> </dl> </dd> <dt>

*ErrorControl* \[ dans\]
</dt> <dd>

Gravité d’une erreur si ce service ne démarre pas au démarrage. La valeur indique l’action prise par le programme de démarrage si une défaillance se produit. Le système journalise toutes les erreurs.

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

mode de démarrage du service de base Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Démarrage système** (« système »)


</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)


</dt> <dd>

Service pour démarrer automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)


</dt> <dd>

Service à démarrer par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-baseservice.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")


</dt> <dd>

Service qui ne peut pas être démarré.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le service peut créer ou communiquer avec une fenêtre sur le bureau.

</dd> <dt>

*StartName* \[ dans\]
</dt> <dd>

Nom du compte sous lequel le service s’exécute, qui dépend du type de service. Le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur. Lorsqu’il s’exécute, le processus de service est enregistré à l’aide de l’une des deux formes précédentes. Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié. Si une chaîne vide est spécifiée, le service est connecté en tant que compte LocalSystem. Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote, par exemple, système de \\ fichiers \\ RDR ou \\ pilote \\ XNS, que le système d’entrée et de sortie utilise pour charger le pilote de périphérique. Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, \\ administrateur DWDOM.

Vous pouvez également utiliser le format UPN (user principal name) pour spécifier le **StartName**, par exemple, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ dans\]
</dt> <dd>

Mot de passe du nom de compte que le paramètre *StartName* spécifie. Spécifiez **null** lorsque vous ne modifiez pas le mot de passe. Spécifiez une chaîne vide si le service n’a pas de mot de passe.

> [!Note]  
> Lorsque vous modifiez un service de système local en réseau ou de réseau à système local, *StartPassword* doit être une chaîne vide ("") et non **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ dans\]
</dt> <dd>

Nom du groupe auquel il est associé. Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent la séquence de chargement des services dans un système d’exploitation. Si le pointeur est **null** ou pointe vers une chaîne vide, le service n’appartient pas à un groupe. Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* . Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe. Le registre système contient une liste de groupes d’ordre de chargement situés dans **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.

</dd> <dt>

*LoadOrderGroupDependencies* \[ dans\]
</dt> <dd>

Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service. Le tableau se termine par un caractère double **null**. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms. La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.

</dd> <dt>

*ServiceDependencies* \[ dans\]
</dt> <dd>

Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service. Le tableau se termine par un caractère double **null**. Si le pointeur est **null** ou pointe vers une chaîne vide, le service n’a pas de dépendances. La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.

<dl> <dt>

**Success**
</dt> <dd>

0

La demande est acceptée.

</dd> <dt>

**Non pris en charge**
</dt> <dd>

1

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur ne dispose pas des privilèges d’accès nécessaires.

</dd> <dt>

**Services dépendants en cours d’exécution**
</dt> <dd>

3

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>

**Contrôle de service non valide**
</dt> <dd>

4

Le code de contrôle demandé n’est pas valide ou n’est pas acceptable pour le service.

</dd> <dt>

**Le service ne peut pas accepter le contrôle**
</dt> <dd>

5

Le code de contrôle demandé ne peut pas être envoyé au service, car la propriété d' [**État**](win32-baseservice.md) de l’objet [**\_ BaseService Win32**](win32-baseservice.md) est égale à 0, 1 ou 2.

</dd> <dt>

**Service non actif**
</dt> <dd>

6

Le service n'a pas été démarré.

</dd> <dt>

**Délai d’expiration de la demande de service**
</dt> <dd>

7

Le service ne répond pas rapidement à la demande de démarrage.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Processus interactif.

</dd> <dt>

**Chemin introuvable**
</dt> <dd>

9

Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.

</dd> <dt>

**Service déjà en cours d’exécution**
</dt> <dd>

10

Le service est déjà en cours d'exécution.

</dd> <dt>

**Base de données du service verrouillée**
</dt> <dd>

11

La base de données pour ajouter un nouveau service est verrouillée.

</dd> <dt>

**Dépendance de service supprimée**
</dt> <dd>

12

Une dépendance sur laquelle ce service repose est supprimée du système.

</dd> <dt>

**Échec de la dépendance du service**
</dt> <dd>

13

Le service ne trouve pas le service nécessaire à partir d’un service dépendant.

</dd> <dt>

**Service désactivé**
</dt> <dd>

14

Le service est désactivé du système.

</dd> <dt>

**Échec de l’ouverture de session du service**
</dt> <dd>

15

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>

**Service marqué pour suppression**
</dt> <dd>

16

Ce service est en cours de suppression du système.

</dd> <dt>

**Service sans thread**
</dt> <dd>

17

Il n'y a pas de thread d'exécution pour le service.

</dd> <dt>

**Dépendance circulaire d’État**
</dt> <dd>

18

Le démarrage du service donne lieu à des dépendances circulaires.

</dd> <dt>

**Nom de l’État en double**
</dt> <dd>

19

Un service est en cours d'exécution sous le même nom.

</dd> <dt>

**Nom de l’état non valide**
</dt> <dd>

20

Le nom du service contient des caractères non valides.

</dd> <dt>

**Paramètre d’État non valide**
</dt> <dd>

21

Des paramètres non valides ont été transmis au service.

</dd> <dt>

**Compte de service de l’état non valide**
</dt> <dd>

22

Le compte pour lequel ce service doit être exécuté n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>

**Le service d’État existe**
</dt> <dd>

23

Le service existe dans la base de données des services disponibles dans le système.

</dd> <dt>

**Service déjà suspendu**
</dt> <dd>

24

Le service est actuellement mis en pause dans le système.

</dd> <dt>

**Autres**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour modifier un service d’un réseau en un système local, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Pour modifier un service d’un système local en réseau, utilisez les valeurs suivantes pour les paramètres *StartName* et *StartPassword* :


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

[**\_BaseService Win32**](win32-baseservice.md)
</dt> </dl>

 

