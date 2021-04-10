---
title: Méthode ResetSecondaries de la classe MicrosoftDNS_Zone
description: La méthode ResetSecondaries réinitialise les adresses IP des serveurs DNS secondaires dans la zone.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- Méthode ResetSecondaries DNS
- Méthode ResetSecondaries DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode ResetSecondaries
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942447"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS

La méthode **ResetSecondaries** réinitialise les adresses IP des serveurs DNS secondaires dans la zone.

## <a name="syntax"></a>Syntaxe


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SecondaryServers* \[ dans\]
</dt> <dd>

Tableau d’adresses IP pour les serveurs DNS secondaires.

</dd> <dt>

*SecureSecondaries* \[ dans\]
</dt> <dd>

Spécifie la sécurité à appliquer et doit être l’une des suivantes :

-   SECSECURE de la ZONE \_ \_ pas de \_ sécurité
-   ZONE \_ SECSECURE \_ NS \_ uniquement
-   Liste des SECSECURE de ZONE \_ \_ \_ uniquement
-   ZONE \_ SECSECURE \_ no \_ XFR

</dd> <dt>

*NotifyServers* \[ dans\]
</dt> <dd>

Adresse IP des serveurs DNS à notifier en cas de modification de la zone.

</dd> <dt>

*Notifier* \[ dans\]
</dt> <dd>

Paramètre de notification et doit avoir l’une des valeurs suivantes :

-   notification de ZONE \_ \_ désactivée
-   \_notifier \_ tous les secondaires de zone \_
-   \_liste des notifications de zone \_ \_ uniquement

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

RR de type [**MicrosoftDNS \_ zone**](microsoftdns-zone.md).

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

[**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





