---
description: La méthode FindCard recherche la carte à puce et ouvre une connexion valide à celle-ci.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'ISCardLocate :: FindCard, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a0db06f9dcafd211f628eb7cd0be9ed2f800b6f1b980d8e2320cd82b2849d386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014239"
---
# <a name="iscardlocatefindcard-method"></a>ISCardLocate :: FindCard, méthode

\[La méthode **FindCard** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **FindCard** recherche la [*carte à puce*](../secgloss/s-gly.md) et ouvre une connexion valide à celle-ci.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ShareMode* \[ dans\]
</dt> <dd>

Mode dans lequel partager ou ne pas partager la carte à puce lorsqu’une connexion est ouverte.



| Valeur                                                                                                                                            | Signification                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Or**</dt> </dl> | Personne d’autre n’utilise cette connexion à la carte à puce.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**PARTAGÉ**</dt> </dl>          | D’autres applications peuvent utiliser cette connexion.<br/>        |



 

</dd> <dt>

*Protocoles* \[ dans\]
</dt> <dd>

Protocole à utiliser lors de la connexion à la carte.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Spécifie quand l' [*interface utilisateur*](../secgloss/u-gly.md) s’affiche :



| Valeur                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**\_ \_ interface utilisateur minimale SC DLG \_**</dt> </dl> | Affiche la boîte de dialogue uniquement si la carte recherchée par l’application appelante n’est pas localisée et peut être utilisée dans un lecteur. Cela permet de trouver la carte connectée (via un mécanisme de boîte de dialogue interne ou à l’aide des fonctions de rappel de l’utilisateur) et retournée à l’application appelante.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ non \_ UI**</dt> </dl>                | N’affiche aucune interface utilisateur, quel que soit le résultat de la recherche.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**\_ \_ interface utilisateur force SC DLG \_**</dt> </dl>       | Provoque l’affichage de l’interface utilisateur, quel que soit le résultat de la recherche.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure de données qui contient ou retourne des informations sur la [*carte à puce*](../secgloss/s-gly.md)ouverte, en cas de réussite. Aura la **valeur null** si l’opération a échoué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                        |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppCardInfo*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                            |



 

## <a name="remarks"></a>Remarques

Pour définir les critères de recherche de la recherche, appelez [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) pour spécifier les noms des cartes de carte à puce.

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardLocate**](iscardlocate.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate est défini en tant que 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
