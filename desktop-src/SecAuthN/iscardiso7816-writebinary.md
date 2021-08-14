---
description: La méthode WriteBinary construit une commande APDU (Application Protocol Data Unit) qui écrit des valeurs binaires dans un fichier élémentaire.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816 :: WriteBinary, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 198a8eedc38636f60886af251c8520ef4726f362958c13a25fc3bf32653d7c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922918"
---
# <a name="iscardiso7816writebinary-method"></a>ISCardISO7816 :: WriteBinary, méthode

\[La méthode **writeBinary** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **writeBinary** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui écrit des valeurs binaires dans un fichier élémentaire.

En fonction des attributs de fichier, la commande effectue l’une des opérations suivantes :

-   Le ou logique des bits déjà présents dans la carte avec les bits indiqués dans la commande APDU (l’État effacé logique des bits du fichier est 0).
-   Le AND logique des bits déjà présents dans la carte avec les bits indiqués dans la commande APDU (l’État effacé logique des bits du fichier est 1).
-   Écriture unique dans la carte des bits donnée dans la commande APDU.

Si aucune indication n’est donnée dans l’octet de codage des données, le comportement logique ou s’applique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteBinary(
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

Décalage à l’emplacement d’écriture à partir du début du fichier binaire (EF). Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier. Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier.

</dd> <dt>

*byP2* \[ dans\]
</dt> <dd>

Décalage à l’emplacement d’écriture à partir du début du fichier binaire (EF). Si B8 = 1 dans P1, alors B7 et B6 de P1 ont la valeur zéro (RFU bits), B5 à B1 pour P1 est un identificateur EF bref et P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier. Si B8 = 0 dans P1, P1 \| \| P2 est le décalage du premier octet à écrire dans les unités de données à partir du début du fichier.

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne d’unités de données à écrire.

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

Lorsque la commande contient un identificateur élémentaire Short valide, elle définit le fichier en tant que fichier élémentaire actuel.

Lorsqu’une opération d’écriture binaire a été appliquée à une unité de données d’un EF d’écriture unique, toute opération d’écriture faisant référence à cette unité de données est abandonnée si le contenu de l’unité de données ou l’indicateur d’État effacé logique (le cas échéant) attaché à cette unité de données est différent de l’État effacé logique.

Impossible d’écrire dans les fichiers élémentaires sans structure transparente. La commande encapsulée est abandonnée si elle est appliquée à un fichier élémentaire sans structure transparente.

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

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
