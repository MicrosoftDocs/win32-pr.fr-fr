---
title: Méthode Import de la classe Win32_TSGatewayServer
description: Importe une configuration donnée sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode d’importation
- Services Bureau à distance de la méthode d’importation, classe Win32_TSGatewayServer
- Win32_TSGatewayServer de la classe Services Bureau à distance, méthode Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2629e8e44acd0f617e86a846cc127ab77250673c8612f2d2f53ab8c0238d9f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574569"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Méthode Import de la \_ classe TSGatewayServer Win32

Importe une configuration donnée sur le serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

## <a name="syntax"></a>Syntaxe


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ImportType* \[ dans\]
</dt> <dd>

Contenu à importer. Définissez le type d’importation en définissant les bits correspondants dans le paramètre *ImportType* . Vous pouvez définir plusieurs types d’importation. Par exemple, si le bit 0 est défini, Services Bureau à distance stratégies d’autorisation des connexions (RD Cap) seront importées. Si les deux bits 0 et 2 sont définis, les stratégies d’autorisation des ressources pour les services Bureau à distance et les Services Bureau à distance RD sont importées.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importer toutes les majuscules** (1)


</dt> <dd>

Importez toutes les connexions Bureau à distance.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importer tous les serveurs RADIUS** (2)


</dt> <dd>

Importez une liste de tous les serveurs NPS (Network Policy Server).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importer tous les stratégies** (4)


</dt> <dd>

Importez tous les stratégies RD.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importer tous les RGs** (8)


</dt> <dd>

Importez tous les groupes de ressources.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importer tous les serveurs LoadBalancing** (16)


</dt> <dd>

Importez une liste de tous les serveurs d’équilibrage de charge.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**importer tous les Paramètres de serveur** (32)


</dt> <dd>

Importez tous les paramètres de serveur liés à la passerelle Bureau à distance.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importer toutes les stratégies de contrôle d’intégrité** (64)


</dt> <dd>

Importez toutes les stratégies de contrôle d’intégrité.

* * Windows Server 2012 r2, Windows Server 2012, Windows server 2008 r2 et Windows server 2008 : * *

Cette valeur n’est pas prise en charge avant Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ dans\]
</dt> <dd>

Configuration sous la forme d’une chaîne XML.

</dd> <dt>

*MergeOrReplace* \[ dans\]
</dt> <dd>

Indique s’il faut fusionner ou remplacer des données lorsqu’un conflit se produit.

> [!Note]  
> La fusion n’est pas encore implémentée. Par conséquent, la valeur de ce paramètre est ignorée.

 

</dd> <dt>

*LogString* \[ à\]
</dt> <dd>

Informations de journal générées pendant l’opération d’importation.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGatewayServer Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

