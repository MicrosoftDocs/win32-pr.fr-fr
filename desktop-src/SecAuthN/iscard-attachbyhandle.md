---
description: Attache l’objet ISCard à un handle de carte à puce ouvert et configuré.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'ISCard :: AttachByHandle, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011275"
---
# <a name="iscardattachbyhandle-method"></a>ISCard :: AttachByHandle, méthode

\[La méthode **AttachByHandle** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **AttachByHandle** attache l’objet [**ISCard**](iscard.md) à un handle de [*carte à puce*](../secgloss/s-gly.md) ouvert et configuré.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCard* \[ dans\]
</dt> <dd>

Handle d’une connexion ouverte à une carte à puce.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                  | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération exécutée avec succès.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *hCard* n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

Lorsque vous avez terminé d’utiliser le handle, libérez la pièce jointe en appelant la méthode [**ISCard ::D Etach**](iscard-detach.md) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’attachement à un handle de carte à puce.


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a>Spécifications



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

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Detach**](iscard-detach.md)
</dt> <dt>

[**Obtient \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**Rattacher**](iscard-reattach.md)
</dt> </dl>

 

 
