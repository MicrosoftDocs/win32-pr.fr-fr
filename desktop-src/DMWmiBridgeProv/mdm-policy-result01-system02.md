---
title: Classe MDM_Policy_Result01_System02
description: La \_ classe Result01 System02 de la stratégie MDM \_ \_ représente les stratégies système disponibles.
ms.assetid: 9A0D9688-9062-429F-897F-75705DC8FD79
keywords:
- Classe MDM_Policy_Result01_System02
- Classe MDM_Policy_Result01_System02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02.InstanceID
- MDM_Policy_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c4ea62ee18a2e5cbba25bb561fe2aefe1ced581d0bea51889ac2ddab1195c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694629"
---
# <a name="mdm_policy_result01_system02-class"></a>\_Classe System02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Result01 \_ System02 de la stratégie MDM** représente les stratégies système disponibles. Ces stratégies déterminent les configurations système autorisées.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_System02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ System02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ System02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[AllowBuildPreview](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowEmbeddedMode](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowExperimentation](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowFontProviders](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowLocation](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowStorageCard](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowTelemetry](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowUserToResetPhone](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[BootStartDriverInitialization](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DisableEnterpriseAuthProxy](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DisableOneDriveFileSync](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DisableSystemRestore](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[FeedbackHubAlwaysSaveDiagnosticsLocally](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « System ».

</dd> <dt>

[LimitEnhancedDiagnosticDataWindowsAnalytics](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »

</dd> <dt>

[TelemetryProxy](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine DMMap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

