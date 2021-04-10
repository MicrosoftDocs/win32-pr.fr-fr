---
description: Enregistre des informations sur l’implémentation physique d’un fournisseur dans WMI. Les fournisseurs qui ne définissent pas la propriété HostingModel sont chargés, par défaut, pour s’exécuter dans un processus Wmiprvse.exe en tant que NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Classe __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952870"
---
# <a name="__win32provider-class"></a>\_\_Win32Provider, classe

La classe système **\_ \_ Win32Provider** inscrit des informations sur l’implémentation physique d’un fournisseur dans WMI. Les fournisseurs qui ne définissent pas la propriété **HostingModel** sont chargés, par défaut, pour s’exécuter dans un processus Wmiprvse.exe en tant que **NetworkServiceHostOrSelfHost**.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ Win32Provider** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ Win32Provider** possède les propriétés suivantes.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur de classe utilisé par WMI pour déterminer s’il faut charger un fournisseur de haute performance dans le processus client ou le processus WMI. Si le fournisseur et le client se trouvent sur le même ordinateur, WMI charge le fournisseur in-process sur le client en utilisant **ClientLoadableCLSID** comme identificateur de classe. Lorsque le fournisseur et le client se trouvent sur des ordinateurs différents, WMI charge le fournisseur in-process dans le processus WMI. WMI utilise également **ClientLoadableCLSID** pour prendre en charge les opérations d’actualisation.

Pour plus d’informations, consultez [inscription d’un fournisseur de High-Performance.](registering-a-high-performance-provider.md)

</dd> <dt>

**IDENTIFICATEUR**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**GUID** qui représente l’identificateur de classe (**CLSID**) de l’objet com du fournisseur. Cet objet COM doit contenir une implémentation de l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .

</dd> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identifie l’ordinateur sur lequel démarrer le fournisseur. Si le fournisseur s’exécute sur l’ordinateur local, il a la **valeur null**.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, cette instance est activée et peut être utilisée pour effectuer les demandes des clients.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Cette propriété est composée de valeurs des propriétés **HostingGroup** et **HostingSpecification** des [**\_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) . La valeur de cette propriété spécifie comment WMI charge le fournisseur et le compte de sécurité sous lequel il s’exécute. Pour plus d’informations sur la définition de la propriété **HostingModel** , consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md) et [inscription d’un fournisseur](registering-a-provider.md).

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Réservé. La valeur par défaut est zéro (0).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Jeu d’indicateurs qui fournissent des informations sur la sérialisation. La valeur par défaut est zéro (0).

<dt>

0
</dt> <dd>

Toute l’initialisation de ce fournisseur doit être sérialisée.

</dd> <dt>

1
</dt> <dd>

Toutes les initialisations de ce fournisseur dans le même espace de noms doivent être sérialisées.

</dd> <dt>

2
</dt> <dd>

Aucune sérialisation d’initialisation n’est nécessaire.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

TBD

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Nom du fournisseur.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur est initialisé pour chaque paramètre régional lorsqu’un utilisateur se connecte à un même espace de noms plusieurs fois à l’aide de différents paramètres régionaux. La valeur par défaut est **FALSE**.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur est initialisé une fois pour chaque utilisateur NT LAN Manager (NTLM) qui effectue des demandes au fournisseur. Si la **valeur est false** (valeur par défaut), le fournisseur est initialisé une fois pour tous les utilisateurs.

</dd> <dt>

**FCP**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur s’engage à préparer le déchargement en appelant [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur tous les points d’interface en attente lorsque WMI appelle la méthode de mise en **version** de son interface principale. Les fournisseurs qui doivent conserver les clients de WMI après qu’ils ne fonctionnent pas comme les fournisseurs doivent définir **pure** sur **false**. Le paramètre par défaut est **true**. Pour plus d’informations, consultez la section Notes de cette rubrique.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Le descripteur de sécurité (SD) dans le langage SDDL (Security Descriptor Definition Language) qui détermine l’ensemble des utilisateurs qui peuvent appeler [**IWbemDecoupledRegistrar : Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) pour le fournisseur découplé. Pour plus d’informations, consultez la rubrique [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language) dans la section sécurité de la SDK Windows. Ce descripteur de sécurité est utilisé uniquement pour les fournisseurs découplés et n’affecte pas les autres fournisseurs. Pour plus d’informations, consultez [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md).

WMI effectue des vérifications d’accès pour les fournisseurs découplés qui utilisent les interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemObjectSink**](iwbemobjectsink.md) . Si le descripteur de sécurité a la **valeur null**, seules les applications ou les services qui s’exécutent sous les comptes LocalSystem, NetworkService et LocalService peuvent exécuter un fournisseur découplé.

La chaîne suivante montre un fournisseur découplé qui doit être exécuté uniquement par des administrateurs intégrés.» O :BAG : BAD : (A ;; 0 x1 ;;; BA)»

Pour plus d’informations sur la définition de la propriété **SecurityDescriptor** , consultez maintenance de la [sécurité WMI](maintaining-wmi-security.md).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

[Format de date et d’heure](date-and-time-format.md) qui spécifie la durée pendant laquelle WMI autorise le fournisseur à rester inactif avant d’être déchargé. En règle générale, les fournisseurs demandent que WMI n’attende pas plus de cinq minutes.

Pour la version actuelle de WMI, la valeur de cette propriété est ignorée. WMI décharge le fournisseur en fonction de la valeur du délai d’attente dans une classe interne de l' \\ espace de noms racine. Il est recommandé que les fournisseurs définissent **UnloadTimeout**. Pour plus d’informations, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Version du fournisseur. Les versions prises en charge sont 1 et 2. La version 2 renforce les contrôles de validité de toutes les inscriptions de propriété associées, en particulier la propriété [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

La classe **\_ \_ Win32Provider** est dérivée du [**\_ \_ fournisseur**](--provider.md).

La plupart des fournisseurs peuvent accepter les valeurs par défaut de la propriété **InitializationReentrancy** . Toutefois, si un fournisseur peut prendre en charge l’initialisation simultanée pour des utilisateurs distincts, cette propriété peut avoir la valeur 1 (un). Si l’initialisation sérialisée est nécessaire, **InitializationReentrancy** reste 0 (zéro). Dans les deux instances, **PerUserInitialization** a la valeur **true**.

Un fournisseur pur ou un fournisseur qui affecte à la propriété **pure** la **valeur true**, existe uniquement pour les demandes de service d’applications et WMI. La plupart des fournisseurs sont des fournisseurs purs. Un fournisseur non pur est l’exception. Les fournisseurs non purs effectuent la transition vers le rôle du client une fois qu’ils ont terminé de traiter les demandes.

Un fournisseur d’émission qui commence à émettre des requêtes et effectue des demandes de WMI une fois l’initialisation terminée est un exemple de fournisseur non pur. Un fournisseur de notifications push n’a pas de responsabilités, sauf pour mettre à jour le référentiel CIM avec des données au moment de l’initialisation. Après la mise à jour du référentiel, un fournisseur d’émission peut attendre le déchargement ou la transition vers le rôle de client. Le fournisseur push qui attend le déchargement est un fournisseur pur. Le fournisseur push qui participe aux activités des clients est non pur.

WMI doit être en mesure de distinguer les fournisseurs purs des fournisseurs non purs afin qu’il puisse déterminer quand il est possible de s’arrêter en toute sécurité. WMI doit attendre la fin de toutes les opérations qui impliquent des fournisseurs non purs avant de pouvoir s’arrêter en toute sécurité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_Fournisseur**](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Inscription d’un fournisseur](registering-a-provider.md)
</dt> </dl>

 

