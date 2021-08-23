---
title: Classe MDM_VPNv2_PluginProfile02
description: la \_ classe VPNv2 \_ PlugInProfile02 MDM décrit les informations nécessaires à l’utilisation d’un plug-in VPN basé sur le magasin de Windows.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- Classe MDM_VPNv2_PluginProfile02
- Classe MDM_VPNv2_PluginProfile02, Description
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5833440924af2c8a3682a50cb066c892ce3e9c428711f21f149c70f4c0db8859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795729"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a>\_ \_ Classe PLUGINPROFILE02 VPNv2 MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

la **classe \_ VPNv2 \_ PlugInProfile02 MDM** décrit les informations nécessaires à l’utilisation d’un plug-in VPN basé sur le magasin de Windows.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a>Membres

La **classe \_ VPNv2 \_ PluginProfile02 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ VPNv2 \_ PluginProfile02 MDM** a ces propriétés.

<dl> <dt>

[CustomConfiguration](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[CustomStoreUrl](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
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

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/VPNv2/*ProfileName*»

</dd> <dt>

[PluginPackageFamilyName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[ServerUrlList](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
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

 

