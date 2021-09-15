---
description: Construit une commande APDU (Application Protocol Data Unit) qui lance le calcul des données d’authentification par la carte à l’aide des données de stimulation envoyées par l’appareil d’interface et d’une clé secrète pertinente (par exemple, une clé) stockée dans la carte.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816 :: InternalAuthenticate, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311346"
---
# <a name="iscardiso7816internalauthenticate-method"></a>ISCardISO7816 :: InternalAuthenticate, méthode

\[La méthode **InternalAuthenticate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **InternalAuthenticate** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui lance le calcul des données d’authentification par la carte à l’aide des données de stimulation envoyées par l’appareil d’interface et d’une clé secrète pertinente (par exemple, une clé) stockée dans la carte.

Lorsque le secret pertinent est attaché à MF, la commande peut être utilisée pour authentifier la carte dans son ensemble.

Lorsque le secret pertinent est attaché à un autre DF, la commande peut être utilisée pour authentifier ce DF.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byAlgorithmRef* \[ dans\]
</dt> <dd>

Référence de l’algorithme dans la carte.

Si cette valeur est égale à zéro, cela indique qu’aucune information n’est fournie. La référence de l’algorithme est connue avant l’émission de la commande ou est fournie dans le champ de données.

</dd> <dt>

*bySecretRef* \[ dans\]
</dt> <dd>

Référence du secret.



| Valeur                                                                                                                                                                                    | Signification                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Aucune information**</dt> </dl>                     | Position du bit : 00000000 <br/> Aucune information n’est fournie. La référence du secret est connue avant l’émission de la commande ou est fournie dans le champ de données.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Référence globale**</dt> </dl>         | Position du bit : 0------- <br/> Données de référence globales (une clé spécifique à MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Réf. spécifique**</dt> </dl> | Position du bit : 1-------<br/> Données de référence spécifiques (clé spécifique à DF).<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Position du bit :-XX-----<br/> 00 (les autres valeurs sont RFU).<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Confidentialité**</dt> </dl>                         | Position du bit :---xxxxx<br/> Numéro du secret.<br/>                                                                                                              |



 

</dd> <dt>

*pChallenge* \[ dans\]
</dt> <dd>

Pointeur vers les données liées à l’authentification (par exemple, Challenge).

</dd> <dt>

*lReplyBytes* \[ dans\]
</dt> <dd>

Nombre maximal d’octets attendus dans la réponse.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé en interne et retourné à l’aide du pointeur *ppCmd* .

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

La réussite de l’exécution de la commande peut être soumise à la réussite des commandes précédentes (par exemple, vérifier ou sélectionner un fichier) ou à des sélections (par exemple, la clé secrète pertinente).

Si une clé et un algorithme sont actuellement sélectionnés lors de l’émission de la commande, la commande peut utiliser la clé et l’algorithme de manière implicite.

Le nombre de fois où la commande est émise peut être enregistré dans la carte pour limiter le nombre de tentatives supplémentaires d’utilisation de la clé secrète ou de l’algorithme approprié.

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
