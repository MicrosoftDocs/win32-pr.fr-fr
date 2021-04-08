---
title: Classe MDM_VPNv2_RouteList02_01
description: La \_ classe MDM VPNv2 \_ RouteList02 \_ 01 contient une liste facultative d’itinéraires à ajouter à la table de routage pour l’interface VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Classe MDM_VPNv2_RouteList02_01
- Classe MDM_VPNv2_RouteList02_01, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033079"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>\_Classe VPNv2 \_ ROUTELIST02 \_ 01 MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** contient une liste facultative d’itinéraires à ajouter à la table de routage pour l’interface VPN.

Cela est nécessaire pour le cas de tunneling fractionné où le site du serveur VPN a plus de sous-réseaux que le sous-réseau par défaut en fonction de l’adresse IP affectée à l’interface.

Chaque ordinateur qui exécute TCP/IP prend des décisions de routage. Ces décisions sont contrôlées par la table de routage IP. L’ajout de valeurs sous ce nœud met à jour la table de routage avec des itinéraires pour l’interface VPN après la connexion. Les valeurs sous ce nœud représentent le préfixe de destination des itinéraires IP. Un préfixe de destination se compose d’un préfixe d’adresse IP et d’une longueur de préfixe.

L’ajout d’un itinéraire ici permet à la pile de mise en réseau d’identifier le trafic qui doit passer par l’interface VPN pour le VPN de tunnel fractionné. Certains serveurs VPN peuvent le configurer pendant la négociation de connexion et n’ont pas besoin de ces informations dans le profil VPN. Vérifiez auprès de votre administrateur de serveur VPN si vous avez besoin de ces informations dans le profil VPN.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>Membres

La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** possède ces propriétés.

<dl> <dt>

[Adresse](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
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

Identifie le nom du nœud parent.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*/RouteList »

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
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

 

