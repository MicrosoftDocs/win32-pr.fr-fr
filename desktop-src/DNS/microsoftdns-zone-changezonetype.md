---
title: Méthode ChangeZoneType de la classe MicrosoftDNS_Zone
description: La méthode ChangeZoneType modifie le type d’une zone.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- Méthode ChangeZoneType DNS
- Méthode ChangeZoneType DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode ChangeZoneType
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4878d2937d6a8e3b14a72a1055fd4d044ad047629d9e63cced375d4f75ddb60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984549"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a>Méthode ChangeZoneType de la \_ classe de zone MicrosoftDNS

La méthode **ChangeZoneType** modifie le type d’une zone.

## <a name="syntax"></a>Syntaxe


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ZoneType* \[ dans\]
</dt> <dd>

Type de zone. Les valeurs suivantes sont valides :



| Valeur                                                                        | Signification                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl> | Zone principale.<br/>   |
| <dl> <dt>1</dt> </dl> | Zone secondaire.<br/> |
| <dl> <dt>2</dt> </dl> | Zone de stub.<br/>      |
| <dl> <dt>3</dt> </dl> | Redirecteur de zone.<br/> |



 

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

[**Méthode CreateZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-createzone.md)
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

 

 





