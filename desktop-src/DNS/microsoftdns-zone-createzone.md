---
title: Méthode CreateZone de la classe MicrosoftDNS_Zone
description: La méthode CreateZone crée une zone DNS.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Méthode CreateZone DNS
- Méthode CreateZone DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode CreateZone
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033036"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a>Méthode CreateZone de la \_ classe de zone MicrosoftDNS

La méthode **CreateZone** crée une zone DNS.

## <a name="syntax"></a>Syntaxe


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NomZone* \[ dans\]
</dt> <dd>

Chaîne représentant le nom de la zone.

</dd> <dt>

*ZoneType* \[ dans\]
</dt> <dd>

Type de zone. Les valeurs suivantes sont valides :



| Valeur                                                                        | Signification                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>1</dt> </dl> | AD intégré.<br/>                                                                                           |
| <dl> <dt>2</dt> </dl> | Zone secondaire.<br/>                                                                                          |
| <dl> <dt>3</dt> </dl> | Zone de stub.<br/> **Windows Server 2003 :** Ce type de zone est introduit dans Windows Server 2003.<br/>      |
| <dl> <dt>4</dt> </dl> | Redirecteur de zone.<br/> **Windows Server 2003 :** Ce type de zone est introduit dans Windows Server 2003.<br/> |



 

</dd> <dt>

*DsIntegrated* \[ dans\]
</dt> <dd>

Indique si les données de zone sont stockées dans le Active Directory ou dans des fichiers. Si la valeur est TRUE, les données sont stockées dans le Active Directory ; Si la valeur est FALSe, les données sont stockées dans des fichiers.

</dd> <dt>

*DataFileName* \[ dans, facultatif\]
</dt> <dd>

Nom du fichier de données associé à la zone.

</dd> <dt>

*Ipaddr* \[ dans, facultatif\]
</dt> <dd>

Adresse IP du serveur DNS maître pour la zone.

</dd> <dt>

*AdminEmailName* \[ dans, facultatif\]
</dt> <dd>

Adresse de messagerie de l’administrateur responsable de la zone.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

RR de type **MicrosoftDns \_ zone**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Zone MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Méthode ForceRefresh de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Méthode PauseZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Méthode ReloadZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





