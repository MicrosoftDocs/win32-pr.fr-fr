---
title: Créer une méthode de la classe Win32_Service (Services Bureau à distance)
description: 'Créer une méthode de la classe Win32_Service (Services Bureau à distance) : crée un nouveau service système.'
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_Service Class
- Win32_Service de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911ecec0c0ad2cc248bcfdfa2b4e475538d6eff35e8d7bd568df29302b610ee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137882"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a>Créer une méthode de la classe Win32_Service (Services Bureau à distance)

La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau service système.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Create(
  [in] string  Name,
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

*Nom* \[ dans\]
</dt> <dd>

Nom du service à installer dans la méthode **Create** . La longueur de chaîne maximale est de 256 caractères. La base de données du gestionnaire de contrôle des services conserve la casse des caractères, mais les comparaisons de noms de services ne respectent jamais la casse. Les barres obliques inverses (/) et les barres obliques inverses ( \\ \\ ) sont des caractères de nom de service non valides.

</dd> <dt>

*DisplayName* \[ dans\]
</dt> <dd>

Nom complet du service. Cette chaîne a une longueur maximale de 256 caractères. Le nom est conservé dans le gestionnaire de contrôle des services. Les comparaisons *DisplayName* ne respectent jamais la casse.

Contraintes : accepte la même valeur que le paramètre *Name* .

Exemple : « Atdisk ».

</dd> <dt>

*Nom du chemin* \[ dans\]
</dt> <dd>

Chemin d’accès complet au fichier exécutable qui implémente le service.

Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ dans\]
</dt> <dd>

Type de services fourni aux processus qui les appellent.

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

Gravité de l’erreur en cas d’échec du démarrage de la méthode **Create** . La valeur indique l’action entreprise par le programme de démarrage en cas d’échec. Toutes les erreurs sont consignées par le système.

<dt>

0
</dt> <dd>

L'utilisateur n'est pas notifié.

</dd> <dt>

1
</dt> <dd>

L'utilisateur est notifié.

</dd> <dt>

2
</dt> <dd>

Le système est redémarré avec la dernière bonne configuration connue.

</dd> <dt>

3
</dt> <dd>

Le système tente de démarrer avec une bonne configuration.

</dd> </dl> </dd> <dt>

*StartMode* \[ dans\]
</dt> <dd>

mode de démarrage du service de base Windows.

<dt>

Démarrage
</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

Système
</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

Automatique
</dt> <dd>

Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

Manuelle
</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](win32-terminalservice-startservice.md) .

</dd> <dt>

Désactivé
</dt> <dd>

Service qui ne peut plus être démarré.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le service peut créer ou communiquer avec Windows sur le bureau.

</dd> <dt>

*StartName* \[ dans\]
</dt> <dd>

Nom du compte sous lequel le service s’exécute. Selon le type de service, le nom du compte peut être au \\ format nom_domaine nom_utilisateur ou UPN (user principal name) ( Username@DomainName ). Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute. Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié. Si **null** est spécifié, le service est connecté en tant que compte LocalSystem. Pour un noyau ou des pilotes de niveau système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique. Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service. Exemple : DWDOM \\ admin.

</dd> <dt>

*StartPassword* \[ dans\]
</dt> <dd>

Mot de passe du nom de compte spécifié par le paramètre *StartName* . Spécifiez **null** si vous ne modifiez pas le mot de passe. Spécifiez une chaîne vide si le service ne possède pas de mot de passe.

</dd> <dt>

*LoadOrderGroup* \[ dans\]
</dt> <dd>

Nom du groupe associé au nouveau service. Les groupes d’ordre de chargement sont contenus dans le registre et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation. Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe. Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* . Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe. Le registre contient une liste de groupes d’ordre de chargement situés à l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder

</dd> <dt>

*LoadOrderGroupDependencies* \[ dans\]
</dt> <dd>

