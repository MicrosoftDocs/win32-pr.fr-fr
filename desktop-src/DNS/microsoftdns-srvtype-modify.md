---
title: Modifier la méthode de la classe MicrosoftDNS_SRVType
description: La méthode modify met à jour un enregistrement de ressource de service (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_SRVType classe
- MicrosoftDNS_SRVType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9e1a4b3b3da3fc7f7cb732c094f4ddfce2e2c0ca3e8836f25bb3034b590bf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076713"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a>Modifier la méthode de la \_ classe SRVType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de service (SRV).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Priorité* \[ dans, facultatif\]
</dt> <dd>

Priorité de l’hôte cible spécifiée dans le nom du propriétaire. Les nombres inférieurs impliquent des priorités plus élevées.

</dd> <dt>

*Poids* \[ dans, facultatif\]
</dt> <dd>

Poids de l’hôte cible. Cela est utile lorsque vous sélectionnez parmi les hôtes qui ont la même priorité. La probabilité d’utiliser cet hôte doit être proportionnelle à son poids.

</dd> <dt>

*Port* \[ dans, facultatif\]
</dt> <dd>

Port utilisé sur l’hôte cible d’un service de protocole.

</dd> <dt>

*SRVDomainName* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet de l’hôte cible. Une cible de \\ . \\ signifie que le service n’est pas disponible dans ce domaine.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SRVType**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





