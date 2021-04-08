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
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035162"
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

## <a name="remarks"></a>Notes

Définissez cette propriété pour spécifier le nom du fournisseur de services de chiffrement à utiliser avec le contrôle d’inscription de carte à puce. Obtient cette propriété pour récupérer le nom du fournisseur de services de chiffrement spécifié. Si vous ne spécifiez pas de valeur pour cette propriété, la propriété **CSPName** est définie par défaut sur le prénom dans la liste des fournisseurs de services de chiffrement disponibles.

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

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
