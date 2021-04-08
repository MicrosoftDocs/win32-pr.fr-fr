---
title: Modifier la méthode de la classe MicrosoftDNS_WINSType
description: La méthode modify met à jour un enregistrement de ressource WINS (Windows Internet Name Service).
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_WINSType classe
- MicrosoftDNS_WINSType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843866"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a>Modifier la méthode de la \_ classe WINSType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource WINS (Windows Internet Name Service).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*MappingFlag* \[ dans, facultatif\]
</dt> <dd>

Indicateur de mappage WINS qui spécifie si l’enregistrement doit être inclus dans la réplication de zone. Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local). Les valeurs suivantes sont valides.



| Valeur                                                                                                                                               | Signification                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Indicateur de réplication<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Indicateur de non-réplication (enregistrement local)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle un serveur DNS tente de résoudre à l’aide de la recherche WINS.

</dd> <dt>

*CacheTimeout* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.

</dd> <dt>

*WinsServers* \[ dans, facultatif\]
</dt> <dd>

Liste des adresses IP séparées par des virgules des serveurs WINS utilisés dans les recherches WINS.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

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

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSType**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





