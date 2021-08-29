---
title: Classe MDM_Policy_Result01_Connectivity02
description: La \_ classe Result01 Connectivity02 de la stratégie MDM \_ \_ représente les stratégies de connexion disponibles.
ms.assetid: af5f21f8-8010-4e5a-b75f-30032333d87d
keywords:
- Classe MDM_Policy_Result01_Connectivity02
- Classe MDM_Policy_Result01_Connectivity02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Connectivity02
- MDM_Policy_Result01_Connectivity02.InstanceID
- MDM_Policy_Result01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e45489e09bff530bf17b499a8875f5bf798f5f270cd5c23b7853638dbada3df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796479"
---
# <a name="mdm_policy_result01_connectivity02-class"></a>\_Classe Connectivity02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Result01 \_ Connectivity02 de la stratégie MDM** représente les stratégies de connexion disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ Connectivity02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ Connectivity02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[AllowBluetooth](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowCellularData](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowCellularDataRoaming](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowConnectedDevices](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowVPNOverCellular](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowVPNRoamingOverCellular](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DiablePrintingOverHTTP](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DisableDownloadingOfPrintDriversOverHTTP](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[DisallowNetworkConnectivityActiveTests](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[HardenedUNCPaths](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « connectivity ».

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

[ProhibitInstallationAndConfigurationOfNetworkBridge](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
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

 

