---
description: La méthode ListReaderGroups récupère les noms des groupes de lecteurs inscrits dans la base de données de la carte à puce.
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'ISCardDatabase :: ListReaderGroups, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fcfc2ac3e123f45aaa1616eadaea57d5dcb92f3552195eafeee5432216aec491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008087"
---
# <a name="iscarddatabaselistreadergroups-method"></a>ISCardDatabase :: ListReaderGroups, méthode

\[La méthode **ListReaderGroups** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **ListReaderGroups** récupère les noms des groupes de [*lecteurs*](../secgloss/r-gly.md) inscrits dans la base de données de la carte à puce.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LocaleID* \[ dans\]
</dt> <dd>

ID de localisation de la langue.

</dd> <dt>

*ppReaderGroups* \[ à\]
</dt> <dd>

Pointeur vers un SAFEARRAY de BSTR qui contient les noms des groupes de lecteurs de carte à puce qui ont respecté les paramètres de recherche en cas de réussite ; **Null** si l’opération a échoué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                            |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé dans *ppReaderGroups*.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                                |



 

## <a name="remarks"></a>Remarques

Pour récupérer toutes les [*cartes à puce*](../secgloss/s-gly.md) ou [*lecteurs*](../secgloss/r-gly.md)connus, appelez [**ListCards**](iscarddatabase-listcards.md) ou [**ListReaders**](iscarddatabase-listreaders.md) respectivement.

Pour récupérer le [*fournisseur de services principal*](../secgloss/p-gly.md) ou les interfaces d’une carte spécifique [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivement.

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardDatabase**](iscarddatabase.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment récupérer les noms des groupes de lecteurs inscrits dans la base de données de la carte à puce.


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
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
| IID<br/>                      | IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
