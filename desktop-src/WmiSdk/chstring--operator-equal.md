---
description: L’opérateur d’assignation CHString (=) réinitialise un objet CHString existant avec de nouvelles données.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'CHString :: Operator = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034620"
---
# <a name="chstringoperator"></a>CHString :: Operator =

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

L’opérateur d’assignation [**CHString**](chstring.md) (=) réinitialise un objet CHString existant avec de nouvelles données.

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*
</dt> <dd>

Assigne une chaîne [**CHString**](chstring.md) à cet objet.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*cascade*
</dt> <dd>

Assigne un caractère à cet objet.

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *PSZ*
</dt> <dd>

Assigne une chaîne terminée par le caractère **null** à cet objet.

</dd> </dl>

## <a name="remarks"></a>Notes

Si la chaîne de destination (autrement dit, le côté gauche) est déjà suffisamment grande pour stocker les nouvelles données, aucune nouvelle allocation de mémoire n’est effectuée. Toutefois, des exceptions de mémoire peuvent se produire chaque fois que vous utilisez l’opérateur d’assignation, car un nouveau stockage est souvent alloué pour contenir l’objet [**CHString**](chstring.md) résultant.

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre l’utilisation de **CHString :: Operator =**:


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>ChString. h (inclure FwCommon. h)</dt> </dl>                                                    |
| Bibliothèque<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll ; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

