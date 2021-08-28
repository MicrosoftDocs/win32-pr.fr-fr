---
description: Ferme la connexion ouverte à la carte à puce.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: ISCard ::D méthode Etach (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 527197be4b62820da818d4cc8ea9b6d344630d6d1cdcd8d4bd4ae1e618080015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482259"
---
# <a name="iscarddetach-method"></a>ISCard ::D méthode Etach

\[La méthode de **détachement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Detach** ferme la connexion ouverte à la [*carte à puce*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Disposition* \[ dans\]
</dt> <dd>

Indique ce qui doit être fait avec la carte dans le [*lecteur*](../secgloss/r-gly.md)connecté.



| Valeur                                                                                                                                      | Signification                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**CONGÉ**</dt> </dl>       | Laisse la carte à puce dans l' [*État*](../secgloss/s-gly.md)actuel.<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**RESET**</dt> </dl>       | Réinitialise la carte à puce à un état connu.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**Hors tension**</dt> </dl> | Supprime l’alimentation de la carte à puce.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**ÉMISSION**</dt> </dl>       | Éjecte la carte à puce si le lecteur possède des fonctionnalités d’éjection.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | La *disposition* n’est pas valide.<br/>       |



 

## <a name="remarks"></a>Remarques

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre la fermeture de la connexion à la carte à puce.


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



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
| IID<br/>                      | IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Rattacher**](iscard-reattach.md)
</dt> </dl>

 

 
