---
description: Modifie un service Win32 \_ .
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Modifier la méthode de la classe Win32_Service (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414016"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a>Modifier la méthode de la classe Win32_Service (Mbnapi. h)

La méthode de la classe **change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifie [**un \_ service Win32**](win32-service.md).

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
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
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

mode de démarrage du service de base Windows. Pour plus d'informations, consultez la section Notes.

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

Manuel
</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) .

</dd> <dt>

Désactivé
</dt> <dd>

Service qui ne peut plus être démarré.

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

**Success**
</dt> <dd>

0

La demande a été acceptée.

</dd> <dt>

**Non pris en charge**
</dt> <dd>

1

La demande n'est pas prise en charge.

</dd> <dt>

**Accès refusé**
</dt> <dd>

2

L’utilisateur n’a pas l’accès nécessaire.

</dd> <dt>

**Services dépendants en cours d’exécution**
</dt> <dd>

3

Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.

</dd> <dt>

**Contrôle de service non valide**
</dt> <dd>

4

Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.

</dd> <dt>

**Le service ne peut pas accepter le contrôle**
</dt> <dd>

5

Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).**** La propriété State) est égale à 0, 1 ou 2.

</dd> <dt>

**Service non actif**
</dt> <dd>

6

Le service n'a pas été démarré.

</dd> <dt>

**Délai d’expiration de la demande de service**
</dt> <dd>

7

Le service n'a pas répondu à la demande de démarrage en temps voulu.

</dd> <dt>

**Échec inconnu**
</dt> <dd>

8

Échec inconnu lors du démarrage du service.

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

Une dépendance sur laquelle repose ce service a été supprimée du système.

</dd> <dt>

**Échec de la dépendance du service**
</dt> <dd>

13

Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.

</dd> <dt>

**Service désactivé**
</dt> <dd>

14

Le service a été désactivé du système.

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

Le service n’a pas de thread d’exécution.

</dd> <dt>

**Dépendance circulaire d’État**
</dt> <dd>

18

Le service a des dépendances circulaires lorsqu’il démarre.

</dd> <dt>

**Nom de l’État en double**
</dt> <dd>

19

Un service est en cours d’exécution sous le même nom.

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

Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.

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

## <a name="remarks"></a>Notes

Lorsqu’un ordinateur démarre, tous les services de démarrage automatique démarrent également. Il peut arriver que l’un de ces services ne puisse pas démarrer avec l’ordinateur. Lorsqu’un service échoue pendant le démarrage du système, l’ordinateur effectue une action en fonction de la valeur du code de contrôle d’erreur du service.

la plupart des services sont installés à l’aide du code de contrôle d’erreur normal. Quelques-unes des exceptions, qui sont installées à l’aide du code d’erreur ignorer, sont les suivantes :

-   Service de réplication de fichiers
-   Carte à puce
-   Ouverture de session secondaire
-   WMI

Pour les services installés à l’aide du code d’erreur ignorer, aucune notification n’est donnée à l’utilisateur pour lequel le service a échoué. Si vous préférez que la notification à l’écran indique qu’un service n’a pas pu démarrer, vous pouvez utiliser WMI pour modifier le code de contrôle de l’erreur. Les codes de contrôle d’erreur s’appliquent uniquement au démarrage de l’ordinateur. les codes de contrôle d’erreur ne sont pas utilisés si vous arrêtez, puis essayez de redémarrer un service une fois que l’ordinateur est en cours d’exécution.

Parfois, vous devrez peut-être modifier le compte sous lequel un service donné s’exécute. Par exemple, vous pouvez exécuter un service sous un compte d’administration. Étant donné que cela peut créer une faille de sécurité, vous pouvez basculer le service vers un compte avec moins de privilèges. Vous pouvez également faire en sorte que les services s’exécutent sous un compte qui est sur le lieu d’être supprimé, ou que vous souhaitiez vous assurer que certains services s’exécutent sous certains comptes sur tous vos serveurs. Vous pouvez utiliser la méthode **change** de la classe de [**\_ service Win32**](win32-service.md) pour configurer des services à exécuter sous un compte d’utilisateur spécifié. Lorsque vous sélectionnez un compte, gardez à l’esprit les points suivants :

-   Le compte utilisé en tant que compte de service doit avoir le droit d’ouvrir une session en tant que service. Ce droit peut être accordé à l’aide de stratégie de groupe.
-   Le compte utilisé en tant que compte de service ne doit pas être membre d’un groupe local, d’un domaine ou d’un groupe administrateurs d’entreprise.
-   Chaque instance d’un service doit s’exécuter sous un compte d’utilisateur unique. Cela offre une sécurité supplémentaire et permet d’auditer des instances de service individuelles.
-   Si le service est interactif, le service doit s’exécuter sous le compte LocalSystem.

    LocalSystem est requis car une seule station Windows (WinSta0) peut être visible et interactive à la fois. Si un service s’exécute sous un compte autre que LocalSystem, il s’exécute dans la \\ station Windows par défaut du service 0x03e7, qui est une fenêtre invisible. Les services qui s’exécutent dans cette station Windows ne peuvent pas recevoir de sortie d’entrée ou d’affichage.

Lorsque vous affectez un compte à un service, le SCM requiert le mot de passe correct pour ce compte avant de procéder à l’attribution. Si vous fournissez un mot de passe incorrect, le SCM rejette le compte. Si vous configurez un compte de service à l’aide du compte LocalSystem, LocalService ou NetworkService, vous n’avez pas besoin de fournir un mot de passe de compte, car ces comptes n’ont pas de mot de passe.

Le SCM stocke le mot de passe du compte dans la base de données de services. Toutefois, une fois le mot de passe affecté, le SCM ne garantit pas que le mot de passe stocké dans la base de données de services et le mot de passe attribué au compte d’utilisateur dans Active Directory continuent de correspondre. Par conséquent, une situation semblable à la suivante peut se produire :

-   Vous configurez un service pour qu’il s’exécute sous un compte d’utilisateur particulier.
-   Le service démarre sous ce compte à l’aide du mot de passe du compte actuel.
-   Vous modifiez le mot de passe du compte d’utilisateur.
-   Le service continue à s’exécuter. Toutefois, si le service s’arrête, vous ne pouvez pas le redémarrer, car le SCM continue à utiliser l’ancien mot de passe non valide. La modification du mot de passe dans Active Directory ne modifie pas le mot de passe stocké dans la base de données de services.

Si vous exécutez des services sous des comptes d’utilisateur standard, vous devez mettre à jour ces mots de passe de service chaque fois que le mot de passe du compte d’utilisateur est modifié. Cela peut s’avérer particulièrement long si vous ne savez pas quels services s’exécutent sous ce compte ou quels sont les ordinateurs qui exécutent les services sous ce compte. Heureusement, vous pouvez utiliser WMI pour vérifier les comptes de service sur tous vos ordinateurs et, si nécessaire, modifier le mot de passe du compte de service.

Le [**paramètre \_ LoadOrderGroup Win32**](win32-loadordergroup.md) représente un groupe de services système qui définissent des dépendances d’exécution. Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres. Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.

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
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



Le script VBScript suivant modifie le mot de passe du compte de service pour tous les scripts exécutés sous netsvc


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Spécifications



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

[**\_Service Win32**](win32-service.md)
</dt> <dt>

[Tâches WMI : services](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

