---
title: Méthode UpdateFromDS de la classe MicrosoftDNS_Zone
description: La méthode UpdateFromDS force une mise à jour de la zone à partir du service d’annuaire (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- Méthode UpdateFromDS DNS
- Méthode UpdateFromDS DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode UpdateFromDS
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106570"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a>Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS

La méthode **UpdateFromDS** force une mise à jour de la zone à partir du service d’annuaire (DS).

## <a name="syntax"></a>Syntaxe


```mof
void UpdateFromDS();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour exécuter correctement cette méthode, ZoneType doit être égal à zéro et la zone doit être stockée sur le DS.

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

[**Méthode ResetSecondaries de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Méthode ResumeZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





