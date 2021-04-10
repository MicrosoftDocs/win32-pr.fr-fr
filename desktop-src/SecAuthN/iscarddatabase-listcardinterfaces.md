---
description: La méthode ListCardInterfaces récupère les identificateurs (GUID) de toutes les interfaces prises en charge pour la carte à puce spécifiée.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'ISCardDatabase :: ListCardInterfaces, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201244"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a>ISCardDatabase :: ListCardInterfaces, méthode

\[La méthode **ListCardInterfaces** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ListCardInterfaces** récupère les identificateurs (Guid) de toutes les interfaces prises en charge pour la [*carte à puce*](../secgloss/s-gly.md)spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrCardName* \[ dans\]
</dt> <dd>

Nom de la carte à puce.

</dd> <dt>

*ppInterfaceGuids* \[ à\]
</dt> <dd>

Pointeur vers les GUID d’interface en cas de réussite ; **Null** si l’opération a échoué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                              |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppInterfaceGuids*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                                  |



 

## <a name="remarks"></a>Notes

Pour récupérer le [*fournisseur de services principal*](../secgloss/p-gly.md) de la carte à puce, appelez [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).

Pour récupérer toutes les [*cartes à puce*](../secgloss/s-gly.md)connues, les [*lecteurs*](../secgloss/r-gly.md)et les [*groupes*](../secgloss/r-gly.md) de lecteurs appellent respectivement [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)et [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardDatabase**](iscarddatabase.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre l’extraction des identificateurs des interfaces prises en charge pour la carte à puce spécifiée.


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
