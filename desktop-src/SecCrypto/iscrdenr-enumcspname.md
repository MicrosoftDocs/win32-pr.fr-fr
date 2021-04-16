---
description: Énumère le nom des fournisseurs de services de chiffrement (CSP) disponibles.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'ISCrdEnr :: enumCSPName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529992"
---
# <a name="iscrdenrenumcspname-method"></a>ISCrdEnr :: enumCSPName, méthode

La méthode **enumCSPName** énumère le nom des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) disponibles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Index de base zéro de la séquence d’énumération.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé pour un usage futur. Définissez cette valeur sur zéro.

</dd> <dt>

*pbstrCSPName* \[ à\]
</dt> <dd>

Pointeur vers une chaîne qui retourne le nom du fournisseur de services de chiffrement énuméré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="c"></a>C++

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

### <a name="vb"></a>VB

Chaîne qui représente le nom du fournisseur de services de chiffrement énuméré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr :: CSPName**](iscrdenr-cspname.md)
</dt> </dl>

 

 
