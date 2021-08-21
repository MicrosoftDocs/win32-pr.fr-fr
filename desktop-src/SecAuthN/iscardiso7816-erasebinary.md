---
description: Construit une commande APDU (Application Protocol Data Unit) qui définit de façon séquentielle une partie du contenu d’un fichier élémentaire à son état effacé logique, à partir d’un offset donné.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816 :: EraseBinary, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 012927e21e3ed897136a9b058ae03539b7d2e2ac0e581d04cb14235aed9ae80f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007897"
---
# <a name="iscardiso7816erasebinary-method"></a>ISCardISO7816 :: EraseBinary, méthode

\[La méthode **EraseBinary** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **EraseBinary** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui définit de façon séquentielle une partie du contenu d’un fichier élémentaire à son état effacé logique, à partir d’un décalage donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EraseBinary(
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

Position RFU.

Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.

Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.

Si le champ de données est présent, il code le décalage de la première unité de données à ne pas effacer. Ce décalage doit être supérieur à celui codé dans P1-P2. Lorsque le champ de données est vide, la commande s’efface jusqu’à la fin du fichier.

</dd> <dt>

*byP2* \[ dans\]
</dt> <dd>

Position RFU.

Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.

Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à effacer (en unités de données) à partir du début du fichier.

Si le champ de données est présent, il code le décalage de la première unité de données à ne pas effacer. Ce décalage doit être supérieur à celui codé dans P1-P2. Lorsque le champ de données est vide, la commande s’efface jusqu’à la fin du fichier.

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers les données qui spécifient la plage d’effacement. Ce paramètre peut avoir la **valeur null**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne à l’aide du pointeur *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un paramètre non valide a été passé.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>              |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                            |



 

## <a name="remarks"></a>Remarques

La commande encapsulée ne peut être exécutée que si l’état de sécurité de la [*carte à puce*](../secgloss/s-gly.md) répond aux attributs de sécurité du fichier élémentaire en cours de traitement.

Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.

Les fichiers élémentaires sans structure transparente ne peuvent pas être effacés. La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure transparente.

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
