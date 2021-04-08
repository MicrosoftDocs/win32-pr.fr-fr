---
description: La méthode ManageChannel construit une commande APDU (Application Protocol Data Unit) qui ouvre et ferme des canaux logiques.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816 :: ManageChannel, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034318"
---
# <a name="iscardiso7816managechannel-method"></a>ISCardISO7816 :: ManageChannel, méthode

\[La méthode **ManageChannel** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ManageChannel** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui ouvre et ferme des canaux logiques.

La fonction Open ouvre un nouveau canal logique autre que celui de base. Des options sont fournies pour que la carte affecte un numéro de canal logique, ou pour que le numéro de canal logique soit fourni à la carte.

La fonction Close ferme explicitement un canal logique autre que le canal de base. Une fois la fermeture terminée, le canal logique sera disponible pour une réutilisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byChannelState* \[ dans\]
</dt> <dd>

Le bit B8 de P1 est utilisé pour indiquer la fonction Open ou la fonction Close ; Si B8 est égal à 0, MANAGE CHANNEL ouvrira un canal logique et, si B8 a la valeur 1, le canal MANAGE doit fermer un canal logique :

P1 = « 00 » pour l’ouvrir

P1 = ' 80 'pour fermer

Les autres valeurs sont RFU

</dd> <dt>

*byChannel* \[ dans\]
</dt> <dd>

Pour la fonction Open (P1 = « 00 »), les bits B1 et B2 de P2 sont utilisés pour coder le numéro de canal logique de la même manière que dans l’octet de classe, les autres bits de P2 sont RFU.

Lorsque B1 et B2 de P2 ont la **valeur null**, la carte affecte un numéro de canal logique qui est retourné dans les bits B1 et B2 du champ de données.

Lorsque B1 et/ou B2 de P2 ne sont pas **null**, ils codent un numéro de canal logique autre que celui de base ; Ensuite, la carte ouvre le numéro de canal logique attribué en externe.

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



 

## <a name="remarks"></a>Notes

Lorsque la fonction Open est correctement exécutée à partir du canal logique de base, le MF est implicitement sélectionné comme DF actuel et l’état de sécurité du nouveau canal logique doit être identique au canal logique de base après ATR. L’état de sécurité du nouveau canal logique doit être distinct de celui de tout autre canal logique.

Lorsque la fonction Open est exécutée avec succès à partir d’un canal logique, qui n’est pas le canal de base, le DF actuel du canal logique qui a émis la commande est sélectionné en tant que DF actuel. En outre, l’état de sécurité du nouveau canal logique doit être identique à l’état de sécurité du canal logique à partir duquel la fonction d’ouverture a été effectuée.

Après une fonction de fermeture réussie, l’état de sécurité associé à ce canal logique est perdu.

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
