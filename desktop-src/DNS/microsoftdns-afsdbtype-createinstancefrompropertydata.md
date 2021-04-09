---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_AFSDBType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942138"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a>Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AFSDBType

La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.

## <a name="syntax"></a>Syntaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DnsServerName* \[ dans\]
</dt> <dd>

Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.

</dd> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.

</dd> <dt>

*OwnerName* \[ dans\]
</dt> <dd>

Nom du propriétaire de l’enregistrement de ressource.

</dd> <dt>

*RecordClass* \[ dans, facultatif\]
</dt> <dd>

Classe de l’enregistrement de ressource. La valeur par défaut est 1. Les valeurs suivantes sont valides.



| Valeur                                                                                                | Signification                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | DANS (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Sous-type* \[ dans\]
</dt> <dd>

Sous-type du serveur AFS hôte. Pour le sous-type 1 (valeur = 1), l’hôte dispose d’un serveur d’emplacement de volume AFS version 3,0 pour la cellule AFS nommée. Dans le cas d’un sous-type 2 (valeur = 2), l’hôte dispose d’un serveur de noms authentifié contenant le nœud de répertoire racine de la cellule pour la cellule DCE/NCA nommée.

</dd> <dt>

*Nom du serveur* \[ dans\]
</dt> <dd>

Nom de domaine complet spécifiant un hôte qui a un serveur pour la cellule AFS spécifiée dans le nom du propriétaire.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe AFSDBType MicrosoftDNS**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





