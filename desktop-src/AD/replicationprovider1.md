---
title: ReplicationProvider1, classe
description: Classe de base pour l’instance du fournisseur.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory de la classe ReplicationProvider1
- Active Directory de la classe ReplicationProvider1, Description
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032766"
---
# <a name="replicationprovider1-class"></a>ReplicationProvider1, classe

Classe de base pour l’instance du fournisseur.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a>Membres

La classe **ReplicationProvider1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **ReplicationProvider1** possède les propriétés suivantes.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur de classe utilisé par WMI pour déterminer s’il faut charger un fournisseur de haute performance dans le processus client ou le processus WMI. Si le fournisseur et le client se trouvent sur le même ordinateur, WMI charge le fournisseur in-process sur le client en utilisant **ClientLoadableCLSID** comme identificateur de classe. Lorsque le fournisseur et le client se trouvent sur des ordinateurs différents, WMI charge le fournisseur in-process dans le processus WMI. WMI utilise également **ClientLoadableCLSID** pour prendre en charge les opérations d’actualisation.

Pour plus d’informations, consultez [inscription d’un fournisseur de High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**IDENTIFICATEUR**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**GUID** qui représente l’identificateur de classe (**CLSID**) de l’objet com du fournisseur. Cet objet COM doit contenir une implémentation de l’interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identifie l’ordinateur sur lequel démarrer le fournisseur. Si le fournisseur s’exécute sur l’ordinateur local, il a la **valeur null**.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, cette instance est activée et peut être utilisée pour effectuer les demandes des clients.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")
</dt> </dl>

Contient le modèle d’hébergement du fournisseur.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Réservé. La valeur par défaut est zéro (0).

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Jeu d’indicateurs qui fournissent des informations sur la sérialisation. La valeur par défaut est zéro (0).

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Toute l’initialisation de ce fournisseur doit être sérialisée.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Toutes les initialisations de ce fournisseur dans le même espace de noms doivent être sérialisées.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


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

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

**Windows Server 2003 :** Cette propriété est désactivée.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nom du fournisseur.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur est initialisé pour chaque paramètre régional lorsqu’un utilisateur se connecte à un même espace de noms plusieurs fois à l’aide de différents paramètres régionaux. La valeur par défaut est **FALSE**.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur est initialisé une fois pour chaque utilisateur NT LAN Manager (NTLM) qui effectue des demandes au fournisseur. Si la **valeur est false** (valeur par défaut), le fournisseur est initialisé une fois pour tous les utilisateurs.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**FCP**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le fournisseur s’engage à préparer le déchargement en appelant [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur tous les points d’interface en attente lorsque WMI appelle la méthode de mise en **version** de son interface principale. Les fournisseurs qui doivent conserver les clients de WMI après qu’ils ne fonctionnent pas comme les fournisseurs doivent définir **pure** sur **false**. Le paramètre par défaut est **true**. Pour plus d’informations, consultez la section Notes de cette rubrique.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Le descripteur de sécurité (SD) dans le langage SDDL (Security Descriptor Definition Language) qui détermine l’ensemble des utilisateurs qui peuvent appeler [**IWbemDecoupledRegistrar : Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) pour le fournisseur découplé. Pour plus d’informations, consultez la rubrique [langage de définition du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-definition-language) dans la section sécurité de la SDK Windows. Ce descripteur de sécurité est utilisé uniquement pour les fournisseurs découplés et n’affecte pas les autres fournisseurs. Pour plus d’informations, consultez [incorporation d’un fournisseur dans une application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

WMI effectue des vérifications d’accès pour les fournisseurs découplés qui utilisent les interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) et [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) . Si le descripteur de sécurité a la **valeur null**, seules les applications ou les services qui s’exécutent sous les comptes LocalSystem, NetworkService et LocalService peuvent exécuter un fournisseur découplé.

La chaîne suivante montre un fournisseur découplé qui doit être exécuté uniquement par des administrateurs intégrés.» O :BAG : BAD : (A ;; 0 x1 ;;; BA)»

Pour plus d’informations sur la définition de la propriété **SecurityDescriptor** , consultez maintenance de la [sécurité WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Non utilisé.

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

[Format de date et d’heure](/windows/desktop/WmiSdk/date-and-time-format) qui spécifie la durée pendant laquelle WMI autorise le fournisseur à rester inactif avant d’être déchargé. En règle générale, les fournisseurs demandent que WMI n’attende pas plus de cinq minutes.

Pour la version actuelle de WMI, la valeur de cette propriété est ignorée. WMI décharge le fournisseur en fonction de la valeur du délai d’attente dans une classe interne de l' \\ espace de noms racine. Il est recommandé que les fournisseurs définissent **UnloadTimeout**. Pour plus d’informations, consultez [déchargement d’un fournisseur](/windows/desktop/WmiSdk/unloading-a-provider).

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Version du fournisseur. Les versions prises en charge sont 1 et 2. La version 2 renforce les contrôles de validité de toutes les inscriptions de propriété associées, en particulier la propriété [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .

Cette propriété est héritée de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> </dl>

## <a name="remarks"></a>Notes

Une instance de cette classe représente le fournisseur WMI pour les services domaine Active Directory. Ces paramètres par défaut sont les suivants :

-   Name = « ReplProv1 »
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = « NetworkServiceHost »

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\MicrosoftActiveDirectory racine<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

