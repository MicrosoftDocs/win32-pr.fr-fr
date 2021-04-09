---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
description: La \_ \_ \_ classe ENTERPRISEDATAPROTECTION01 EXE03 de MDM AppLocker capture la liste des applications exécutables qui sont autorisées à gérer les données d’entreprise.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03
- Classe MDM_AppLocker_EnterpriseDataProtection01_EXE03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106150"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a>\_ \_ Classe EXE03 ENTERPRISEDATAPROTECTION01 de MDM AppLocker \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ EnterpriseDataProtection01 \_ EXE03 de MDM AppLocker** capture la liste des applications exécutables qui sont autorisées à gérer les données d’entreprise. Doit être utilisé conjointement avec les paramètres de./Vendor/MSFT/Policy/ConfigSource/DataProtection.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ EnterpriseDataProtection01 \_ EXE03 de MDM AppLocker** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ EnterpriseDataProtection01 \_ EXE03 de MDM AppLocker** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Définit des restrictions pour le lancement d’applications exécutables.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*regroupement*»

</dd> <dt>

[**Stratégie**](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine DMMap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

