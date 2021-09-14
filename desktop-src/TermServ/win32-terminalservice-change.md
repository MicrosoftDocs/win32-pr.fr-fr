---
title: Modifier la méthode de la classe Win32_Service (Mbnapi. h) (TerminalService)
description: Modifie un TerminalService Win32 \_ .
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode de modification
- Services Bureau à distance de la méthode de modification, classe Win32_Service
- Services Bureau à distance de la classe Win32_Service, méthode change
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856804"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a>Méthode change de la classe Win32_Service (Mbnapi. h)-TerminalService

La méthode **change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifie un [**\_ TerminalService Win32**](win32-terminalservice.md).

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DisplayName* \[ dans\]
</dt> <dd>

Nom d’affichage du service. Cette chaîne a une longueur maximale de 256 caractères. Le nom est conservé dans le gestionnaire de contrôle des services. Les comparaisons *DisplayName* ne respectent jamais la casse.

Contraintes : accepte la même valeur que la propriété **Name** .

Exemple : « Atdisk ».

</dd> <dt>

*Nom du chemin* \[ dans\]
</dt> <dd>

Le chemin d’accès complet au fichier exécutable qui implémente le service, par exemple, « \\ racine_système \\ system32 \\ drivers \\afd.sys ».

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

0
</dt> <dd>

**Ignorer**. Le démarrage se poursuit. Aucune notification n’est donnée à l’utilisateur en raison de l’échec du service.

</dd> <dt>

1
</dt> <dd>

**Normal.** Le démarrage se poursuit. Avant que l’utilisateur ouvre une session, l’utilisateur reçoit la notification « au moins un service ou un périphérique a échoué au démarrage ».

</dd> <dt>

2
</dt> <dd>

**Sérieux.** L’ordinateur tente de redémarrer avec la dernière bonne configuration connue. Si le service échoue à nouveau, le démarrage se poursuit et la notification est donnée à l’utilisateur.

</dd> <dt>

3
</dt> <dd>

**Critique.** L’ordinateur tente de redémarrer avec la dernière bonne configuration connue. Si le service échoue à nouveau, le démarrage s’arrête.

</dd> </dl> </dd> <dt>

*StartMode* \[ dans\]
</dt> <dd>

mode de démarrage du service de base Windows. Pour plus d'informations, consultez la section Notes.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Partition**


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Requise**


</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique**


</dt> <dd>

Le service est démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système. Les services de démarrage automatique démarrent avant qu’un utilisateur ouvre une session sur l’ordinateur et s’exécute même si aucun utilisateur ne se connecte à l’ordinateur.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuelle**


</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](win32-terminalservice-startservice.md) . Bien que les services manuels doivent être démarrés spécifiquement par un utilisateur (ou par un script), ils continuent à s’exécuter même si l’utilisateur se déconnecte. Les services manuels sont souvent appelés services à la demande.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**


</dt> <dd>

Service qui ne peut plus être démarré. Pour démarrer un service désactivé, vous devez d’abord définir l’option de démarrage sur automatique ou manuel.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le service peut créer ou communiquer avec une fenêtre sur le bureau.

</dd> <dt>

*StartName* \[ dans\]
</dt> <dd>

Nom du compte sous lequel le service s’exécute. Selon le type de service, le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur ou. \\ Nom d’utilisateur. Le processus de service sera journalisé à l’aide de l’une de ces deux formes lorsqu’il s’exécute. Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié. Si **null** est spécifié, le service est connecté en tant que compte LocalSystem. Pour les pilotes au niveau du noyau ou du système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou le \\ pilote \\ XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique. Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service, par exemple, « DWDOM \\ admin ».

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

Nom du groupe auquel il est associé. Les groupes d’ordre de chargement sont contenus dans le registre système et déterminent l’ordre dans lequel les services sont chargés dans le système d’exploitation. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’appartient pas à un groupe. Pour plus d'informations, consultez la section Notes.

Les dépendances entre les groupes doivent être listées dans le paramètre *LoadOrderGroupDependencies* . Les services de la liste de groupes d’ordre de chargement sont démarrés en premier, suivis par des services dans des groupes qui ne figurent pas dans la liste des groupes d’ordre de chargement, suivis par des services qui n’appartiennent pas à un groupe. La liste des groupes d’ordre de chargement se trouve dans le registre système à l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local ServiceGroupOrder

</dd> <dt>

*LoadOrderGroupDependencies* \[ dans\]
</dt> <dd>

Liste des groupes d’ordre de chargement qui doivent démarrer avant le démarrage de ce service. Le tableau se termine par un caractère double **null**. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. Les noms de groupes doivent être préfixés par l' **\_ \_ identificateur de groupe SC** (défini dans le fichier winsvc. h) pour les différencier des noms de service, car les services et les groupes de services partagent le même espace de noms. La dépendance sur un groupe signifie que ce service peut s’exécuter si au moins un membre du groupe est en cours d’exécution après une tentative de démarrage de tous les membres du groupe.

</dd> <dt>

*ServiceDependencies* \[ dans\]
</dt> <dd>

Liste qui contient les noms des services qui doivent démarrer avant le démarrage de ce service. Le tableau se termine par un caractère double **null**. Si le pointeur a la **valeur null**, ou s’il pointe vers une chaîne vide, le service n’a pas de dépendances. La dépendance sur un service indique que ce service ne peut s’exécuter que si le service dont il dépend est en cours d’exécution.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur. Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).

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

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**** La propriété State) est égale à 0, 1 ou 2.

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

