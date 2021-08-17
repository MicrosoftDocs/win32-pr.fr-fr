---
description: La méthode Create crée un fichier à un emplacement donné au sein du système de fichiers de la carte à puce.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'ISCardFileAccess :: Create, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: cc6609e2b39c8e0e6b2c034d9220d78b3e28194ca1d92a383236411e77802164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481309"
---
# <a name="iscardfileaccesscreate-method"></a>ISCardFileAccess :: Create, méthode

\[La méthode **Create** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Create** crée un fichier à un emplacement donné au sein du système de fichiers de la [*carte à puce*](../secgloss/s-gly.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
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

ID de fichier à créer dans le contexte actuel.

</dd> <dt>

*TLV* \[ dans\]
</dt> <dd>

Liste des structures TLV (tag, Length, value) dont les valeurs doivent être définies.

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Spécifie si la messagerie sécurisée doit être utilisée et les données préallouées.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ messagerie sécurisée SC FL \_**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL \_ préalloué**
</dt> </dl> </dd> <dt>

*pDataBuffer* \[ dans\]
</dt> <dd>

Pointeur vers des données préallouées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Remarques

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
