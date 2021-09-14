---
description: La méthode ReadRecord construit une commande APDU (Application Protocol Data Unit) qui lit soit le contenu des enregistrements spécifiés, soit la partie de début d’un enregistrement d’un fichier élémentaire.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816 :: ReadRecord, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193952"
---
# <a name="iscardiso7816readrecord-method"></a>ISCardISO7816 :: ReadRecord, méthode

\[La méthode **ReadRecord** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ReadRecord** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui lit soit le contenu des enregistrements spécifiés, soit la partie de début d’un enregistrement d’un fichier élémentaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byRecordId* \[ dans\]
</dt> <dd>

Numéro d’enregistrement ou ID du premier enregistrement à lire (00 indique l’enregistrement en cours).

</dd> <dt>

*byRefCtrl* \[ dans\]
</dt> <dd>

Codage du contrôle de référence.



| Valeur                                                                                                                                                                                | Signification                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF actuel**</dt> </dl>     | Position du bit : 00000---<br/> EF actuellement sélectionné.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID EF Short**</dt> </dl> | Position du bit : xxxxx---<br/> Identificateur EF bref.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Position du bit : 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Enregistrement \#**</dt> </dl>            | Position du bit :-----1xx<br/> Utilisation du numéro d’enregistrement dans P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Lire l’enregistrement**</dt> </dl> | Position du bit :-----100<br/> Lire l’enregistrement P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Jusqu’au dernier**</dt> </dl>     | Position du bit :-----101<br/> Lit tous les enregistrements de P1 jusqu’au dernier. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Jusqu’à P1**</dt> </dl>             | Position du bit :-----110<br/> Lit tous les enregistrements du dernier au plus P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Position du bit :-----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**ID d’enregistrement**</dt> </dl>         | Position du bit :-----0XX<br/> Utilisation du numéro d’enregistrement dans P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**Première apparition**</dt> </dl> | Position du bit :-----000<br/> Lire la première occurrence. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Dernière exécution**</dt> </dl>     | Position du bit :-----001<br/> Lire la dernière occurrence. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Suivant**</dt> </dl>     | Position du bit :-----010<br/> Lire l’occurrence suivante. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Précédente**</dt> </dl>             | Position du bit :-----011<br/> Lire l’occurrence précédente. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Confidentialité**</dt> </dl>                     | Position du bit :---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[ dans\]
</dt> <dd>

Nombre d’octets à lire à partir du EF transparent.

Si le champ le contient uniquement des zéros, en fonction de b3b2b1 de P2 et dans la limite de 256 pour la longueur abrégée ou de 65536 pour la longueur étendue, la commande doit lire complètement l’enregistrement demandé unique ou la séquence d’enregistrements demandée.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de lecture.

Si un autre fichier élémentaire est actuellement sélectionné au moment de l’émission de cette commande, il peut être traité sans identification du fichier actuellement sélectionné.

Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.

Impossible de lire les fichiers élémentaires sans structure d’enregistrement. La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure d’enregistrement.

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Spécifications



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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
