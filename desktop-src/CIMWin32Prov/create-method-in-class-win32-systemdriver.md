---
description: Crée un nouveau service géré par le pilote système.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85b18a04672f63c4f1fd8fe4fa386ffb4e3094e817b53a20af9887a84748a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080153"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Créer une méthode de la \_ classe SystemDriver Win32

La méthode **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) crée un nouveau service géré par le pilote système. Le *paramètre \_ LoadOrderGroup Win32* représente un regroupement de services système définissant les dépendances d’exécution. Les services doivent être lancés dans l’ordre spécifié par le groupe d’ordre de chargement, car les services dépendent les uns des autres. Ces services dépendants requièrent la présence des services antécédents pour fonctionner correctement.

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

Nom du service à installer dans la méthode **Create** . La longueur de chaîne maximale est de 256 caractères. La base de données du gestionnaire de contrôle des services conserve la casse des caractères, mais les comparaisons de noms de services ne respectent jamais la casse. Les barres obliques inverses (/) et les barres obliques inverses ( \\ ) sont des caractères de nom de service non valides.

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

Gravité de l’erreur en cas d’échec du démarrage de la méthode **Create** . Cette valeur indique l’action entreprise par le programme de démarrage en cas d’échec. Toutes les erreurs sont consignées par le système.

<dt>

0
</dt> <dd>

Tenir

L'utilisateur n'est pas notifié.

</dd> <dt>

1
</dt> <dd>

"Normal"

L'utilisateur est notifié.

</dd> <dt>

2
</dt> <dd>

Sérieux

Le système est redémarré avec la dernière bonne configuration connue.

</dd> <dt>

3
</dt> <dd>

Critique

Le système tente de démarrer avec une bonne configuration.

</dd> </dl> </dd> <dt>

*StartMode* \[ dans\]
</dt> <dd>

mode de démarrage du service de base Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Partition**


</dt> <dd>

Pilote de périphérique Démarré par le chargeur du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Requise**


</dt> <dd>

Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation. Cette valeur est uniquement valide pour les services de pilote.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique**


</dt> <dd>

Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuelle**


</dt> <dd>

Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**


</dt> <dd>

Service qui ne peut plus être démarré.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ dans\]
</dt> <dd>

Si la **valeur est true**, le service peut créer ou communiquer avec les fenêtres sur le bureau.

</dd> <dt>

*StartName* \[ dans\]
</dt> <dd>

Nom du compte sous lequel le service s’exécute. Selon le type de service, le nom du compte peut être au \\ format nom_domaine nom_utilisateur ou UPN (user principal name) ( Username@DomainName ). Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute. Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié. Si **null** est spécifié, le service est connecté en tant que compte LocalSystem. Pour un noyau ou des pilotes de niveau système, *StartName* contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou le \\ pilote \\ XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique. Si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.

Exemple : DWDOM \\ admin

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

Retourne la valeur 0 (zéro) si le service a été créé avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.

## <a name="requirements"></a>Configuration requise



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

 

