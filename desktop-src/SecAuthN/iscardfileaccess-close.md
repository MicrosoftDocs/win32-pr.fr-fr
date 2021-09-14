---
description: La méthode Close ferme le fichier spécifié. Aucun autre accès au fichier n’est autorisé.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: 'ISCardFileAccess :: Close, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121182"
---
# <a name="iscardfileaccessclose-method"></a>ISCardFileAccess :: Close, méthode

\[La méthode **Close** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Close** ferme le fichier spécifié. Aucun autre accès au fichier n’est autorisé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFile* \[ dans\]
</dt> <dd>

Handle du fichier à fermer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

Pour ouvrir un fichier, appelez [**Open**](iscardfileaccess-open.md).

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Ouvrir**](iscardfileaccess-open.md)
</dt> </dl>

 

 