## <a name="remarks"></a>Notes

Lorsqu’un ordinateur démarre, tous les services de démarrage automatique démarrent également. Il peut arriver que l’un de ces services ne puisse pas démarrer avec l’ordinateur. Lorsqu’un service échoue pendant le démarrage du système, l’ordinateur effectue une action en fonction de la valeur du code de contrôle d’erreur du service.

la plupart des services sont installés à l’aide du code de contrôle d’erreur normal. Quelques-unes des exceptions, qui sont installées à l’aide du code d’erreur ignorer, sont les suivantes :

-   Service de réplication de fichiers
-   Carte à puce
-   Ouverture de session secondaire
-   WMI

Pour les services installés à l’aide du code d’erreur ignorer, aucune notification n’est donnée à l’utilisateur pour lequel le service a échoué. Si vous préférez que la notification à l’écran indique qu’un service n’a pas pu démarrer, vous pouvez utiliser WMI pour modifier le code de contrôle de l’erreur. Les codes de contrôle d’erreur s’appliquent uniquement au démarrage de l’ordinateur. les codes de contrôle d’erreur ne sont pas utilisés si vous arrêtez, puis essayez de redémarrer un service une fois que l’ordinateur est en cours d’exécution.

Parfois, vous devrez peut-être modifier le compte sous lequel un service donné s’exécute. Par exemple, vous pouvez exécuter un service sous un compte d’administration. Étant donné que cela peut créer une faille de sécurité, vous pouvez basculer le service vers un compte avec moins de privilèges. Vous pouvez également faire en sorte que les services s’exécutent sous un compte qui est sur le lieu d’être supprimé, ou que vous souhaitiez vous assurer que certains services s’exécutent sous certains comptes sur tous vos serveurs. Vous pouvez utiliser la méthode **change** de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) pour configurer les services à exécuter sous un compte d’utilisateur spécifié. Lorsque vous sélectionnez un compte, gardez à l’esprit les points suivants :

-   Le compte utilisé en tant que compte de service doit avoir le droit d’ouvrir une session en tant que service. Ce droit peut être accordé à l’aide de stratégie de groupe.
-   Le compte utilisé en tant que compte de service ne doit pas être membre d’un groupe local, d’un domaine ou d’un groupe administrateurs d’entreprise.
-   Chaque instance d’un service doit s’exécuter sous un compte d’utilisateur unique. Cela offre une sécurité supplémentaire et permet d’auditer des instances de service individuelles.
-   Si le service est interactif, le service doit s’exécuter sous le compte LocalSystem.

    LocalSystem est requis car une seule station Windows (WinSta0) peut être visible et interactive à la fois. Si un service s’exécute sous un compte autre que LocalSystem, il s’exécute dans la \\ station Windows par défaut du service 0x03e7, qui est une fenêtre invisible. Les services qui s’exécutent dans cette station Windows ne peuvent pas recevoir de sortie d’entrée ou d’affichage.

Lorsque vous affectez un compte à un service, le SCM requiert le mot de passe correct pour ce compte avant de procéder à l’attribution. Si vous fournissez un mot de passe incorrect, le SCM rejette le compte. Si vous configurez un compte de service à l’aide du compte LocalSystem, LocalService ou NetworkService, vous n’avez pas besoin de fournir un mot de passe de compte, car ces comptes n’ont pas de mot de passe.

Le SCM stocke le mot de passe du compte dans la base de données de services. Toutefois, une fois le mot de passe affecté, le SCM ne garantit pas que le mot de passe stocké dans la base de données de services et le mot de passe attribué au compte d’utilisateur dans Active Directory continuent de correspondre. Par conséquent, une situation semblable à la suivante peut se produire :

-   . Vous configurez un service pour qu’il s’exécute sous un compte d’utilisateur particulier.
-   Le service démarre sous ce compte à l’aide du mot de passe du compte actuel.
-   Vous modifiez le mot de passe du compte d’utilisateur.
-   Le service continue à s’exécuter. Toutefois, si le service s’arrête, vous ne pouvez pas le redémarrer, car le SCM continue à utiliser l’ancien mot de passe non valide. La modification du mot de passe dans Active Directory ne modifie pas le mot de passe stocké dans la base de données de services.

Si vous exécutez des services sous des comptes d’utilisateur standard, vous devez mettre à jour ces mots de passe de service chaque fois que le mot de passe du compte d’utilisateur est modifié. Cela peut s’avérer particulièrement long si vous ne savez pas quels services s’exécutent sous ce compte ou quels sont les ordinateurs qui exécutent les services sous ce compte. Heureusement, vous pouvez utiliser WMI pour vérifier les comptes de service sur tous vos ordinateurs et, si nécessaire, modifier le mot de passe du compte de service.

Le [**paramètre \_ LoadOrderGroup Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) représente un groupe de services système qui définissent des dépendances d’exécution. Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres. Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.

Pour modifier un service d’un service réseau en système local, les paramètres *StartName* et *StartPassword* doivent avoir les valeurs suivantes :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Pour modifier un service d’un service système local sur un réseau, les paramètres *StartName* et *StartPassword* doivent avoir les valeurs suivantes :


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Exemples

Le code VBScript suivant modifie le compte de service pour les services qui s’exécutent sous un compte d’utilisateur spécifié sur LocalSystem.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



Le script VBScript suivant modifie le mot de passe du compte de service pour tous les scripts exécutés sous netsvc


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
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

 

