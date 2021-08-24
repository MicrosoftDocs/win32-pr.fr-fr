---
description: Construit une commande APDU qui initie l’une des opérations listées.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816 :: WriteRecord, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a023443f1121759872c4eba0743e5db5b01c8446403b312644e22c83559a527d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014379"
---
# <a name="iscardiso7816writerecord-method"></a>ISCardISO7816 :: WriteRecord, méthode

\[La méthode **WriteRecord** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **WriteRecord** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui initie l’une des opérations suivantes :

-   Écriture unique d’un enregistrement.
-   **Or** logique des octets de données d’un enregistrement déjà présent dans la carte avec les octets de données de l’enregistrement donné dans la commande APDU.
-   Le AND logique des octets de données d’un enregistrement déjà présent dans la carte avec les octets de données de l’enregistrement donné dans la commande APDU.

Si aucune indication n’est donnée dans l’octet de codage des données, le comportement logique ou s’applique.

> [!Note]  
> Lors de l’utilisation de l’adressage d’enregistrement actuel, la commande définit le pointeur d’enregistrement sur l’enregistrement mis à jour avec succès.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byRecordId* \[ dans\]
</dt> <dd>

Identification de l’enregistrement. Il s’agit de la valeur P1 :

P1 = « 00 » désigne l’enregistrement en cours.

P1 ! = « 00 » est le numéro de l’enregistrement spécifié.

</dd> <dt>

*byRefCtrl* \[ dans\]
</dt> <dd>

Codage du contrôle de référence P2.



| Valeur                                                                                                                                                                                                | Signification                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF actuel**</dt> </dl>                     | Position du bit : 00000---<br/> EF actuellement sélectionné.<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID EF Short**</dt> </dl>                 | Position du bit : xxxxx---<br/> Identificateur EF bref.<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**Premier enregistrement**</dt> </dl>             | Position du bit :-----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**Dernier enregistrement**</dt> </dl>                 | Position du bit :-----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**Enregistrement suivant**</dt> </dl>                 | Position du bit :-----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**Enregistrement précédent**</dt> </dl> | Position du bit :-----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**Enregistrement \# dans P1**</dt> </dl>    | Position du bit :-----100<br/>                                   |



 

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers l’enregistrement à écrire.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .

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

La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.

Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel. Si un autre fichier élémentaire est actuellement sélectionné au moment de l’émission de cette commande, cette commande peut être traitée sans identification du fichier actuellement sélectionné.

Si la commande encapsulée s’applique à un fichier élémentaire linéaire ou à structure cyclique, elle est abandonnée si la longueur de l’enregistrement est différente de la longueur de l’enregistrement existant. Si elle s’applique à un fichier élémentaire structuré à variables linéaires, elle peut être exécutée lorsque la longueur de l’enregistrement est différente de la longueur de l’enregistrement existant.

Si P2 = xxxxx011 et que le fichier élémentaire est un fichier cyclique, cette commande a le même comportement qu’une commande construite à l’aide de [**AppendRecord**](iscardiso7816-appendrecord.md).

Impossible d’écrire dans les fichiers élémentaires sans structure d’enregistrement. La commande construite s’arrête si elle est appliquée à un fichier élémentaire sans structure d’enregistrement.

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
