---
title: Classe MDM_VPNv2_NativeProfile02
description: la \_ \_ classe NativeProfile2 MDM VPNv2 définit les informations de profil lors de l’utilisation d’un protocole VPN Windows boîte de réception (IKEv2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- Classe MDM_VPNv2_NativeProfile02
- Classe MDM_VPNv2_NativeProfile02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b09152d705e7746aded2487d06c5668c766e37940a620a19ff15733ac6522459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076953"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a>\_ \_ Classe NATIVEPROFILE02 VPNv2 MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

la **classe \_ \_ NativeProfile2 MDM VPNv2** définit les informations de profil lors de l’utilisation d’un protocole VPN Windows boîte de réception (IKEv2, PPTP, L2TP).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a>Membres

La **classe \_ VPNv2 \_ NativeProfile02 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ VPNv2 \_ NativeProfile02 MDM** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent.

</dd> <dt>

[L2tpPsk](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[NativeProtocolType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»

</dd> <dt>

[RoutingPolicyType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Serveurs](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
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
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

