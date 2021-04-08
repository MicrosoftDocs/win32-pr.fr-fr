---
title: Classe MDM_PassportForWork_Device_Policies02
description: La \_ \_ classe Policies02 de l’appareil MDM PassportForWork \_ définit les paramètres de la stratégie Windows Hello entreprise.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- Classe MDM_PassportForWork_Device_Policies02
- Classe MDM_PassportForWork_Device_Policies02, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941937"
---
# <a name="mdm_passportforwork_device_policies02-class"></a>\_Classe de \_ Policies02 d’appareil PassportForWork MDM \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La classe Policies02 de l' **\_ \_ appareil \_ MDM PassportForWork** définit les paramètres de la stratégie Windows Hello entreprise.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a>Membres

La classe Policies02 de l' **\_ \_ appareil \_ PassportForWork MDM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe Policies02 de l' **\_ \_ appareil \_ MDM PassportForWork** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nœud pour les paramètres de stratégie Windows Hello entreprise.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Device/Vendor/MSFT/PassPortForWork/*TenantID*/ »

</dd> <dt>

[UseCertificateForOnPremAuth](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

