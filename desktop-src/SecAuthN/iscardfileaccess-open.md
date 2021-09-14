---
description: La méthode Open ouvre le fichier spécifié pour une utilisation ultérieure.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'ISCardFileAccess :: Open, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194004"
---
# <a name="iscardfileaccessopen-method"></a>ISCardFileAccess :: Open, méthode

\[La méthode **Open** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Open** ouvre le fichier spécifié pour une utilisation ultérieure.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RefType* \[ dans\]
</dt> <dd>

Type de référence utilisé dans *bstrPathSpec*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ type \_ by \_ Name**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ type \_ by \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ type \_ par \_ short**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ type \_ par \_ any**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ dans\]
</dt> <dd>

Fichier à ouvrir.

</dd> <dt>

*phFile* \[ à\]
</dt> <dd>

Pointeur vers un fichier HSCARD qui contiendra \_ le descripteur de fichier.

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

Pour fermer un fichier, appelez [**Close**](iscardfileaccess-close.md).

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

[**Plus**](iscardfileaccess-close.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
