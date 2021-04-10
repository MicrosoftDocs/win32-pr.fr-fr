---
title: Méthode Export de la classe Win32_TSGatewayServer
description: Retourne la configuration du serveur de passerelle Bureau à distance (passerelle Bureau à distance) sous la forme d’une chaîne XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode d’exportation
- Méthode d’exportation Services Bureau à distance, classe Win32_TSGatewayServer
- Services Bureau à distance de la classe Win32_TSGatewayServer, méthode d’exportation
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942890"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Méthode Export de la \_ classe TSGatewayServer Win32

Retourne la configuration du serveur de passerelle Bureau à distance (passerelle Bureau à distance) sous la forme d’une chaîne XML.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ExportType* \[ dans\]
</dt> <dd>

Contenu à exporter. Définissez le type d’exportation en définissant les bits correspondants dans le paramètre *ExportType* . Vous pouvez définir plusieurs types d’exportation. Par exemple, si le bit 0 est défini, Services Bureau à distance stratégies d’autorisation des connexions (RD Cap) seront exportées. Si les deux bits 0 et 2 sont définis, les stratégies d’autorisation des ressources pour les services Bureau à distance et les Services Bureau à distance RD sont exportées.

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Exporter toutes les majuscules** (1)


</dt> <dd>

Exporter toutes les connexions Bureau à distance.

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Exporter tous les serveurs RADIUS** (2)


</dt> <dd>

Exportez une liste de tous les serveurs NPS (Network Policy Server).

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Exporter tous les stratégies** (4)


</dt> <dd>

Exporter tous les stratégies RD.

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Exporter tous les RGs** (8)


</dt> <dd>

Exportez tous les groupes de ressources.

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Exporter tous les serveurs LoadBalancing** (16)


</dt> <dd>

Exporter une liste de tous les serveurs d’équilibrage de charge.

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Exporter tous les paramètres du serveur** (32)


</dt> <dd>

Exportez tous les paramètres de serveur liés à la passerelle des services Bureau à distance.

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Exporter toutes les stratégies de contrôle d’intégrité** (64)


</dt> <dd>

Exporter toutes les stratégies de contrôle d’intégrité.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 et Windows Server 2008 : * *

Cette valeur n’est pas prise en charge avant Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ à\]
</dt> <dd>

Chaîne du XML.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

