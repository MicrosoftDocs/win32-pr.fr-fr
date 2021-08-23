---
description: Définit ou récupère le nom du fournisseur de services de chiffrement (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'ISCrdEnr :: CSPName, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 7a1b5b443807dfe7fa737cdfc5eb4da678845e53b555ffe6eebf1529583fdb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005227"
---
# <a name="iscrdenrcspname-property"></a>ISCrdEnr :: CSPName, propriété

La propriété **CSPName** définit ou récupère le nom du fournisseur de [*services de chiffrement*](../secgloss/c-gly.md) (CSP).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom du fournisseur de services de chiffrement.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="remarks"></a>Remarques

Définissez cette propriété pour spécifier le nom du fournisseur de services de chiffrement à utiliser avec le contrôle d’inscription de carte à puce. Obtient cette propriété pour récupérer le nom du fournisseur de services de chiffrement spécifié. Si vous ne spécifiez pas de valeur pour cette propriété, la propriété **CSPName** est définie par défaut sur le prénom dans la liste des fournisseurs de services de chiffrement disponibles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