Tableau des groupes d’ordre de chargement qui doivent démarrer avant ce service. Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** . dans Visual Basic ou un script, vous pouvez transmettre un vbArray. Si le pointeur est **null** ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour le différencier d’un nom de service, car les services et les groupes de services partagent le même espace de noms. La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.

</dd> <dt>

*ServiceDependencies* \[ dans\]
</dt> <dd>

Tableau qui contient les noms des services qui doivent démarrer avant le démarrage de ce service. Chaque élément du tableau est délimité par **null** et la liste se termine par deux valeurs **null** . dans Visual Basic ou un script, vous pouvez transmettre un vbArray. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. La dépendance sur un service signifie que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

La demande a été acceptée.

</dd> <dt>

**1**
</dt> <dd>

La demande n'est pas prise en charge.

</dd> <dt>

**2**
</dt> <dd>

L’utilisateur n’a pas l’accès nécessaire.

</dd> <dt>

**3**
</dt> <dd>

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>

**4**
</dt> <dd>

Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.

</dd> <dt>

**5**
</dt> <dd>

Le code de contrôle demandé ne peut pas être envoyé au service, car l’état du service (propriété **State** de la classe [**\_ BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) est égal à 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

Le service n'a pas été démarré.

</dd> <dt>

**7**
</dt> <dd>

Le service n'a pas répondu à la demande de démarrage en temps voulu.

</dd> <dt>

**8**
</dt> <dd>

Échec inconnu lors du démarrage du service.

</dd> <dt>

**9**
</dt> <dd>

Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.

</dd> <dt>

**10**
</dt> <dd>

Le service est déjà en cours d'exécution.

</dd> <dt>

**11**
</dt> <dd>

La base de données pour ajouter un nouveau service est verrouillée.

</dd> <dt>

**12**
</dt> <dd>

Une dépendance sur laquelle repose ce service a été supprimée du système.

</dd> <dt>

**13**
</dt> <dd>

Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.

</dd> <dt>

**14**
</dt> <dd>

Le service a été désactivé du système.

</dd> <dt>

**15**
</dt> <dd>

Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.

</dd> <dt>

**16**
</dt> <dd>

Ce service est en cours de suppression du système.

</dd> <dt>

**17**
</dt> <dd>

Le service n’a pas de thread d’exécution.

</dd> <dt>

**19**
</dt> <dd>

Le service a des dépendances circulaires lorsqu’il démarre.

</dd> <dt>

**19**
</dt> <dd>

Un service est en cours d’exécution sous le même nom.

</dd> <dt>

**20**
</dt> <dd>

Le nom du service contient des caractères non valides.

</dd> <dt>

**21**
</dt> <dd>

Des paramètres non valides ont été transmis au service.

</dd> <dt>

**22**
</dt> <dd>

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

</dd> <dt>

**23**
</dt> <dd>

Le service existe dans la base de données des services disponibles dans le système.

</dd> <dt>

**24**
</dt> <dd>

Le service est actuellement mis en pause dans le système.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les services sont généralement installés de l’une des deux manières suivantes : dans le cadre de l’installation du système d’exploitation ou à l’aide d’un programme d’installation fourni par le développeur du service. Toutefois, certains services, en particulier ceux créés en interne, peuvent ne pas avoir de programme d’installation. Dans ces instances, vous pouvez utiliser la méthode **Create** pour installer des services par programme.

Malgré le nom, la méthode de création ne crée pas réellement un service ; Il installe simplement un service existant. Pour utiliser cette commande, vous devez copier le fichier exécutable du service sur un ordinateur, puis utiliser **créer** pour installer le service.

La méthode **Create** est semblable à la méthode [**change**](win32-terminalservice-change.md) . Dans les deux cas, les propriétés du service sont passées en tant que paramètres à la méthode. Comme avec les paramètres utilisés avec la méthode **change** , l’ordre dans lequel ces paramètres sont transmis est très important.

Le paramètre *LoadOrderGroup* représente un regroupement de services système définissant les dépendances d’exécution. Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres. Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classes du système d’exploitation](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[Tâches WMI : services](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

