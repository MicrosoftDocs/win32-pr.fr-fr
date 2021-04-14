---
description: Construit une commande APDU (Application Protocol Data Unit) qui met à jour l’état de la sécurité de manière conditionnelle, en vérifiant l’identité de l’ordinateur lorsque la carte à puce ne l’approuve pas.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816 :: ExternalAuthenticate, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393551"
---
# <a name="iscardiso7816externalauthenticate-method"></a>ISCardISO7816 :: ExternalAuthenticate, méthode

\[La méthode **ExternalAuthenticate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ExternalAuthenticate** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui met à jour l’état de la sécurité de manière conditionnelle, en vérifiant l’identité de l’ordinateur lorsque la [*carte à puce*](../secgloss/s-gly.md) ne l’approuve pas.

La commande utilise le résultat (oui ou non) du calcul par la carte (en fonction d’une demande précédemment émise par la carte, par exemple par la \_ commande ins obtenir un \_ Challenge), d’une clé (éventuellement secrète) stockée dans la carte et des données d’authentification transmises par l’appareil de l’interface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
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



| Valeur                                                                                                                                                                                    | Signification                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Aucune information**</dt> </dl>                     | Position du bit : 00000000<br/> Aucune information n’est fournie. La référence du secret est connue avant l’émission de la commande ou est fournie dans le champ de données.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Référence globale**</dt> </dl>         | Position du bit : 0-------<br/> Données de référence globales (une clé spécifique à MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Réf. spécifique**</dt> </dl> | Position du bit : 1-------<br/> Données de référence spécifiques (clé spécifique à DF).<br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Position du bit :-XX-----<br/> 00 (les autres valeurs sont RFU).<br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Secret**</dt> </dl>                         | Position du bit :---xxxxx<br/> Numéro du secret.<br/>                                                                                                             |



 

</dd> <dt>

*pChallenge* \[ dans\]
</dt> <dd>

Pointeur vers les données liées à l’authentification. Ce paramètre peut avoir la **valeur null**.

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



 

## <a name="remarks"></a>Notes

Pour que la commande encapsulée réussisse, la dernière demande d’obtention de la carte doit être valide.

Les comparaisons ayant échoué peuvent être enregistrées dans la carte (par exemple, pour limiter le nombre de tentatives supplémentaires d’utilisation des données de référence).

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

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
