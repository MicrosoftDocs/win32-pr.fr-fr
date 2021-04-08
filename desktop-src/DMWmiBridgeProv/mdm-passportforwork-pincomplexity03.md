---
title: Classe MDM_PassportForWork_PINComplexity03
description: La \_ \_ classe PINComplexity03 MDM PassportForWork définit la complexité du code confidentiel pour les informations d’identification de connexion pour Windows Hello entreprise.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- Classe MDM_PassportForWork_PINComplexity03
- Classe MDM_PassportForWork_PINComplexity03, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941935"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a>\_ \_ Classe PINCOMPLEXITY03 PassportForWork MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ PINComplexity03 MDM PassportForWork** définit la complexité du code confidentiel pour les informations d’identification de connexion pour Windows Hello entreprise.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a>Membres

La **classe \_ PassportForWork \_ PINComplexity03 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ PassportForWork \_ PINComplexity03 MDM** a ces propriétés.

<dl> <dt>

[Chiffres](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Expiration](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[History](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
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

Nœud racine pour les stratégies de code confidentiel.

</dd> <dt>

[LowercaseLetters](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[MaximumPINLength](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[MinimumPINLength](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
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

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/PassPortForWork/*TenantID*/Policies »

</dd> <dt>

[SpecialCharacters](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[UppercaseLetters](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

