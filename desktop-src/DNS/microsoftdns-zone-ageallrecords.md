---
title: Méthode AgeAllRecords de la classe MicrosoftDNS_Zone
description: La méthode AgeAllRecords active l’antériorité pour tout ou partie des enregistrements non NS et non SOA dans une zone.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- Méthode AgeAllRecords DNS
- Méthode AgeAllRecords DNS, classe MicrosoftDNS_Zone
- MicrosoftDNS_Zone de la classe DNS, méthode AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466482"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>Méthode AgeAllRecords de la \_ classe de zone MicrosoftDNS

La méthode **AgeAllRecords** active l’antériorité pour tout ou partie des enregistrements non NS et non SOA dans une zone.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nodename* \[ dans, facultatif\]
</dt> <dd>

Nom du nœud à vieillir.

</dd> <dt>

*ApplyToSubtree* \[ dans, facultatif\]
</dt> <dd>

Spécifie si l’antériorité doit s’appliquer à tous les enregistrements dans la sous-arborescence. Affectez la valeur TRUE pour appliquer l’antériorité à tous les enregistrements de la sous-arborescence, en commençant par NodeName.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

ERREUR \_ : la datation a été effectuée avec succès. Toute autre valeur est un code d’erreur.

## <a name="remarks"></a>Notes

Si *nodename* n’est pas spécifié, tous les enregistrements sont soumis au vieillissement et au nettoyage.

Si *nodename* est spécifié et que *ApplyToSubtree* n’est pas spécifié ou défini à zéro, les enregistrements au niveau du nœud spécifié seront soumis au vieillissement et au nettoyage.

Si *nodename* est spécifié et que *ApplyToSubtree* a la valeur 1, tous les enregistrements de la sous-arborescence commençant à *nodename* sont soumis à la datation et au nettoyage. L’horodatage est défini sur l’heure actuelle pour tous les enregistrements de ressource non-NS et non SOA avec le ou les noms de propriétaires identifiés par les paramètres d’entrée.

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

[**Méthode UpdateFromDS de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Méthode WriteBackZone de la \_ classe de zone MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





