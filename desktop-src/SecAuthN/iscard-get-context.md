---
description: Récupère le handle de contexte du gestionnaire de ressources actuel. Cette méthode retourne ( \* pContext) = = NULL si aucun contexte n’a été établi.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'ISCard :: get_Context, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 82094d51912031655585cacde0b156451107276bc08ca1be6dc6d82bdbb3229d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015629"
---
# <a name="iscardget_context-method"></a>ISCard :: obtient le \_ contexte, méthode

\[La méthode **obtenir le \_ contexte** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode d’extraction de **\_ contexte** récupère le handle de [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md) actuel. Cette méthode retourne ( \* *pContext*) = = **null** si aucun contexte n’a été établi.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pContext* \[ à\]
</dt> <dd>

Pointeur vers le handle de contexte lors du retour.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération exécutée avec succès.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *pContext* n’est pas valide.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Un pointeur incorrect a été passé dans *pContext*.<br/> |



 

## <a name="remarks"></a>Remarques

Le contexte du gestionnaire de ressources est défini en appelant la fonction de [*carte à puce*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer le handle de [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md) actuel.


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
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

[**Obtient \_ ATR**](iscard-get-atr.md)
</dt> <dt>

[**Obtient \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**Obtient le \_ protocole**](iscard-get-protocol.md)
</dt> <dt>

[**afficher l' \_ État**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
