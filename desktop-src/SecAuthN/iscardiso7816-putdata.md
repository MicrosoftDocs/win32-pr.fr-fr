---
description: La méthode PutData construit une commande APDU (Application Protocol Data Unit) qui stocke un objet de données primitif unique ou le jeu d’objets de données contenu dans un objet de données construit, en fonction du fichier sélectionné.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: ISCardISO7816 ::P méthode utData (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 66698db3c15223071167441fc37437bfa299baa100c58943a41cb4d774a8e17c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141112"
---
# <a name="iscardiso7816putdata-method"></a>ISCardISO7816 ::P méthode utData

\[La méthode **PutData** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **PutData** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui stocke un objet de données primitif unique ou le jeu d’objets de données contenu dans un objet de données construit, en fonction du fichier sélectionné.

La façon dont les objets sont stockés (écriture unique et/ou mise à jour et/ou ajout) dépend de la définition ou de la nature des objets de données.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byP1* \[ dans\]
</dt> <dd>

Codage de P1-P2.



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

Codage de P1-P2.



| Valeur                                                                                  | Signification                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | La balise BER-TLV (1 octet) dans P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Données d’application (codage propriétaire)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Balise SIMPLE-TLV dans P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | La balise BER-TLV (2 octets) dans P1-P2<br/>        |



 

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon d’octets qui contient les paramètres et les données à écrire.

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

La commande ne peut être exécutée que si l’état de sécurité répond aux conditions de sécurité définies par l’application dans le [*contexte*](../secgloss/c-gly.md) de la fonction.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Stocker les données d’application
</dt> <dd>

Lorsque la valeur de P1-P2 se situe dans la plage comprise entre 0100 et 01FF, la valeur P1-P2 est un identificateur réservé aux tests internes de carte et aux services propriétaires explicites dans un contexte d’application donné.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Stocker des objets de données
</dt> <dd>

Lorsque la valeur P1-P2 se trouve dans la plage comprise entre 0040 et 00FF, la valeur de P2 doit être une balise BER-TLV sur un octet unique. La valeur de 00FF est réservée pour indiquer que le champ de données contient des objets de données BER-TLV.

Lorsque la valeur de P1-P2 se situe dans la plage 0200 à 02FF, la valeur de P2 doit être une balise SIMPLE-TLV. La valeur 0200 est RFU. La valeur 02FF est réservée pour indiquer que le champ de données contient des objets de données simples-TLV.

Lorsque la valeur de P1-P2 se situe dans la plage comprise entre 4000 et FFFF, la valeur P1-P2 doit être une balise BER-TLV sur deux octets. Les valeurs 4000 à FFFF sont RFU.

Lorsqu’un objet de données primitif est fourni, le champ de données du message de commande doit contenir la valeur de l’objet de données primitif correspondant.

Lorsqu’un objet de données construit est fourni, le champ de données du message de commande doit contenir la valeur de l’objet de données construit (autrement dit, les objets de données, y compris leur balise, leur longueur et leur valeur).

</dd> </dl>

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

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
