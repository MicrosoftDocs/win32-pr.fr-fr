---
title: Classe MDM_VPNv2_Proxy02
description: La \_ \_ classe Proxy02 MDM VPNv2 définit un objet de configuration pour activer la prise en charge de proxy après connexion pour le VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- Classe MDM_VPNv2_Proxy02
- Classe MDM_VPNv2_Proxy02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465342"
---
# <a name="mdm_vpnv2_proxy02-class"></a>\_ \_ Classe PROXY02 VPNv2 MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Proxy02 MDM VPNv2** définit un objet de configuration pour activer la prise en charge de proxy après connexion pour le VPN. Le proxy défini pour ce profil est appliqué lorsque ce profil est actif et connecté.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a>Membres

La **classe \_ VPNv2 \_ Proxy02 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ VPNv2 \_ Proxy02 MDM** a ces propriétés.

<dl> <dt>

[AutoConfigUrl](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
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

Identifie le nom du nœud parent. Collection d’objets de configuration permettant d’activer la prise en charge d’un proxy après connexion pour le VPN. Le proxy défini pour ce profil est appliqué lorsque ce profil est actif et connecté.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»

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

 

