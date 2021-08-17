---
title: Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
description: la \_ \_ \_ classe EnterpriseDataProtection01 StoreApps03 de MDM AppLocker capture la liste des applications Windows autorisées à gérer les données d’entreprise. Doit être utilisé conjointement avec les paramètres de./Vendor/MSFT/Policy/ConfigSource/DataProtection.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- Classe MDM_AppLocker_EnterpriseDataProtection01_StoreApps03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5b0c3af455e501695cb7a2093b841159f5755ac54e1de97a370c7dc7f2d6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077409"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a>\_ \_ Classe StoreApps03 ENTERPRISEDATAPROTECTION01 de MDM AppLocker \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

la **classe \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de MDM AppLocker** capture la liste des applications Windows autorisées à gérer les données d’entreprise. Doit être utilisé conjointement avec les paramètres de./Vendor/MSFT/Policy/ConfigSource/DataProtection.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de MDM AppLocker** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de MDM AppLocker** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

définit des restrictions pour l’exécution d’applications à partir du magasin de Windows.

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

[**Policy**](/windows/client-management/mdm/applocker-csp)
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

 

