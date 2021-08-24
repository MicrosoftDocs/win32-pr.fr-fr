---
description: La méthode GetData construit une commande APDU (Application Protocol Data Unit) qui récupère soit un objet de données primitif unique, soit un ensemble d’objets de données (contenu dans un objet de données construit), en fonction du type de fichier sélectionné.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816 :: GetData, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ef783092edb87a29203c83afcf67fb594eb84dcc296621379c9f39a9ccbcc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672379"
---
# <a name="iscardiso7816getdata-method"></a>ISCardISO7816 :: GetData, méthode

\[La méthode **GetData** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **GetData** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui récupère soit un objet de données primitif unique, soit un ensemble d’objets de données (contenu dans un objet de données construit), en fonction du type de fichier sélectionné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byP1* \[ dans\]
</dt> <dd>

Paramètres.



| Valeur                                                                                  | Signification                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | La balise BER-TLV (1 octet) dans P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Données d’application (codage propriétaire)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Balise SIMPLE-TLV dans P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | La balise BER-TLV (2 octets) dans P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ dans\]
</dt> <dd>

Paramètres.



| Valeur                                                                                  | Signification                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | La balise BER-TLV (1 octet) dans P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Données d’application (codage propriétaire)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Balise SIMPLE-TLV dans P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | La balise BER-TLV (2 octets) dans P1-P2<br/>        |



 

</dd> <dt>

*lBytesToGet* \[ dans\]
</dt> <dd>

Nombre d’octets attendus dans la réponse.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Remarques

La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de lecture. Les conditions de sécurité dépendent de la stratégie de la carte et peuvent être manipulées par le biais de [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), etc.

Pour sélectionner un fichier, appelez [**SelectFile**](iscardiso7816-selectfile.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**PutData**](iscardiso7816-putdata.md)
</dt> <dt>

[**SelectFile**](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
