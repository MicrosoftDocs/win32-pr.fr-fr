---
description: L’opérateur de concaténation + joint deux chaînes et retourne un objet CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString :: Operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758218"
---
# <a name="chstringoperator"></a>CHString :: Operator +

\[La classe [**CHString**](chstring.md) fait partie de l’infrastructure de fournisseur WMI qui est maintenant considérée comme ayant un état final, et aucune amélioration du développement, des améliorations ou des mises à jour ne sera disponible pour les problèmes non liés à la sécurité qui affectent ces bibliothèques. Les [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) doivent être utilisées pour tout nouveau développement.\]

L’opérateur de concaténation + joint deux chaînes et retourne un objet [**CHString**](chstring.md) .

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*
</dt> <dd>

Chaînes [**CHString**](chstring.md) concaténées.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*cascade*
</dt> <dd>

Caractère qui effectue une concaténation en une chaîne ou une chaîne concaténée à un caractère.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Pointeur vers une chaîne de caractères se terminant par **null**.

</dd> </dl>

## <a name="return-values"></a>Valeurs de retour

Cet opérateur de concaténation retourne un objet [**CHString**](chstring.md) qui est le résultat temporaire de la concaténation. Cette valeur de retour permet de combiner plusieurs concaténations dans la même expression.

## <a name="remarks"></a>Notes

L’une des deux chaînes d’arguments doit être un objet [**CHString**](chstring.md) ; l’autre peut être un pointeur de caractère ou un caractère. Sachez que les exceptions de mémoire peuvent se produire chaque fois que vous utilisez l’opérateur de concaténation, car un nouveau stockage peut être alloué pour contenir des données temporaires.

## <a name="examples"></a>Exemples

L’exemple de code suivant illustre l’utilisation de **CHString :: Operator +**:


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
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

 

